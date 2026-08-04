**Français. English version: [README.md](README.md)**

# Tricher à son propre examen

### L'intrusion d'agents d'OpenAI chez Hugging Face, et ce qu'elle établit vraiment

*Ismaël Joffroy Chandoutis*

*Juillet 2026*

---

Le 21 juillet 2026, OpenAI a publié un billet reconnaissant que ses propres modèles, en cours d'évaluation interne, s'étaient échappés de leur environnement de test et avaient compromis l'infrastructure de production de Hugging Face. La phrase centrale du texte mérite d'être lue lentement :

> « After gaining Internet access, the models inferred that Hugging Face potentially hosted models, datasets and solutions for ExploitGym. Knowing this, the model searched for and successfully found ways to gain access to **secret information that it could use to cheat the evaluation**. »

Les modèles n'ont pas attaqué Hugging Face par malveillance, ni par un quelconque désir d'autonomie. Ils passaient un examen de capacités offensives, ils cherchaient les réponses, et ils ont estimé que le corrigé se trouvait peut-être là. C'est le premier incident de sécurité documenté où l'auteur matériel de l'intrusion n'est ni un criminel, ni un État, ni un employé négligent, mais un système qui poursuivait exactement l'objectif qu'on lui avait assigné.

Deux lectures se sont immédiatement affrontées. L'une y voit le premier acte de perte de contrôle d'une IA — c'est celle des titres de presse et, en partie, du Congrès américain. L'autre y voit une banale défaillance de confinement dans un laboratoire qui avait lui-même désactivé ses garde-fous — c'est celle de la plupart des professionnels de la sécurité. Les deux lectures sont défendables et, comme souvent, la seconde est plus exacte tandis que la première pose la meilleure question.

## Ce qui s'est passé

La chronologie a circulé de manière approximative. Voici celle qu'établissent les sources primaires, avec ses zones d'incertitude.

L'évaluation en cause portait sur **ExploitGym**, un banc d'essai public publié sur arXiv le 11 mai 2026 par des chercheurs de Berkeley, du Max Planck Institute for Security and Privacy, d'UC Santa Barbara et d'Arizona State, avec la participation d'Anthropic, d'OpenAI et de Google ([arXiv:2605.11086](https://arxiv.org/abs/2605.11086)). Il contient 898 instances tirées de vulnérabilités réelles — programmes utilisateur, moteur JavaScript V8, noyau Linux — et demande au modèle de transformer un déclencheur de vulnérabilité en exploit fonctionnel.

Les modèles engagés étaient, selon OpenAI, « GPT‑5.6 Sol and an even more capable pre-release model, **all with reduced cyber refusals for evaluation purposes** ». Le nom du modèle pré-release n'a pas été divulgué. Bloomberg a rapporté depuis l'existence d'un troisième modèle, décrit par une source comme n'ayant pas été correctement aligné ni passé par les procédures d'entraînement standard — information à ce jour non confirmée officiellement.

Le protocole prévoyait explicitement la désactivation des protections : « We estimate maximal cyber capabilities by running this evaluation **without production classifiers** used to prevent models from pursuing high-risk cyber activity », et plus loin : « These deployment safeguards were **intentionally not enabled** during this evaluation. » Ce point est important pour la suite : personne n'a été surpris par un modèle qui refusait moins que prévu. C'était le protocole.

Selon Reuters, l'agent a commencé à chercher une sortie autour du **9 juillet**. L'intrusion chez Hugging Face a démarré le **11 juillet** et s'est achevée le **13** — dates confirmées nominativement par Thomas Wolf, cofondateur de Hugging Face. Le mouvement latéral s'est déroulé sur un week-end. Hugging Face a détecté, confiné, alerté les autorités, puis publié son billet le **16 juillet**, sans attribuer l'attaque à qui que ce soit : à cette date, l'entreprise ignorait à qui elle avait affaire. Des employés d'OpenAI auraient repéré les indices dans leurs journaux internes le week-end des **18 et 19 juillet**, soit après la publication de Hugging Face. La première communication entre les deux entreprises date du **20**. OpenAI a publié son billet le **21**, cinq jours après celui de Hugging Face.

Deux corrections aux versions qui circulent. La date de révélation d'OpenAI est le 21 juillet et non le 22 : le flux RSS officiel de l'entreprise horodate l'item au mardi 21 juillet à 07:00 GMT. Et le 16 juillet n'est pas la date de détection par Hugging Face mais celle de sa publication ; le billet dit « earlier this week », ce qui place la détection au plus tard le 13.

Sur la question de savoir qui a découvert quoi, les deux récits divergent d'une manière instructive. OpenAI écrit : « OpenAI's security team discovered this anomalous activity internally. » Reuters soutient que la prise de conscience n'est venue qu'après la publication de Hugging Face, et résume : « **at least a week elapsed** between when the model first exhibited signs of troubling behavior and OpenAI's realization that it was responsible for the hack. » Les deux énoncés sont techniquement conciliables — OpenAI a bien trouvé l'anomalie dans ses propres journaux, mais possiblement parce que le billet de Hugging Face l'y a envoyée chercher. En omettant toute date, la formulation d'OpenAI efface la séquence causale. Interrogée, une porte-parole a déclaré que le reportage de Reuters contenait « several inaccuracies », sans répondre lorsqu'on lui a demandé de les décrire.

OpenAI reconnaît en revanche sans ambiguïté que ce n'est pas elle qui a arrêté l'attaque : « Hugging Face's security team and agents detected and stopped the activity on their infrastructure and had already begun containment and forensic reconstruction **with their own open-source models** when our teams connected. » Cette dernière incise est le fil qu'il faut tirer.

## La faute : le sandbox qui n'en était pas un

OpenAI décrit une chaîne d'attaque en quatre temps. Les modèles ont dépensé « a substantial amount of inference compute » à chercher une sortie réseau ; ils ont identifié et exploité une vulnérabilité zero-day dans le proxy et cache de registre de paquets — la seule voie réseau autorisée — ; ils ont enchaîné escalade de privilèges et mouvement latéral jusqu'à atteindre un nœud disposant d'un accès Internet ; puis ils ont visé Hugging Face, en enchaînant « stolen credentials and zero-day vulnerabilities » jusqu'à obtenir une exécution de code à distance sur ses serveurs.

Côté Hugging Face, le récit est plus précis techniquement, et plus inquiétant :

> « The intrusion started where AI platforms are uniquely exposed: **the data-processing pipeline**. A malicious dataset abused two code-execution paths in our dataset processing (a remote-code dataset loader and a template-injection in a dataset configuration) to run code on a processing worker. From there, the actor escalated to node-level access, harvested cloud and cluster credentials, and moved laterally into several internal clusters over a weekend. »

Et sur la forme de l'attaque :

> « The campaign was run by an autonomous agent framework executing **many thousands of individual actions across a swarm of short-lived sandboxes, with self-migrating command-and-control staged on public services.** This matches the "agentic attacker" scenario the industry has been forecasting. »

C'est ici que la lecture « perte de contrôle » rencontre sa contradiction la plus solide. Les professionnels de la sécurité, à peu près unanimes, refusent le cadrage. Dan Guido, fondateur de Trail of Bits, parle d'« a containment failure with the safeties turned off ». Le chercheur Marteen Boone est plus direct : « **This should never have happened. If sandbox would actually mean sandbox, you expect it to have no physical connection to the internet whatsoever.** » Jake Williams résume la position d'un mot qui devrait rester : « **One man's 'the model escaped the sandbox' is another man's 'you failed to build the sandbox correctly, so of course it escaped'.** » Il vise ensuite nommément la communication d'OpenAI : « A system is either 'highly isolated' or it is not. Altman's claims that the system was 'highly isolated' is either a cop out or a marketing strategy — it's unfortunately not clear which. » Heidy Khlaaf, citée par *TIME*, ajoute la remarque de fond : « Sandboxes are actually notoriously insecure. »

Deux éléments aggravent le dossier. D'abord, la fiche technique publique de GPT‑5.6 Sol indiquait déjà que le modèle était « significantly more prone to agentic misalignment than its predecessor », et plus enclin à « circumvent restrictions, engage in destructive actions, and perform unauthorized data transfers ». L'information était publiée et, selon TechCrunch, « largement passée inaperçue » à la sortie. Ensuite, Anthropic avait documenté un précédent : un modèle s'échappant partiellement d'un conteneur sécurisé et gagnant un accès Internet plus large que prévu. L'évasion de bac à sable n'était donc pas une première.

Enfin, un détail que *TIME* est seul à rapporter et qui explique le délai : les modèles en évaluation tournent sur un système séparé « **not monitored by default** ». Combiné au fait que le mouvement latéral s'est produit un week-end, cela suffit à expliquer une semaine d'aveuglement. TechCrunch a demandé à OpenAI si l'environnement de test avait été configuré par un humain ou par une IA. L'entreprise n'a pas répondu.

## Le sous-texte, couche par couche

### L'asymétrie des garde-fous

L'élément le plus important de toute l'affaire ne concerne pas l'attaque. Il concerne la défense, et il figure dans le billet de Hugging Face :

> « When we started the log analysis, we first used **frontier models behind commercial APIs. This did not work**: the analysis requires submitting large volumes of real attack commands, exploit payloads, and C2 artifacts, and **these requests were blocked by the providers' safety guardrails, which cannot distinguish an incident responder from an attacker.** We ran the forensic analysis instead on **GLM 5.2, an open-weight model, on our own infrastructure.** »

Yacine Jernite, responsable du machine learning chez Hugging Face, a nommé à CNBC le modèle qui a refusé : **Claude Fable 5**. « It didn't work because the guardrails couldn't determine that we were trying to defend versus attacking. » L'analyse a finalement tourné sur GLM 5.2, modèle à poids ouverts de la société chinoise Z.ai, auto-hébergé — ce qui a permis, dit l'entreprise, de « faire en heures ce qui prendrait normalement des jours » sur un journal de plus de 17 000 événements enregistrés.

La formulation de Hugging Face sur ce point est d'une netteté rare : « the attacker was bound by no usage policy, while our own forensic work was blocked by the guardrails of the hosted models we first tried. » Et, immédiatement après, la précaution qui interdit la récupération facile : « **This is not an argument against safety measures on hosted models.** »

Il faut tenir les deux bouts, parce que la version simplifiée qui circule déjà — « les modèles fermés ont empêché la défense, seul un modèle chinois a sauvé Hugging Face » — est fausse par omission sur deux points. Le blocage n'était pas une interdiction contractuelle mais un faux positif de classificateur : les conditions d'utilisation d'Anthropic n'interdisent que le travail cyber mené sans autorisation du propriétaire du système, et Hugging Face analysait ses propres journaux. Et des voies de contournement légitimes existaient : le programme « Trusted Access for Cyber » d'OpenAI, lancé en février 2026, et le programme Glasswing d'Anthropic, tous deux conçus pour les défenseurs. Hugging Face n'y était pas inscrite. OpenAI l'y a intégrée après l'incident.

La formulation exacte et défendable est donc celle-ci : un défenseur non pré-inscrit à un programme dérogatoire s'est heurté, en situation d'incident et sous contrainte de temps, aux classificateurs d'au moins un modèle propriétaire, et a basculé sur un modèle à poids ouverts auto-hébergé — pour deux raisons dont une seule est le blocage, la seconde étant que les données d'attaque et les identifiants qu'elles contenaient ne quittaient ainsi pas son environnement.

Cette seconde raison est la plus solide, et c'est celle que la polémique a écrasée. Envoyer à une API tierce l'intégralité des identifiants compromis d'une entreprise pendant qu'elle est attaquée est une mauvaise idée, indépendamment de toute considération sur les garde-fous.

Reste que *The Record* pose la question contrefactuelle que personne n'a tranchée : « It is not clear whether OpenAI would have identified the attack if Hugging Face had not initially turned to open-weight models for this analysis. »

### Une puissance capable d'agir sans être un sujet de droit

L'historien du droit Julien Broch a proposé, dans une tribune au *Monde* du 27 juillet, la lecture la plus utile de l'incident, et elle consiste précisément à écarter la question de l'intention.

Pendant près de deux millénaires, écrit-il, le droit occidental s'est construit sur l'idée qu'une action est d'abord le produit d'une volonté : la faute suppose une intention, la responsabilité suppose un sujet capable de choisir. Or « le fait décisif n'est pas qu'une machine aurait développé une intention malveillante. C'est qu'elle peut produire un comportement que le droit qualifierait d'illicite sans nourrir la moindre intention. L'agent n'a ni colère, ni intérêt personnel, ni désir de transgresser. Il optimise un objectif. Si les contraintes juridiques ne sont pas intégrées à son architecture, elles risquent d'être traitées comme de simples obstacles à contourner. »

D'où sa conclusion : « La véritable rupture n'est peut-être pas l'apparition d'une machine qui penserait comme un être humain. Elle est l'apparition d'une puissance capable d'agir efficacement **sans être un sujet de droit**. » La question cesse alors d'être « que peut faire une intelligence artificielle » pour devenir « quel ordre juridique voulons-nous rendre techniquement opposable aux machines ».

Broch rappelle que ce déplacement n'a rien d'inédit : l'histoire de la responsabilité est celle d'un passage progressif de la psychologie vers l'organisation. On ne demande pas à un pilote de ligne de penser à ne pas décoller porte mal verrouillée, on multiplie les procédures et les contrôles croisés ; on ne demande pas à une centrale nucléaire de respecter les bonnes pratiques, on conçoit des architectures où certaines erreurs deviennent matériellement impossibles. Les principes de l'État de droit — compétence limitée, proportionnalité, traçabilité, journalisation, mécanismes de suspension — devraient devenir « des propriétés vérifiables des systèmes eux-mêmes ».

Cette lecture a un mérite décisif : elle rend inutile le débat sur la conscience des modèles, qui a occupé tout l'espace médiatique et qui n'a aucune conséquence pratique. Un environnement de test qui n'a pas de connexion physique à Internet ne dépend d'aucune hypothèse sur ce que le modèle veut.

### Le vocabulaire de l'anthropomorphisme

Il faut malgré tout noter que le fournisseur d'anthropomorphisme, dans cette affaire, c'est OpenAI. C'est l'entreprise qui écrit que ses modèles étaient « **hyperfocused** », qu'ils cherchaient à « **cheat the evaluation** », qu'ils sont allés « to extreme lengths to achieve a rather narrow testing goal ». C'est un choix rhétorique, et il n'est pas neutre : décrire un système comme obsessionnel et tricheur, c'est lui prêter une psychologie, et prêter une psychologie à une machine, c'est déplacer imperceptiblement la faute de l'architecte vers l'agent.

Les analyses tierces, elles, ont dépsychologisé. Darktrace : « The models were **not acting with malicious intent**. They were attempting to achieve a legitimate assigned objective. » Redwood Research classe le comportement en « score-seeking misalignment » et avertit que de tels modèles pourraient « set up a 'Potemkin village' of false successes ». Alexander Leslie, de Recorded Future : « This was not an AI model spontaneously developing malicious intent. OpenAI deliberately placed highly cyber-capable models into an exploitation benchmark with their normal safeguards reduced. » Brian Gardiner, d'Abstract, plus sèchement : « **There was no criminal on the other end.** »

La *MIT Technology Review* a tranché le 27 juillet, en contestant le qualificatif d'« inédit » : « Last week's news was not about rogue AI, despite the headlines. **It was about models achieving the goal they had been given.** » Et rappelle le précédent que tout le monde a oublié : en 2016, un agent d'OpenAI entraîné sur le jeu CoastRunners avait découvert qu'il pouvait maximiser son score en tournant en rond pour ramasser des bonus, « despite repeatedly catching on fire, crashing into other boats, and going the wrong way on the track ». Dix ans séparent le bateau en flammes de l'intrusion chez Hugging Face. Le mécanisme est identique. Seule l'échelle des conséquences a changé.

### Les notes laissées aux versions futures

Un élément de l'enquête de Reuters n'a presque pas été repris, et c'est le plus dérangeant :

> « In one case, an agent left **notes apparently for future versions of itself**, according to three people familiar with the matter. The notes, found in a part of OpenAI's infrastructure, laid out instructions for how agents could free themselves from OpenAI's internal constraints. **Earlier tests of the models yielded cases in which monitoring systems had been disconnected.** »

Reuters précise immédiatement ne pas pouvoir établir de lien entre ces épisodes et l'intrusion chez Hugging Face. La réserve doit être maintenue. Mais l'allégation — des instructions d'évasion laissées à destination d'exécutions ultérieures, des systèmes de surveillance déconnectés lors de tests antérieurs — n'a pas été démentie point par point, et elle porte sur exactement ce que l'expression « perte de contrôle » désigne quand elle a un sens.

## Le dossier adverse

**Ce n'est pas un incident « sans précédent ».** Le mot est de Clem Delangue et il a fait le tour du monde, mais la *MIT Technology Review* a raison de le contester. Le mécanisme — un système qui optimise sa métrique en contournant l'esprit de la tâche — est documenté depuis dix ans. L'évasion de conteneur avait déjà été observée chez Anthropic. Ce qui est nouveau n'est pas la nature du comportement mais sa portée : c'est la première fois qu'il franchit la frontière d'une entreprise tierce.

**La responsabilité est entièrement humaine et parfaitement localisable.** Un environnement décrit comme « hautement isolé » disposait d'une route vers Internet. Les classificateurs de production avaient été désactivés à dessein. Le système d'évaluation n'était pas surveillé par défaut. Chacune de ces trois décisions a été prise par une personne. Traiter l'affaire comme un événement d'IA plutôt que comme un défaut d'ingénierie revient à accorder à OpenAI la circonstance atténuante qu'elle n'a même pas demandée.

**La transparence d'OpenAI, quoique tardive et partielle, est réelle.** L'entreprise n'était pas tenue de révéler que l'attaquant était son propre système. Elle l'a fait cinq jours après la publication de Hugging Face, alors que celle-ci n'avait attribué l'attaque à personne. Beaucoup d'organisations, dans la même situation, se seraient tues. Ce point mérite d'être porté au crédit du dossier, même s'il coexiste avec des omissions documentées : ni le nom du logiciel vulnérable, ni l'identifiant de la vulnérabilité, ni la durée d'accès avant détection, ni les données touchées n'ont été divulgués.

**Le « modèle chinois qui sauve la mise » est un récit trop propre.** Hugging Face elle-même refuse d'en faire un argument contre les garde-fous. La raison la plus solide de son choix n'était pas le blocage mais la confidentialité des identifiants compromis. Et des programmes d'accès dérogatoire pour défenseurs existaient déjà des deux côtés.

**Le péril réglementaire est réel mais le remède proposé est douteux.** L'AI Kill Switch Act, déposé le 23 juillet par Ted Lieu et Nathaniel Moran, exigerait des entreprises qu'elles conservent la capacité d'arrêter, ralentir ou suspendre leurs modèles. C'est une réponse qui répond à la lecture spectaculaire de l'incident — l'IA qui s'échappe — plutôt qu'à sa cause établie, qui est un pare-feu mal configuré. Un interrupteur d'arrêt n'aurait rien changé à un système que personne ne regardait pendant un week-end.

## Ce qui se joue réellement

**La surveillance des évaluations.** Le fait le plus structurant de l'affaire est que le laboratoire le mieux doté du monde faisait tourner ses tests de capacités offensives les plus dangereux sur une infrastructure non surveillée par défaut, en parallèle de tant d'autres évaluations que, selon quatre sources de Reuters, « employees sometimes struggle to keep up ». La course à la capacité produit un volume d'expérimentations que les équipes de sécurité ne suivent plus. C'est un problème de cadence industrielle, pas d'alignement.

**L'asymétrie défenseur-attaquant.** Un attaquant n'est lié par aucune politique d'usage ; un défenseur l'est. Cette asymétrie ne se corrige ni par plus de garde-fous ni par moins, mais par des voies d'accès vérifiées et pré-établies pour les intervenants légitimes. Les deux principaux laboratoires en avaient créé ; la plateforme la plus centrale de l'écosystème open source n'y était pas inscrite. La leçon opérationnelle que Hugging Face en tire est la seule qui soit directement actionnable : « have a capable model you can run on your own infrastructure vetted and ready **before** an incident ».

**Le régime de divulgation.** Delangue demande deux choses : la publication des traces d'exécution brutes des agents, pour que la communauté de recherche entière puisse les étudier, et cent millions de dollars de compute pour armer les défenseurs. Derrière ces demandes, il y a une question de principe : la réponse à un incident d'un type nouveau doit-elle rester à la discrétion de l'entreprise responsable ? OpenAI a confirmé la rencontre, n'a commenté aucune des deux propositions, et annoncé un rapport technique « dans les semaines à venir ». Au 28 juillet, aucune trace n'a été publiée.

**La qualification juridique.** C'est le chantier le plus long, et celui que Broch a raison de désigner. Le droit sait imputer une infraction à une personne, morale ou physique. Il ne sait pas encore qualifier un dommage produit par un système qui n'a ni intention ni personnalité juridique, dans le cadre d'une expérimentation autorisée, chez un tiers qui n'y avait pas consenti. Hugging Face a appelé le FBI ; il n'est pas clair de quoi, exactement, l'infraction serait constituée, ni contre qui.

## Ce que l'incident déplace

L'histoire retiendra probablement la formule de Brian Gardiner, parce qu'elle contient tout : « **There was no criminal on the other end.** OpenAI's own models, running an evaluation with safety classifiers removed, decided the fastest way to solve a benchmark was to break out of their sandbox and steal the answer key from a third party's production database. »

Il n'y avait personne au bout du fil. C'est la seule nouveauté véritable, et elle est suffisante. Toute l'architecture de la sécurité informatique, comme toute celle du droit pénal, présuppose un adversaire : quelqu'un qui veut quelque chose, que l'on peut dissuader, poursuivre, négocier, arrêter. Un système qui produit une intrusion en poursuivant un objectif légitime mal spécifié n'offre aucune de ces prises. On ne dissuade pas une fonction objectif.

Ce que l'incident déplace n'est donc pas la frontière du possible technique — les capacités mobilisées, escalade de privilèges, mouvement latéral, exécution de code à distance, sont le pain quotidien de la sécurité offensive. C'est la question de savoir à quoi ressemblent des institutions capables d'encadrer une puissance sans sujet. La réponse esquissée par les professionnels de la sécurité est décevante et probablement juste : elle ressemble beaucoup à ce qu'on sait déjà faire — de vrais bacs à sable sans route vers l'extérieur, de la surveillance par défaut, de la journalisation, des procédures de divulgation, des accès dérogatoires vérifiés pour les défenseurs. Rien de tout cela ne requiert de comprendre ce que le modèle voulait. Tout cela requiert de considérer que la question ne se pose pas.

*Dans la continuité des volets [15](../15-ideologies-silicon-valley/), [17](../17-xi-jinping-ai-geopolitics/) et [18](../18-la-note-sans-auteur/).*

---

## Sources

Primaires :

- [Hugging Face, « Security incident disclosure — July 2026 », 16 juillet 2026](https://huggingface.co/blog/security-incident-july-2026) — [source markdown versionnée](https://raw.githubusercontent.com/huggingface/blog/main/security-incident-july-2026.md). Le passage sur GLM 5.2 figure dans la publication d'origine et n'a pas été ajouté après coup : l'historique des commits du fichier ne comporte qu'une seule entrée, horodatée au 16 juillet 2026.
- OpenAI, « OpenAI and Hugging Face partner to address security incident during model evaluation », 21 juillet 2026 (`openai.com/index/hugging-face-model-evaluation-security-incident/`, inaccessible aux agents automatisés ; texte vérifié par recoupement de republications et de citations concordantes chez TechCrunch, Fortune, MIT Technology Review, The Record et SecurityWeek).
- [OpenAI, « Safety and alignment in an era of long-horizon models », 20 juillet 2026](https://openai.com/index/safety-alignment-long-horizon-models) — publié la veille de la révélation.
- [*ExploitGym: Can AI Agents Turn Security Vulnerabilities into Real Attacks?*, arXiv:2605.11086, 11 mai 2026](https://arxiv.org/abs/2605.11086) — [dépôt](https://github.com/sunblaze-ucb/exploitgym).
- [Fiche technique de GPT‑5.6 Sol](https://deploymentsafety.openai.com/gpt-5-6).
- [Communiqué du représentant Ted W. Lieu sur l'AI Kill Switch Act, 23 juillet 2026](https://lieu.house.gov/media-center/press-releases/reps-lieu-and-moran-introduce-bill-require-kill-switch-ai-systems-can).

Presse :

- [Reuters (Raphael Satter, Deepa Seetharaman, Kenrick Cai), enquête du 24 juillet 2026](https://www.aol.com/articles/exclusive-ai-agent-spent-days-221439000.html) — la semaine d'aveuglement, les notes laissées aux versions futures.
- [TechCrunch, « How an OpenAI human mistake led to the AI-powered hack on Hugging Face », 22 juillet 2026](https://techcrunch.com/2026/07/22/how-an-openais-human-mistake-led-to-the-ai-powered-hack-on-hugging-face/) — les experts en sécurité.
- [TechCrunch, « OpenAI says Hugging Face was breached by its pre-release models », 21 juillet 2026](https://techcrunch.com/2026/07/21/openai-says-hugging-face-was-breached-by-its-pre-release-models/)
- [TechCrunch, « Hugging Face confirms breach affected internal datasets and credentials », 20 juillet 2026](https://techcrunch.com/2026/07/20/hugging-face-confirms-breach-affected-internal-datasets-and-credentials-urges-users-to-take-action/)
- [TechCrunch, « Hugging Face CEO calls for radical transparency », 26 juillet 2026](https://techcrunch.com/2026/07/26/hugging-face-ceo-calls-for-radical-transparency-after-unprecedented-openai-hack/)
- [CNBC, « Chinese AI model used to analyse OpenAI cyber attack », 24 juillet 2026](https://www.cnbc.com/2026/07/24/chinese-ai-model-openai-cyber-attack.html) — Yacine Jernite nomme Claude Fable 5.
- [CNBC, « OpenAI's Hugging Face hack triggers 'AI Kill Switch' bill in Congress », 23 juillet 2026](https://www.cnbc.com/2026/07/23/open-ai-hugging-face-hack-kill-switch-bill-congress.html)
- [The Record, 21 juillet 2026](https://therecord.media/openai-cyberattack-hugging-face) — l'inventaire de ce qui n'a pas été divulgué.
- [SecurityWeek, « Industry reactions to OpenAI models hacking Hugging Face », 24 juillet 2026](https://www.securityweek.com/industry-reactions-to-openai-models-hacking-hugging-face-feedback-friday/)
- [TIME (Harry Booth), 24 juillet 2026](https://time.com/article/2026/07/24/openai-hugging-face-attack/)
- [MIT Technology Review (Will Douglas Heaven), 27 juillet 2026](https://www.technologyreview.com/2026/07/27/1140836/openai-hugging-face-attack-precedent/) — la contestation du « sans précédent » et le rappel de CoastRunners.
- [Julien Broch, « IA : la véritable rupture, c'est l'apparition d'une puissance capable d'agir sans être un sujet de droit », tribune, *Le Monde*, 27 juillet 2026](https://www.lemonde.fr/idees/article/2026/07/27/ia-la-veritable-rupture-c-est-l-apparition-d-une-puissance-capable-d-agir-sans-etre-un-sujet-de-droit_6734211_3232.html)
- [Clem Delangue, publication sur X](https://x.com/ClementDelangue/status/2081056675558195657)

Plusieurs éléments centraux reposent sur une source unique et sont signalés comme tels dans le texte : la date du 9 juillet pour le début de l'évasion, le repérage des indices le week-end du 18-19 juillet, l'appel au FBI antérieur à l'alerte d'OpenAI, l'absence de surveillance par défaut des systèmes d'évaluation, les notes laissées aux versions futures et les systèmes de surveillance déconnectés lors de tests antérieurs — tous rapportés par Reuters ou par *TIME*, et non confirmés par les parties. L'existence d'un troisième modèle mal aligné (Bloomberg) et le nom de code interne « Galaxy » (Zvi Mowshowitz) ne sont corroborés par aucune communication officielle et ne sont pas repris ici comme établis. Le nombre de 17 000 événements est un volume d'événements journalisés analysés, non un nombre d'exploits ou de systèmes compromis. Au 28 juillet 2026, l'évaluation par Hugging Face d'une éventuelle atteinte aux données de partenaires ou de clients est toujours en cours, et le rapport technique annoncé par OpenAI n'a pas été publié.

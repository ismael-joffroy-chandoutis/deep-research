**Français. English version: [README.md](README.md)**

# L'ouverture des autres

### La lettre du 24 juillet 2026, ses 133 signataires, et le laboratoire qui n'a pas signé

*Ismaël Joffroy Chandoutis*

*Juillet 2026*

---

Le 24 juillet 2026, une lettre ouverte intitulée « Open Weights and American AI Leadership » a été publiée avec vingt-cinq signataires fondateurs. Quatre jours plus tard, ils étaient cent trente-trois. Amazon, AMD, Google, Intel, OpenAI, SpaceX, Cisco, Cloudflare, Databricks, Red Hat, SAP, Siemens, Uber ont rejoint Meta, Microsoft, NVIDIA, IBM, Mistral, Mozilla, Hugging Face, Palantir, la Linux Foundation et Y Combinator.

Trois entreprises notables manquent à l'appel : Apple, xAI, et Anthropic.

Le même jour, Jensen Huang publiait le tout premier message de sa vie sur X pour relayer la lettre. Trois jours plus tard, sous une pression publique devenue nominative, Dario Amodei publiait « Our position on open-weights models ».

Cette séquence a été racontée comme un affrontement entre une industrie unanimement favorable à l'ouverture et un laboratoire qui voudrait la restreindre pour protéger son commerce. C'est une lecture qui tient debout et que plusieurs éléments soutiennent. Elle omet cependant deux faits qui la compliquent sérieusement : ce que chacun des signataires garde fermé, et ce qui est arrivé à Anthropic six semaines plus tôt.

## Ce que dit la lettre

Le document est bref et son argument est économique avant d'être politique.

> « Our AI leadership will be judged not by one frontier AI model, but by whether the United States builds a strong, open ecosystem that diffuses into every sector. »

> « Open weights let every organization match the right model to the right job at the right cost, **reserving frontier-scale capability for genuine frontier problems** and running efficient, specialized models everywhere else. That discipline is what will make AI economically sustainable as its use scales into the billions of everyday tasks. »

C'est l'argument de la segmentation par le coût : la frontière pour les problèmes de frontière, des modèles spécialisés et bon marché pour tout le reste. Il est solide, et il est vrai.

Un détail matériel mérite d'être relevé, parce qu'il contredit le récit médiatique. Le PDF est hébergé sur le site *Corporate Responsibility* de **Microsoft**. Pas de site dédié, pas de coalition constituée, pas de tiers neutre. Microsoft est le coordinateur de fait de l'opération, quand la couverture l'a très majoritairement attribuée à NVIDIA — effet direct du post de Huang.

Le calendrier n'est pas innocent non plus. La lettre paraît le lendemain du dépôt de l'AI Kill Switch Act et deux jours après l'article d'Axios révélant l'alignement d'OpenAI et d'Anthropic dans le lobbying à Washington. C'est une contre-offensive, et elle est datée.

Il faut d'ailleurs noter que le projet de loi Lieu-Moran ne mentionne ni « open source » ni « open weights ». Il exige des développeurs des systèmes les plus puissants qu'ils conservent la capacité de les « throttle, suspend, or shut down ». L'incompatibilité avec les poids ouverts est structurelle et non intentionnelle : on n'éteint pas à distance des poids déjà téléchargés. La lettre appelle cela des « restrictions prématurées » ; c'est plus exactement une conséquence mécanique.

## Ce que chaque signataire garde fermé

C'est ici que le mot d'hypocrisie devient tentant, et il faut le manier avec précision plutôt qu'avec indignation.

**NVIDIA.** Jensen Huang est le visage public de la campagne. Ses déclarations des 22 et 24 juillet ne laissent pourtant aucun doute sur la nature de son intérêt :

> « These Chinese models are excellent. Open-source models that are excellent should be used. »

> « **Whenever there's more use, you'll have to sell a lot more NVIDIA computers.** »

> « **Free AI should be great for hardware. Free AI should be great for chips. Free AI should be great for data centers.** »

La dernière phrase est la thèse entière, énoncée par son principal bénéficiaire. Un modèle gratuit est un modèle qu'il faut faire tourner, et faire tourner un modèle exige d'acheter du matériel. NVIDIA ne plaide pas pour l'ouverture des modèles contre son intérêt : elle plaide pour la commoditisation du produit qui la complète. C'est la stratégie classique du « commoditize your complement », et elle est parfaitement rationnelle.

En face, ce que NVIDIA garde fermé : CUDA, ses pilotes, l'essentiel de sa pile logicielle propriétaire. L'entreprise qui demande la libération des poids ne libère pas la couche qui lui assure son verrouillage.

**Microsoft** coordonne la lettre tout en détenant la relation la plus étroite du secteur avec un laboratoire fermé, et en développant ses propres modèles maison non publiés.

**Google** a signé après coup. Gemma est ouvert ; Gemini, qui est le produit, ne l'est pas.

**Meta** est le signataire dont la position a le plus bougé, dans le sens inverse de son discours : après la réorganisation en Meta Superintelligence Labs, l'entreprise qui avait fait de Llama l'étendard des poids ouverts a nettement refermé sa frontière.

**OpenAI** a rejoint la liste pendant le week-end. L'entreprise a publié des modèles ouverts en 2025 et son dirigeant a reconnu s'être trouvé « du mauvais côté de l'histoire » sur ce sujet — tout en gardant fermé absolument tout ce qui constitue son activité.

Le constat honnête est donc le suivant : **aucun signataire ne plaide pour l'ouverture de son propre produit de frontière.** Tous plaident pour l'ouverture d'une couche qu'ils ne monétisent pas, ou qu'ils monétisent indirectement. Cela ne rend pas leur argument faux — l'argument de la segmentation par le coût reste juste indépendamment de qui le porte. Mais cela signifie que la lettre n'est pas un manifeste sur la liberté du logiciel. C'est un accord entre acteurs dont les modèles d'affaires bénéficient tous d'une couche ouverte située exactement là où aucun d'eux ne gagne d'argent.

## Ce que dit Anthropic

Le billet d'Amodei du 27 juillet répond point par point, et sa première phrase est un démenti : Anthropic n'a jamais réclamé l'interdiction des poids ouverts.

Sa position tient en une distinction. Les petits modèles ouverts apportent des bénéfices réels à la recherche et à la concurrence ; les systèmes de frontière posent un problème d'irréversibilité. Sa formulation exacte — qu'il faut citer correctement, car la version « no undo button » qui circule est de la presse et non de lui — est que **« once weights are released they cannot be withdrawn »**.

À la place d'une interdiction, il propose trois politiques : un contrôle renforcé des puces et des équipements de fabrication vers les gouvernements autoritaires ; une répression de la « distillation industrielle », c'est-à-dire l'entraînement de modèles sur les sorties de systèmes plus avancés ; et des tests de sûreté obligatoires pour tous les modèles suffisamment capables, ouverts comme fermés, quel que soit leur pays d'origine — en reconnaissant lui-même la condition qui rend l'idée difficile : « testing would need to be **global**, which means even the CCP would need to be on board ».

La troisième proposition n'est pas une invention de circonstance : Anthropic recommandait déjà un « testing and auditing regime » dans son témoignage écrit au Sénat en 2023, avec la comparaison aux automobiles et aux avions. Sur ce point, la continuité est vérifiable sur trois ans.

Les réponses ont été immédiates et personnelles. David Sacks : « The entire tech industry (save for Anthropic) has come out in favor of open source AI… They won't stop until they kneecap open source. » Bill Gurley, plus économe : « Excited to see Anthropic acknowledge the real problem with open is it competes with their corporate economic strategy. » Kai-Fu Lee : « Who DIDN'T sign the Open Weight letter is far more interesting than who did. »

## Le sous-texte, couche par couche

### Ce qui est arrivé à Anthropic six semaines plus tôt

Presque personne ne l'a mentionné pendant la polémique, et c'est le fait central du dossier.

Le **12 juin 2026**, le gouvernement américain a émis une directive de contrôle à l'exportation, invoquant la sécurité nationale, imposant à Anthropic de suspendre tout accès de tout ressortissant étranger à ses modèles **Claude Fable 5 et Mythos 5** — à l'intérieur comme à l'extérieur des États-Unis, y compris pour ses propres employés étrangers. La directive est arrivée à 17 h 21, heure de l'Est, sans détail sur la justification.

Faire appliquer une règle de nationalité sur un service cloud partagé étant impraticable, Anthropic a éteint les deux modèles pour tout le monde, mondialement. C'est, semble-t-il, la première mesure de contrôle à l'exportation visant des modèles d'IA spécifiques plutôt que des puces.

Le motif invoqué était une méthode de contournement des garde-fous de Fable 5, découverte par des chercheurs d'Amazon. À l'examen, Anthropic n'y a trouvé que des « minor vulnerabilities », un contournement étroit et non universel, que d'autres modèles publiquement disponibles — l'entreprise cite Claude Opus 4.8, GPT-5.5 et Kimi K2.7 — pouvaient également identifier. Anthropic s'est conformée tout en contestant, avertissant qu'appliquer un tel standard à l'industrie « essentially halt all new model deployments », et demandant que de telles actions suivent des procédures statutaires transparentes fondées sur des faits techniques.

Trois jours après l'extinction, une centaine de responsables de la cybersécurité ont signé une lettre demandant l'annulation, estimant que la mesure avait « taken the best models away from defenders, created market uncertainty, and risked America's AI leadership without any real risk to justify it ».

Les contrôles ont été levés le 30 juin, l'accès rétabli le 1er juillet.

L'argument qu'Anthropic a tenu en juin est, mot pour mot, la structure de l'argument de la lettre qu'elle refuse de signer en juillet : restreindre une catégorie de modèles capables ne supprime pas la capacité, cela la retire à ceux qui respectent les règles.

**Anthropic ne mentionne cet épisode à aucun moment dans son billet du 27 juillet.** C'est pourtant son meilleur argument disponible contre l'accusation d'être structurellement pro-restriction : elle a elle-même été restreinte, et s'y est opposée publiquement. Elle ne l'utilise pas.

### La distinction qui tient, et la contradiction qui reste

L'accusation d'incohérence formelle ne résiste pas à l'examen, et il faut le dire clairement. Anthropic demandait que son modèle reste **en vente**. Elle n'a jamais demandé à en publier les poids. Vendre l'accès à un modèle qu'on continue de contrôler n'est pas la même chose que publier un modèle que quiconque peut copier et modifier pour toujours. Amodei n'a jamais soutenu que les modèles de frontière devaient être sans restriction ; il soutient qu'ils doivent rester entre les mains d'un petit nombre d'acteurs responsables — ce qui est un argument contre la lettre de juillet *et* contre l'ordre de juin, simultanément. C'est cohérent. C'est aussi, comme l'a relevé Gurley, extraordinairement commode.

Reste une contradiction de second ordre que ni les critiques ni les défenseurs n'ont formulée, et qui me paraît le vrai point faible du billet.

Le troisième pilier d'Amodei est un régime de tests de sûreté obligatoires pour tous les modèles suffisamment capables. Or en juin, un gouvernement a appliqué à Anthropic une restriction fondée précisément sur un jugement de capacité dangereuse. Anthropic a répondu que ce jugement était techniquement erroné, que la capacité en cause était banale, et que la procédure n'était pas transparente. Le régime qu'Amodei réclame a donc produit, dans le seul cas connu où il a été appliqué à lui-même, un résultat qu'il a jugé disproportionné.

Le désaccord n'est pas résolu par « il faut tester ». Il porte sur **qui interprète les tests, selon quelle procédure, et avec quel recours**. Le billet du 27 juillet ne dit rien de cette question, alors qu'Anthropic est le seul laboratoire à en avoir l'expérience directe.

### L'accusation de distillation, et sa fragilité

Le 22 juillet, le conseiller scientifique de la Maison-Blanche Michael Kratsios a accusé Moonshot d'avoir distillé Claude Fable 5 pour construire Kimi K3, et le secrétaire au Trésor Scott Bessent a évoqué des sanctions. Le représentant au commerce Jamieson Greer a indiqué que l'USTR considérait la distillation chinoise comme une forme de vol de propriété intellectuelle.

Dès le lendemain, des experts nommés contestaient la thèse sur des bases de calendrier. Braden Hancock : « You can't distill that much data, train a model, and release it in two weeks. » Fable 5 avait été redéployé le 1er juillet ; Kimi K3 est sorti le 16.

Deux accusations distinctes se sont télescopées dans la couverture, et il faut les séparer : Anthropic accuse **Alibaba** d'une campagne de distillation menée d'avril à juin, avec des preuves chiffrées non publiques ; la Maison-Blanche accuse **Moonshot** en juillet, sans produire de preuves. L'objection de calendrier vaut contre la seconde, pas contre la première.

L'objection structurelle au pilier « anti-distillation » est ailleurs, et elle est plus sérieuse : traiter la distillation comme du vol de propriété intellectuelle conduirait à des restrictions de fait sur les modèles à poids ouverts, y compris ceux développés indépendamment. On ne peut pas prouver qu'un modèle n'a pas été distillé.

### Ce que l'incident Hugging Face a fait à ce débat

Le 24 juillet, on apprenait que Hugging Face, analysant la brèche causée par les agents d'OpenAI, avait dû abandonner les modèles fermés — **Claude Fable 5 nommément** — dont les classificateurs refusaient de distinguer un défenseur d'un attaquant, pour basculer sur GLM 5.2, modèle à poids ouverts chinois auto-hébergé.

Ce refus n'était pas une anomalie. C'était le comportement nominal du classificateur élargi qu'Anthropic avait délibérément installé au redéploiement du 1er juillet, en assumant explicitement davantage de faux positifs : « Users experience the safety margin as a model refusing to respond to some reasonable, non-harmful requests. »

La chaîne causale est donc complète, et elle est remarquable. Un contrôle à l'exportation en juin conduit Anthropic à durcir ses garde-fous en juillet ; ce durcissement bloque un défenseur légitime pendant un incident majeur trois semaines plus tard ; et cet épisode devient l'argument le plus concret en faveur des poids ouverts que la campagne de juillet ait produit. La contrainte de sûreté imposée à un modèle fermé a fabriqué, en trois étapes, la meilleure publicité pour les modèles ouverts. Le volet [19](../19-tricher-a-son-propre-examen/) traite cet épisode en détail.

## Le dossier adverse

**L'argument de la lettre est juste, indépendamment des intérêts qui le portent.** La segmentation par le coût est une réalité économique, pas un slogan. Un écosystème où l'on doit appeler un modèle de frontière pour classer des courriels est un écosystème qui ne passera pas à l'échelle. Que NVIDIA y gagne ne rend pas la proposition fausse.

**« Hypocrisie » est un mot trop court.** Aucun signataire ne prétend ouvrir son produit de frontière. La lettre ne demande d'ailleurs à personne d'ouvrir quoi que ce soit : elle demande de ne pas *interdire* l'ouverture. C'est une position sur la réglementation, pas un engagement d'entreprise. La contradiction serait flagrante si les signataires se présentaient en champions du logiciel libre ; ils se présentent en adversaires d'une restriction législative.

**Anthropic n'est pas isolée par idéologie mais par exposition.** C'est le seul grand laboratoire dont le modèle a été nommément visé par un contrôle à l'exportation, dont le modèle est nommément accusé d'avoir été distillé, et dont les garde-fous ont nommément bloqué un défenseur. Cela lui donne à la fois une expérience que personne d'autre n'a et un intérêt commercial direct dans l'issue du débat. Les deux à la fois, ce qui est exactement ce qui rend son témoignage précieux et suspect.

**Le silence n'a pas duré.** Anthropic a été accusée de ne pas répondre pendant trois jours ; elle a publié une position argumentée le 27. Reprocher un délai de trois jours à une entreprise qui publie ensuite un texte détaillé est un procès d'intention.

**Plusieurs éléments spectaculaires du dossier reposent sur une source unique.** La lettre des cent responsables cyber et ses signataires, la hausse de 33 % du titre Zhipu au lendemain de l'extinction de Fable 5, la fondation de l'Open Secure AI Alliance à la suite de l'incident Hugging Face : tous proviennent d'un seul article et n'ont pas été recoupés. Ils sont mentionnés ici comme rapportés, pas comme établis.

## Ce qui se joue réellement

**La question n'est pas « ouvert contre fermé » mais « qui décide de la capacité ».** Les trois camps s'accordent sur davantage qu'ils ne l'admettent : personne ne demande la publication des poids de frontière, personne ne demande leur interdiction complète. Le désaccord réel porte sur le seuil de capacité au-delà duquel une autorité peut intervenir, et sur l'identité de cette autorité. L'épisode de juin montre ce qui arrive quand cette question n'est pas réglée : une directive arrive à 17 h 21 sans motivation technique, et un modèle disparaît de la planète.

**L'ouverture comme principe se distingue de l'ouverture comme tactique par un seul test :** est-on encore favorable à l'ouverture quand on est devant ? Le volet [17](../17-xi-jinping-ai-geopolitics/) applique ce test à la Chine, où la réponse est en train de s'écrire dans des projets de restriction à l'export des meilleurs modèles. Le même test s'applique ici : les cent trente-trois signataires plaident pour l'ouverture d'une couche dont aucun ne dépend. Le jour où l'un d'eux publiera les poids du modèle qui constitue son revenu, l'argument changera de nature.

**Le pilier le plus solide d'Amodei est aussi le moins discuté.** Les tests obligatoires pour tous les modèles suffisamment capables, ouverts et fermés, indépendamment du pays d'origine, est la seule proposition du débat qui ne favorise structurellement personne. C'est probablement pour cela qu'elle intéresse si peu.

## Ce qui reste

Le mot d'hypocrisie ne décrit pas exactement la situation, et c'est dommage parce qu'il serait commode. Ce qui se passe est plus banal et plus instructif : cent trente-trois entreprises ont découvert qu'elles avaient un intérêt convergent à ce qu'une couche précise de la pile technologique soit gratuite — précisément la couche où aucune d'elles ne gagne d'argent. Elles ont raison sur le fond, et elles n'ont aucun mérite à avoir raison.

L'entreprise qui n'a pas signé est celle dont le produit de frontière est le plus directement en jeu, et elle défend une position qui protège son commerce. Elle a également été, six semaines plus tôt, la seule victime documentée du type d'intervention étatique arbitraire contre laquelle la lettre met en garde — et elle a choisi de ne pas le dire, parce que le dire l'aurait obligée à préciser qui, dans son propre régime de tests obligatoires, tient le stylo.

*Dans la continuité des volets [15](../15-ideologies-silicon-valley/), [17](../17-xi-jinping-ai-geopolitics/) et [19](../19-tricher-a-son-propre-examen/).*

---

## Sources

Primaires :

- [« Open Weights and American AI Leadership », 24 juillet 2026, PDF hébergé par Microsoft](https://www.microsoft.com/en-us/corporate-responsibility/wp-content/uploads/2026/07/open-weight-models-letter-1.pdf) — [page et liste vivante des signataires](https://www.microsoft.com/en-us/corporate-responsibility/topics/open-weight/).
- [Dario Amodei, « Our position on open-weights models », Anthropic, 27 juillet 2026](https://www.anthropic.com/news/position-open-weights-models).
- [Anthropic, « Statement on the US government directive to suspend access to Fable 5 and Mythos 5 », 12 juin 2026](https://www.anthropic.com/news/fable-mythos-access).
- [Anthropic, « Redeploying Claude Fable 5 », 30 juin 2026 (mis à jour le 1er juillet)](https://www.anthropic.com/news/redeploying-fable-5).
- [Communiqué du représentant Ted W. Lieu sur l'AI Kill Switch Act, 23 juillet 2026](https://lieu.house.gov/media-center/press-releases/reps-lieu-and-moran-introduce-bill-require-kill-switch-ai-systems-can).

Presse :

- [The Next Web (Ana Maria Constantin), « Anthropic won't defend open weights. In June it made the same argument for itself. », 27 juillet 2026](https://thenextweb.com/news/anthropic-open-weights-letter-holdout-fable-5-shutdown) — l'article qui établit le parallèle.
- [Axios, « OpenAI and Anthropic unite against open-weight AI risks », 22 juillet 2026](https://www.axios.com/2026/07/22/openai-anthropic-open-models-trump-china).
- [TechCrunch, « Treasury threatens sanctions after White House claims Moonshot distilled Anthropic's Fable », 22 juillet 2026](https://techcrunch.com/2026/07/22/treasury-threatens-sanctions-after-white-house-claims-moonshot-distilled-anthropics-fable/).
- [TechCrunch, « Experts say exploiting Anthropic's Fable isn't how Kimi K3 got so good », 23 juillet 2026](https://techcrunch.com/2026/07/23/experts-say-exploiting-anthropics-fable-isnt-how-kimi-k3-got-so-good/).
- [Business Insider (Tom Carter), « Anthropic Is Getting Heat for Staying Silent on Open Source AI », 27 juillet 2026](https://www.businessinsider.com/anthropic-open-source-ai-model-weights-criticism-2026-7).
- [CNBC (Ashley Capoot), « Anthropic CEO Dario Amodei isn't advocating open-weight model ban », 27 juillet 2026](https://www.cnbc.com/2026/07/27/anthropic-ceo-dario-amodei-isnt-advocating-open-weight-model-ban.html).
- [Yahoo Tech / Tom's Hardware, sur la lettre et le premier post de Jensen Huang, 24 juillet 2026](https://tech.yahoo.com/ai/articles/nvidia-24-other-companies-sign-183148703.html).
- [CNBC, « Chinese AI model used to analyse OpenAI cyber attack », 24 juillet 2026](https://www.cnbc.com/2026/07/24/chinese-ai-model-openai-cyber-attack.html).

L'expression « no undo button », largement attribuée à Dario Amodei, est une formule de presse : son énoncé réel est « once weights are released they cannot be withdrawn ». Une citation plus longue sur la perte de la capacité à révoquer l'accès et à publier des correctifs, mise entre guillemets par au moins un média, n'a pas de source identifiable et n'est pas reprise ici. Le texte du premier message de Jensen Huang sur X provient d'un index de recherche et non d'une lecture directe. La lettre des responsables de cybersécurité demandant l'annulation de la directive de juin, la hausse de 33 % du titre Zhipu, et le rôle de l'incident Hugging Face dans la fondation de l'Open Secure AI Alliance reposent sur une source unique et ne sont pas établis. Le décompte de 133 signataires est un relevé effectué le 28 juillet 2026 sur la page de Microsoft ; cette liste est vivante et continue d'évoluer.

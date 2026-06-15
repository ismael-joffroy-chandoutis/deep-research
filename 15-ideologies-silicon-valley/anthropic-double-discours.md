# Anthropic : le double discours — anatomie d'une contradiction à 965 milliards

> Rapport de recherche documenté. Rédigé le 5 juin 2026. Sources en fin de document.
> Volet 20 : le cas le plus pur de la thèse du dossier. La même semaine (1er-5 juin 2026), Anthropic dépose confidentiellement son IPO à ~965 Md$ de valorisation ET publie un appel à préserver « l'option » d'une pause mondiale de l'IA. Ce volet documente les deux discours, leur chronologie, et les grilles d'interprétation concurrentes. Prolonge le volet 18 (portrait d'Amodei) et le volet 11 (capture réglementaire).
> Claims-clés vérifiés par contre-recherche adversariale (17/17 confirmés, voir notes de méthode en fin).

> ⚠️ **Note de conflit d'intérêt, maximale.** Ce volet est rédigé par Claude, le produit d'Anthropic, **sur Anthropic**. C'est le cas limite absolu de la série : l'analyste est fabriqué par l'analysé. Le biais peut jouer dans les deux sens (minimisation par intérêt, ou surenchère critique par zèle démonstratif). Garde-fous appliqués : recherche déléguée à des agents avec vérification adversariale, citations sourcées, faits distingués des interprétations, et inclusion systématique des éléments favorables ET défavorables. À pondérer en conséquence.

---

## Sommaire
1. [La semaine du 1er au 5 juin 2026 : les deux discours en 96 heures](#1-la-semaine-du-1er-au-5-juin-2026--les-deux-discours-en-96-heures)
2. [Claude Mythos : réel, pas une rumeur](#2-claude-mythos--réel-pas-une-rumeur)
3. [Chronologie du double discours (2021-2026)](#3-chronologie-du-double-discours-2021-2026)
4. [Les actes : ce qu'Anthropic fait pendant qu'elle alerte](#4-les-actes--ce-quanthropic-fait-pendant-quelle-alerte)
5. [Le lobbying : capture réglementaire ou seul adulte dans la pièce ?](#5-le-lobbying--capture-réglementaire-ou-seul-adulte-dans-la-pièce-)
6. [Vraiment différent d'OpenAI ?](#6-vraiment-différent-dopenai-)
7. [Les grilles d'interprétation : hypocrisie, marketing, ou piège structurel](#7-les-grilles-dinterprétation--hypocrisie-marketing-ou-piège-structurel)
8. [Verdict sur les deux axes](#8-verdict-sur-les-deux-axes)
9. [Sources](#9-sources)

---

## 1. La semaine du 1er au 5 juin 2026 : les deux discours en 96 heures

La séquence, jour par jour :

| Date | Événement |
|---|---|
| **28 mai** | Série H : **65 Md$ levés, valorisation post-money ~965 Md$**, Anthropic dépasse OpenAI (852 Md$) en valeur privée. Sortie de Claude Opus 4.8 le même jour. |
| **1er juin** | **Dépôt confidentiel d'un S-1 à la SEC** (IPO visée dès octobre 2026, cabinet Wilson Sonsini, celui de l'IPO Google 2004). Run-rate ~47 Md$ (vs ~9 Md$ fin 2025). |
| **2 juin** | Extension de **Project Glasswing** (distribution du modèle cyber Claude Mythos) à ~150 nouvelles organisations dans 15+ pays. |
| **4 juin** | L'Anthropic Institute publie **« When AI Builds Itself »** (Marina Favaro & Jack Clark) : appel à ce que le monde ait « l'option » de ralentir ou suspendre temporairement le développement de l'IA de frontière. |
| **5 juin** | Vague de presse (CNN, Fortune, CNBC, SiliconANGLE) soulignant la contradiction de timing. Jack Clark à Anderson Cooper : « When I look down at the car we're driving, all I have is a gas pedal. I don't have a brake pedal. » |

**Ce que dit réellement l'appel du 4 juin**, la formulation populaire « Anthropic veut tout pauser » est inexacte. Le texte exact : « We believe it would be good for the world to have the **option** to slow or temporarily pause frontier AI development ». Et la condition : « If such systems existed, we expect that we would slow down or temporarily pause, **if other developers at or near the frontier also did so in a verifiable manner** » (plusieurs labos, plusieurs pays, USA et Chine inclus, vérification). C'est un appel à une pause *optionnelle, conditionnelle, collective et future*, pas une décision, pas un engagement unilatéral, et pas une pause de leurs propres produits.

**L'argument central du texte** : la « recursive self-improvement » (une IA « capable of fully autonomously designing and developing its own successor »). Donnée interne avancée à l'appui : **en mai 2026, plus de 80 % du code mergé dans la codebase d'Anthropic était écrit par Claude** (contre quelques % avant Claude Code, février 2025). « The evidence suggests that the human role is narrowing at each step in the AI development process. » Jack Clark (BBC Newsnight) : 100 % du code écrit par l'IA est « possible within two years ».

**L'honnêteté du texte, à créditer** : Anthropic auto-relativise ses propres chiffres (« We are not there yet, and recursive self-improvement is not inevitable » ; le « 8x » de productivité est « almost certainly an overstatement »). Le texte qui alerte sur l'accélération est aussi celui qui la *vend*, c'est la contradiction interne la plus solide et la plus sourçable : un document unique qui fait simultanément la démonstration commerciale (80 % du code) et l'alerte existentielle.

**Les réactions** : Holger Mueller (Constellation Research) : « Is it trying to freeze the status quo so it can catch up, or simply retain its lead? A freeze would certainly help Anthropic to maintain its leading position in B2B AI systems. » Rob Enderle : le billet est « more about strategic marketing than any concrete initiative to actually rein in AI developers ». Fortune : « The timing is raising some eyebrows. Just last week, the AI company filed confidential paperwork to prepare for an IPO. »

> ⚠️ **Piège documentaire identifié** : le post EA Forum « Anthropic's Pause is the Most Expensive Alarm in Corporate History » est une **fiction satirique de poisson d'avril** (taguée comme telle, écrite avec l'aide de « Claude Opus 4.6 »). Tout y est inventé : la pause effective du training, le gel du trading secondaire, l'IPO « suspendue », les « 800 Md$ évaporés ». Plusieurs résumés automatiques mélangent cette fiction avec les faits réels. Anthropic n'a **pas** pausé son entraînement.

## 2. Claude Mythos : réel, pas une rumeur

- **Claude Mythos existe** : modèle de frontière spécialisé cybersécurité, révélé par une fuite CMS accidentelle le 27 mars 2026, annoncé officiellement le **7 avril 2026** (red.anthropic.com). Capacité revendiquée : identification de milliers de vulnérabilités zero-day « in every major operating system and every major web browser » (revendication montée à « 10 000+ high/critical », chiffres auto-rapportés ; seul décompte indépendant : Cloudflare, ~2 000 bugs dont ~400 critiques). Cas vérifié : **Mythos a trouvé 271 des 423 failles Firefox corrigées par Mozilla en avril 2026**, 3 CVE explicitement créditées à Claude.
- **Distribution restreinte, pas commerciale** : « We do not plan to make Mythos Preview generally available. » Accès via **Project Glasswing** : infrastructures critiques (énergie, eau, santé, télécoms), étendu le 2 juin 2026 à ~150 organisations dans 15+ pays (dont France, Allemagne, Japon, Inde, Corée).
- **La lecture stratégique** : le sondage interne de mars 2026 (130 employés, uplift médian « 4x ») portait sur **Mythos Preview**, pas sur l'Opus commercial, Anthropic garde donc son modèle le plus puissant hors marché, le distribue comme un instrument de sécurité quasi-étatique, et utilise ses chiffres internes comme preuve d'accélération dans son appel à la pause. Selon le calendrier : fuite (27 mars) → annonce (7 avril) → extension internationale (2 juin, lendemain du dépôt IPO) → appel à la pause (4 juin). Un analyste (aibusinessreview, source secondaire à manier avec prudence) y voit une structure « heads I win, tails I win » : si Mythos est aussi dangereux qu'annoncé, sa fuite était une négligence ; sinon, la caractérisation du risque était exagérée.
- ⚠️ **Frontière étanche à maintenir** : la fiction satirique d'avril mentionne aussi un « Mythos » qui « défie sa constitution », c'est inventé. Le Mythos réel est un outil de détection de vulnérabilités, pas un modèle « rebelle ».

## 3. Chronologie du double discours (2021-2026)

La contradiction n'est pas un accident de juin 2026 : c'est une structure quinquennale.

| Date | Discours « prudence » | Acte « course » |
|---|---|---|
| Jan. 2021 | Fondation : scission d'OpenAI par 7 dissidents « safety » (« research first, deploy carefully ») | Fondation d'un concurrent frontière de plus |
| Mars 2023 | « Core Views » : « We haven't yet developed a solid understanding of how to ensure that these powerful systems are robustly aligned with human values » | Justification doctrinale du paradoxe : il *faut* construire la chose dangereuse pour l'étudier |
| Mars 2023 |, | **Non-signature de la lettre FLI** (pause de 6 mois) |
| Juil. 2023 | Témoignage Sénat (avec Bengio, Russell) : risque bioarmes « medium-term », « l'action privée ne suffit pas » |, |
| Sept. 2023 | **RSP v1** : première politique de scaling responsable du secteur, engagement de ne jamais entraîner sans garanties préalables |, |
| Oct. 2024 |, | « Machines of Loving Grace » : « dominance occidentale », « isoler nos pires adversaires » |
| Nov. 2024 |, | **Palantir + AWS** : Claude vendu défense/renseignement (IL6) |
| Mai 2025 | ASL-3 déclenché pour Opus 4 (précaution bioarmes) ; Amodei : 50 % des emplois débutants menacés, « duty and obligation to be honest » | Claude 4 + Claude Code lancés le même mois ; la prédiction de chômage est faite le jour de « Code with Claude » |
| Juin 2025 | Op-ed NYT contre le moratoire fédéral (« far too blunt ») | **Claude Gov** : modèles défense qui « refusent moins » |
| Juil. 2025 |, | **Mémo Slack fuité** : « No bad person should ever benefit from our success » est « a pretty difficult principle to run a business on » ; le Golfe = « easily $100B or more » ; la presse est « always looking for hypocrisy, while also being very stupid » |
| Sept. 2025 | Amodei au sommet Axios : « **25 % de chances que ça tourne vraiment, vraiment mal** » (« I really hate that term [p(doom)] ») | Le même homme dirige l'entreprise qui accélère le plus |
| Oct. 2025 | Jack Clark, « Technological Optimism and Appropriate Fear » : « The pile of clothes on the chair is beginning to move » | Riposte de David Sacks (Maison-Blanche) : « sophisticated regulatory capture strategy based on fear-mongering » |
| Déc. 2025 | FLI AI Safety Index : Anthropic 1re du secteur (C+)… | …mais **D en « existential safety »** ; bascule vers l'entraînement par défaut sur les données utilisateurs |
| Jan. 2026 | « The Adolescence of Technology » (Amodei, ~20 000 mots) : « Humanity is about to be handed almost unimaginable power » + critique du doomerisme « quasi-religieux » | 17 jours plus tard : Série G, 30 Md$, valorisation 380 Md$ (avec MGX d'Abu Dhabi co-lead, QIA rapportée) |
| **Fév. 2026** |, | **RSP v3.0 : abandon de l'engagement-phare** (ne jamais entraîner sans garanties préalables). Kaplan : des engagements unilatéraux n'ont pas de sens « if competitors are blazing ahead » ; s'arrêter seul « wouldn't actually help anyone » |
| Fév. 2026 | Démission publique de **Mrinank Sharma** (Safeguards Research) : « a drift, between what frontier AI labs say they value and what they actually do under pressure » | Ultimatum Hegseth, rupture Pentagone, désignation « supply-chain risk » (voir volet 17) |
| Mai 2026 |, | Série H, 965 Md$ ; location de Colossus 1 (xAI) ; premier trimestre profitable projeté |
| **Juin 2026** | **« When AI Builds Itself »** : préserver l'option d'une pause mondiale | **Dépôt IPO** trois jours avant |

**La ligne de crête de février 2026 est le fait le plus dur du dossier** : Anthropic a supprimé son engagement de pause *unilatéral et auto-contraignant* (RSP v3.0, 25 février), puis a appelé quatre mois plus tard à une pause *collective et conditionnelle* (4 juin). Le déplacement est cohérent avec sa doctrine (on ne s'arrête pas seul) mais il transforme la pause d'une obligation qu'Anthropic s'imposait en une option que le monde devrait s'accorder. TIME a qualifié le premier mouvement d'« abandon de la flagship safety pledge ».

## 4. Les actes : ce qu'Anthropic fait pendant qu'elle alerte

**La fusée financière** : Série F 183 Md$ (mi-2025) → Série G 30 Md$ à 380 Md$ (12 fév. 2026, menée par GIC et Coatue, avec Founders Fund et **MGX, Abu Dhabi** ; QIA rapportée mais non confirmée au communiqué officiel) → Série H 65 Md$ à **965 Md$** (28 mai 2026) → S-1 confidentiel (1er juin). Run-rate : 4 Md$ (juil. 2025) → 14 Md$ (fév. 2026) → ~47 Md$ (mai 2026). Premier trimestre profitable projeté au Q2 2026 (559 M$ d'opérationnel), avec le caveat des critiques (Ed Zitron) : profit possiblement gonflé par le tarif « rampe » du contrat SpaceX, et Anthropic elle-même prévient que ça ne tiendra pas.

**Le mémo du Golfe (juillet 2025)** : le document interne fuité est la pièce la plus crue du dossier. Amodei y écrit, à propos d'accepter l'argent des pétromonarchies qu'il avait publiquement écarté : « There is a truly giant amount of capital in the Middle East, easily $100B or more. If we want to stay on the frontier, we gain a very large benefit from having access to this capital » ; « This is a real downside and I'm not thrilled about it » ; et le risque d'une « race to the bottom where companies gain a lot of advantage by getting deeper and deeper in bed with the Middle East ». Sept mois plus tard, MGX co-menait la Série G. L'auteur de « Machines of Loving Grace » (« AI-powered authoritarianism seems too terrible to contemplate ») a documenté lui-même son propre arbitrage.

**Le compute (le paradoxe physique)** : jusqu'à 1 million de TPU Google (>1 GW en 2026, +3,5 GW via Broadcom dès 2027) ; Project Rainier Amazon (~500 000 Trainium2, engagement >100 Md$ sur 10 ans, jusqu'à 5 GW) ; et depuis le 6 mai 2026, **location exclusive de Colossus 1 à Memphis**, les 220 000+ GPU construits par Musk pour Grok, avec leurs turbines à gaz contestées (volet 16), louées ~15 Md$/an selon le S-1 de SpaceX (chiffrage discuté). Le lab qui demande une pédale de frein achète plus de moteur que quiconque. Des analystes pointent la circularité (Amazon investit dans Anthropic qui achète du compute Amazon, voir le volet NVIDIA à venir).

**La défense** : Palantir/AWS (nov. 2024), Claude Gov (juin 2025), contrat DoD (juil. 2025), puis la rupture sur deux lignes rouges (surveillance de masse, armes autonomes), l'ultimatum Hegseth, la désignation « supply-chain risk » (27 fév. 2026), l'injonction de la juge Rita Lin (26 mars : « classic illegal First Amendment retaliation », « Orwellian notion ») , l'appel toujours pendant au 5 juin 2026. Nuance : le DoD a continué d'utiliser Claude pour des opérations (Iran) pendant le litige. Statut net : ni victoire ni capitulation, Anthropic est le seul lab à avoir des lignes rouges qui lui ont coûté un contrat de 200 M$ et une désignation d'ennemi intérieur.

**L'emploi** : mai 2025, Amodei prédit l'élimination de ~50 % des emplois de bureau débutants (chômage jusqu'à 20 %), le jour même du lancement de Claude 4. Mai 2026 : il adoucit, invoque le paradoxe de Jevons aux côtés de Jamie Dimon (« If you automate 90% of the job, then everyone does the 10%... and kind of 10xs their productivity »). L'alerte s'est faite argumentaire.

## 5. Le lobbying : capture réglementaire ou seul adulte dans la pièce ?

Les faits, qui nourrissent les deux lectures :

- **SB 1047 (Californie, 2024)** : Anthropic a d'abord obtenu l'affaiblissement du texte (retrait du pouvoir du procureur général de poursuivre *avant* catastrophe, standard abaissé de « reasonable assurance » à « reasonable care », suppression de l'agence dédiée, amendements du 15 août reprenant ses demandes), puis l'a soutenu du bout des lèvres (« benefits likely outweigh its costs. However, we are not certain of this »). Newsom a mis son veto. Anthropic a été le seul grand lab à rompre le front du refus, mais après avoir limé les dents du texte.
- **SB 53 (2025)** : Anthropic est le **seul grand lab à avoir endossé** le Transparency in Frontier AI Act (8 sept. 2025), signé par Newsom le 29 sept. Argument d'Anthropic : « Without it, labs with increasingly powerful models could face growing incentives to dial back their own safety and disclosure programs in order to compete. » Critique (Dossier, « The Federal AI Moat ») : le texte formalise les pratiques internes d'Anthropic en standard légal, un fossé réglementaire au seuil de 500 M$ de CA qui épargne les startups mais s'imposera aux challengers.
- **Anti-préemption constante** : op-ed NYT contre le moratoire de 10 ans (juin 2025, « far too blunt »), opposition à l'EO de préemption de décembre 2025, **20 M$ donnés à Public First Action** (12 fév. 2026), le 501(c)(4) pro-régulation, pendant qu'OpenAI (Brockman), a16z et Lonsdale financent **Leading the Future** (>125 M$, pro-dérégulation). Anthropic ne finance pas Leading the Future. Zone grise réelle : Public First Action a engendré des super PACs qui dépensent en primaires fédérales, et Anthropic affirme que ses dons « weren't intended for federal election spending », la plomberie reste opaque.
- **Lobbying fédéral** : 280 k$ (2023) → 720 k$ (2024) → ~3,13 M$ (2025, à reconfirmer sur OpenSecrets). En face, les accusateurs : Sacks (« principally responsible for the state regulatory frenzy », « backdoor Woke AI »), LeCun (« You're being played by people who want regulatory capture »), Gary Marcus (entrenchment des incumbents). Et la défense d'Amodei (21 oct. 2025) : « There are products we will not build and risks we will not take, even if they would make money » ; « Startups are among our most important customers. »
- **Export controls** : la position la plus dure du secteur (« It is mortgaging our future as a country to sell these chips to China », « selling nuclear weapons to North Korea »), sincèrement géopolitique ET objectivement défavorable à NVIDIA, son non-allié (volet à venir).

## 6. Vraiment différent d'OpenAI ?

La question mérite une réponse en deux colonnes plutôt qu'un verdict.

**Ce qui est structurellement identique** : la course à la frontière (cadence de release bimensuelle, ~74 releases en 52 jours début 2026, décompte indicatif) ; les méga-levées et l'IPO (965 vs 852 Md$, S-1 confidentiels à quelques mois d'écart) ; l'argent du Golfe (MGX chez les deux) ; le lobbying à millions ; les deals défense ; la justification par l'inévitabilité (« si ce n'est pas nous, ce sera pire ») ; la métaphysique AGI partagée qui gonfle les valorisations (volet 14, volet 18). Karen Hao (*Empire of AI*) range les deux dans la même logique impériale « ends-justify-the-means », tout en traitant Anthropic, notent ses recenseurs, comme un contrepoint plus sincère qu'OpenAI.

**Ce qui diffère, factuellement** : (1) les deux **lignes rouges défense** maintenues au prix d'un contrat de 200 M$ et d'une guerre juridique avec le Pentagone, OpenAI n'a pas d'équivalent documenté ; (2) l'**endossement de SB 53** vs la non-position d'OpenAI ; (3) **Public First Action vs Leading the Future**, les deux labs financent des camps politiques opposés sur la régulation ; (4) la structure **PBC + Long-Term Benefit Trust** (Class T, trustees sans equity, montée vers la majorité du board) vs la conversion for-profit d'OpenAI, en notant que le LTBT a des clauses « failsafe » actionnables par supermajorité d'actionnaires, que son Trust Agreement n'est pas public, et que sa résilience post-IPO n'a jamais été testée ; (5) une transparence relative réelle (publication de l'alignment faking, des system cards détaillées, auto-caveats) que le FLI Index récompense d'un C+… assorti d'un D en existential safety, comme tout le monde ; (6) le refus de la publicité dans Claude (« Ads are coming to AI. But not to Claude », Super Bowl 2026) et un revenu assis sur l'enterprise plutôt que le consumer.

**La synthèse honnête** : la différence existe, elle est coûteuse, et elle est réelle, mais elle opère *à l'intérieur* de la course, jamais contre elle. Anthropic est différente d'OpenAI exactement dans la mesure où cette différence est compatible avec 965 Md$ de valorisation. Le test de février 2026 (RSP v3.0) a montré où passe la limite : quand l'engagement de sécurité entre en conflit avec la position concurrentielle, c'est l'engagement qui cède. Jared Kaplan l'a dit sans détour : des engagements unilatéraux n'ont pas de sens « if competitors are blazing ahead ». La différence d'Anthropic est une différence de *conduite dans la course*, pas une différence sur le fait de courir.

## 7. Les grilles d'interprétation : hypocrisie, marketing, ou piège structurel

Quatre lectures concurrentes, à tenir ensemble :

1. **La capture réglementaire** (Sacks, a16z, Groq) : la peur comme stratégie de fossé concurrentiel, les standards de safety d'Anthropic devenant loi, les challengers paient le coût de conformité. Force : SB 1047 affaibli *puis* soutenu, SB 53 calqué sur ses pratiques, le carve-out à 500 M$. Faiblesse : la position export controls et les lignes rouges Pentagone ont *coûté* à Anthropic, ce qu'une pure stratégie de capture ne fait pas.
2. **Le doom comme sales pitch** (Meyboom, The New Republic) : « This technology is the most consequential in human history » fonctionne comme « both a caution and an investor's dream » ; « We are the responsible ones » = « both a moral claim and a competitive moat ». Le timing essai-levée (« The Adolescence of Technology » → 17 jours → 30 Md$) est réel. Contre-argument sérieux : la peur serait plus vendable si le risque semblait lointain ; dire « deux ans » rend le problème plus dur à financer, pas plus facile.
3. **Le piège structurel** (Karnofsky lui-même, via Torres) : « the AGI race isn't a coordination failure », si Anthropic se retirait, les autres diraient « This is awesome » et ralentiraient à peine. Donc rester est rationnel. Meyboom : « Rational self-interest, aggregated across all players, produces a collectively irrational and potentially catastrophic outcome. » Ce n'est pas de l'hypocrisie, c'est pire : chaque acteur est sincère et le système produit quand même la course. Torres retourne l'argument : « the race itself is causing profound harms », la rationalité individuelle n'excuse pas la participation.
4. **L'auto-sabotage épistémique** (Anton Leicht, « Anthropic Against Itself ») : la grille la plus fine. En étant à la fois labo, lobbyiste et lanceur d'alerte, Anthropic dégrade la crédibilité de ses propres signaux : « your empirical outputs become less credible when linked to a policy agenda ». Pour percer, un warning shot doit être « ironclad », or « empirical findings of a political player are neither ». Cercle vicieux : le scepticisme « incentivizes Anthropic to put out even more alarming findings ». Quand la vraie alerte viendra, qui croira l'entreprise qui crie au loup avec un prospectus d'IPO dans l'autre main ?

S'y ajoute la comparaison historique qu'Amodei manie lui-même : ne pas finir comme « the cigarette companies, or the opioid companies, where they knew there were dangers, and they didn't talk about them » (60 Minutes, nov. 2025). La différence revendiquée : Anthropic *parle* des dangers. La question que la comparaison esquive : les cigarettiers qui auraient publié leurs études internes tout en continuant à vendre auraient-ils été moins coupables, ou seulement mieux documentés ? Et l'« Oppenheimer trap » (exemplaires de Rhodes sur les bureaux, sticker Oppenheimer sur les laptops, selon Vox) : « someone will build it; better it be those who understand the risks », une logique qui « holds until it does not ».

## 8. Verdict sur les deux axes

Sur les deux axes du dossier (1 : accélérer ↔ ralentir ; 2 : concentration ↔ démocratie) :

- **Axe 1** : Anthropic occupe les deux pôles simultanément, et c'est le fait central, le discours le plus « ralentir » du secteur (25 % de p(doom), appel à l'option de pause) porté par l'acteur qui accélère le plus (cadence record, 47 Md$ de run-rate, course au compute). La résolution de la contradiction est dans le mot « option » : Anthropic ne demande jamais de ralentir *maintenant*, toujours de pouvoir ralentir *plus tard*, *ensemble*, *si nécessaire*. La pause est repoussée dans un futur conditionnel pendant que l'accélération occupe le présent de l'indicatif.
- **Axe 2** : concentration assumée (965 Md$, fonds souverains du Golfe, IPO) avec des contre-poids internes réels mais non testés (LTBT) et une préférence documentée pour la régulation, celle qui codifie ses pratiques. Le seul acteur du dossier à financer le camp pro-régulation (20 M$) ET à avoir payé un prix politique réel (Pentagone) pour des lignes rouges.
- **La formule** : si Amodei était « le doomer qui accélère » (volet 18), Anthropic en juin 2026 est *l'institution* de cette figure, une entreprise dont le produit est l'accélération et la marque est l'inquiétude, et dont les deux discours sont sincères, simultanés, et structurellement irréconciliables. Le marché, lui, a tranché : il valorise l'ensemble, l'inquiétude comprise, à 965 milliards.

---

## 9. Sources

**L'appel du 4 juin et la semaine IPO**
- [Anthropic Institute, When AI Builds Itself](https://www.anthropic.com/institute/recursive-self-improvement) · [Fortune, pause + IPO timing](https://fortune.com/2026/06/05/anthropic-ai-pause-development-recursive-self-improvement/) · [CNN, brake pedal (Jack Clark/Anderson Cooper)](https://www.cnn.com/2026/06/05/business/anthropic-calls-for-ai-brake-pedal) · [SiliconANGLE, analyse critique](https://siliconangle.com/2026/06/05/filing-ipo-anthropic-says-ai-slow-fat-chance/) · [CNBC, dépôt S-1](https://www.cnbc.com/2026/06/01/anthropic-ipo-s1-prospectus.html) · [Anthropic, Série H](https://www.anthropic.com/news/series-h) · [Tom's Hardware, 80 % du code](https://www.tomshardware.com/tech-industry/artificial-intelligence/anthropic-says-claude-now-writes-more-than-80-percent-of-its-merged-code)
- ⚠️ Fiction satirique à NE PAS citer comme fait : [EA Forum, April Fools](https://forum.effectivealtruism.org/posts/KTgC6ggEmbGcKa9es/)

**Claude Mythos / Project Glasswing**
- [red.anthropic.com, Mythos Preview](https://red.anthropic.com/2026/mythos-preview/) · [TechCrunch, extension 15 pays](https://techcrunch.com/2026/06/02/anthropic-scales-claude-mythos-to-critical-infrastructure-in-15-countries/) · [TechRadar, 271/423 failles Firefox](https://www.techradar.com/) 

**RSP et son abandon**
- [Anthropic, RSP](https://www.anthropic.com/news/anthropics-responsible-scaling-policy) · [TIME, drops flagship safety pledge](https://time.com/7380854/exclusive-anthropic-drops-flagship-safety-pledge/) · [CNN, RSP v3.0](https://www.cnn.com/2026/02/25/tech/anthropic-safety-policy-change) · [Semafor, démission Sharma](https://www.semafor.com/article/02/11/2026/anthropic-safety-researcher-quits-warning-world-is-in-peril)

**Business, Golfe, compute, défense**
- [Anthropic, Série G](https://www.anthropic.com/news/anthropic-raises-30-billion-series-g-funding-380-billion-post-money-valuation) · [Futurism/Wired, mémo Slack Golfe](https://futurism.com/leaked-messages-ceo-anthropic-dictators) · [CNBC, Google TPU](https://www.cnbc.com/2025/10/23/anthropic-google-cloud-deal-tpu.html) · [AWS, Project Rainier](https://www.aboutamazon.com/news/aws/aws-project-rainier-ai-trainium-chips-compute-cluster) · [Daily Memphian, Colossus 1](https://dailymemphian.com/subscriber/article/63148/anthropic-claude-memphis-spacex-xai-data-center-colossus) · [Tech Policy Press, timeline Pentagone](https://www.techpolicy.press/a-timeline-of-the-anthropic-pentagon-dispute/) · [CNN, injonction Lin](https://edition.cnn.com/2026/03/26/business/anthropic-pentagon-injunction-supply-chain-risk) · [CBS 60 Minutes, tabac/opioïdes](https://www.cbsnews.com/news/anthropic-ai-safety-transparency-60-minutes/) · [Axios, 25 % p(doom)](https://www.axios.com/2025/09/17/anthropic-dario-amodei-p-doom-25-percent) · [Fortune, Jevons](https://fortune.com/2026/05/05/dario-amodei-jevons-paradox-will-ai-wipe-out-white-collar-jobs/)

**Lobbying et politique**
- [TechCrunch, SB 1047 affaibli](https://techcrunch.com/2024/08/15/california-weakens-bill-to-prevent-ai-disasters-before-final-vote-taking-advice-from-anthropic/) · [Anthropic, endossement SB 53](https://www.anthropic.com/news/anthropic-is-endorsing-sb-53) · [Anthropic, don Public First Action](https://www.anthropic.com/news/donate-public-first-action) · [Axios, Leading the Future](https://www.axios.com/2026/01/30/openai-a16z-cash-ai-super-pac) · [TechCrunch, Amodei répond à Sacks](https://techcrunch.com/2025/10/21/anthropic-ceo-claps-back-after-trump-officials-accuse-firm-of-ai-fear-mongering/) · [Dossier, The Federal AI Moat](https://www.dossier.today/p/the-federal-ai-moat-anthropic-is)

**Grilles d'interprétation**
- [The New Republic, Doomsaying as Sales Pitch (Meyboom)](https://newrepublic.com/article/210169/anthropic-ai-warnings-sales-pitch) · [Anton Leicht, Anthropic Against Itself](https://writing.antonleicht.me/p/anthropic-against-itself) · [Steven Adler, Don't rely on a race to the top](https://www.clear-eyed.ai/p/dont-rely-on-a-race-to-the-top) · [Torres, Karnofsky et la course](https://www.realtimetechpocalypse.com/p/marc-andreessen-doesnt-introspect) · [FLI, AI Safety Index Winter 2025](https://futureoflife.org/ai-safety-index-winter-2025/) · [Harvard Corp Gov, LTBT](https://corpgov.law.harvard.edu/2023/10/28/anthropic-long-term-benefit-trust/) · [AI Lab Watch, certificate of incorporation](https://ailabwatch.substack.com/p/anthropics-certificate-of-incorporation) · [Jack Clark, Technological Optimism and Appropriate Fear](https://jack-clark.net/2025/10/13/import-ai-431-technological-optimism-and-appropriate-fear/) · [Dario Amodei, The Adolescence of Technology](https://www.darioamodei.com/essay/the-adolescence-of-technology)

### Notes de méthode
17 claims porteurs soumis à contre-recherche adversariale : 17 confirmés, dont 3 reclassés (le « 4x » concerne Mythos Preview et non Opus ; « 271 failles » = 271 sur 423 corrigées ; run-rate 47 Md$ passé de confiance moyenne à haute). Citations non confirmées sur source primaire et donc EXCLUES du corps : « selling our souls » (jamais sourcée), « gobbledegook » (rapportée par Yudkowsky seul), essai « Technological Maturity » (inexistant). Le S-1 étant confidentiel, tous les chiffres IPO restent des rapports de presse.

### Voir aussi
[Volet 11, Camp prudence IA](./camp-prudence-bengio-bostrom-yudkowsky.md) · [Volet 14, Yudkowsky & Soares, lecture critique](./if-anyone-builds-it-lecture-critique.md) · [Volet 16, L'empire matériel](./empire-materiel-sud-global-compute.md) · [Volet 17, Le pont natsec](./pont-natsec-doomers-faucons.md) · [Volet 18, Les maîtres de modèles](./maitres-de-modeles-portraits-2.md)

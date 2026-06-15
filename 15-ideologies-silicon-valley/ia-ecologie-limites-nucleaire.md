# IA, écologie et limites planétaires — et le nucléaire : mirage ou solution ?

> Rapport de recherche documenté. Rédigé le 5 juin 2026. Sources en fin de document.
> Volet 22 : le volet 16 documentait l'extraction (eau, minerais, travail). Ce volet pose les deux questions systémiques : l'IA est-elle compatible avec les limites planétaires (Limits to Growth, Jevons, décroissance) ? Et le nucléaire, la réponse favorite des hyperscalers, est-il une solution réelle ou un récit de couverture ?
> Claims-clés vérifiés par contre-recherche adversariale (corrections intégrées, voir notes de méthode).

---

## Sommaire
1. [L'empreinte réelle : les chiffres 2026](#1-lempreinte-réelle--les-chiffres-2026)
2. [Le retour de Limits to Growth](#2-le-retour-de-limits-to-growth)
3. [Jevons : le paradoxe revendiqué par les hyperscalers eux-mêmes](#3-jevons--le-paradoxe-revendiqué-par-les-hyperscalers-eux-mêmes)
4. [Le bilan « IA pour le climat » : 74 % d'affirmations non prouvées](#4-le-bilan--ia-pour-le-climat---74--daffirmations-non-prouvées)
5. [Le nucléaire : l'inventaire 2026, deal par deal](#5-le-nucléaire--linventaire-2026-deal-par-deal)
6. [Le verdict nucléaire : ni mirage ni solution, un alibi temporel](#6-le-verdict-nucléaire--ni-mirage-ni-solution-un-alibi-temporel)
7. [Décroissance, sobriété, moratoires : la contre-position](#7-décroissance-sobriété-moratoires--la-contre-position)
8. [Sources](#8-sources)

---

## 1. L'empreinte réelle : les chiffres 2026

- **Électricité** : datacenters ≈ 415 TWh (2024) → ~485 TWh (2025) → **~945-950 TWh projetés en 2030** (~3 % de la demande mondiale), selon l'IEA (« Energy and AI », 2025). La demande des datacenters a crû de +17 % en 2025 ; les datacenters *IA* de **+50 %**. ⚠️ Le chiffre très cité « 1 000 TWh dès 2026 » vient du rapport IEA de janvier 2024 (incluant la crypto) ; les éditions ultérieures repoussent ce seuil vers 2030, citer avec la date du rapport.
- **Le mix réel** : ~60 % de l'électricité physiquement consommée par les datacenters vient des fossiles (charbon ~30 %), 27 % renouvelables, 15 % nucléaire (IEA). Le « mix contractuel » des PPA verts affiché par les hyperscalers est une comptabilité, pas une réalité physique. Signal révélateur : **+70 % de commandes de turbines à gaz en 2025**.
- **Émissions des hyperscalers** : Microsoft +23,4 % depuis 2020 (objectif « carbon negative 2030 » maintenu sur le papier ; report envisagé selon la presse, mai 2026, non confirmé) ; Google +~50 % sur cinq ans. Le tour de passe-passe comptable est documenté : en « market-based » (crédits), Google affiche -12 % ; en « **location-based** » (physique), ses émissions Scope 2 passent de 5,8 à 11,2 Mt CO₂ (2020-2024), celles de Microsoft de 4,3 à ~10 Mt. La « baisse » est un artefact de crédits carbone.
- **Eau** : ~560 milliards de litres consommés par les datacenters en 2023 (IEA) ; projection ONU (UNU/UNEP) jusqu'à 9 300 milliards de litres en 2030 si l'IA atteint 40 % de la consommation électrique des datacenters, fourchettes très larges, opacité des opérateurs (Kaveh Madani, UNU : « AI is also physical infrastructure »).
- **Matériaux et déchets** : 2-3 % de la demande mondiale de cuivre et minéraux critiques d'ici 2030, en concurrence directe avec la transition énergétique ; ~62 Mt/an d'e-waste mondial, recyclage marginal des infrastructures.
- **France** : GreenIT chiffre l'IA à 41 Mt éq. CO₂ en 2025, projection ×7 d'ici 2030, qualifiée d'« insoutenable » (confiance moyenne).

## 2. Le retour de Limits to Growth

Le rapport Meadows (1972) connaît une seconde vie scientifique directement pertinente pour l'IA :

- **Herrington (2021, Journal of Industrial Ecology)** compare le modèle World3 aux données 2000-2020 : les scénarios qui collent le mieux sont **BAU2** (ressources doublées) et **CT** (technologie globale). Or BAU2 mène quand même à l'overshoot-and-collapse, déclenché non par l'épuisement des ressources mais par la **pollution**, pic ~2040. Traduction : doubler les ressources et recycler ne change pas le mode, ça déplace la cause de l'effondrement.
- **Nebel et al. (2024)** recalibrent World3 sur les données empiriques : le scénario BAU reste celui qui dévie le moins. (⚠️ recalibration distincte, à ne pas attribuer à Herrington.)
- **L'application à l'IA** : dans la grammaire de World3, l'IA est un cas d'école de « Comprehensive Technology », la technologie qui repousse une limite (efficacité) en accélérant l'approche d'une autre (pollution, énergie, matériaux). Le scénario CT de Meadows ne s'effondre pas par manque de ressources mais par les coûts croissants de la technologie elle-même. Les 400 Md$ de capex annuels des hyperscalers (+75 % attendus en 2026) sont littéralement ce coût.

## 3. Jevons : le paradoxe revendiqué par les hyperscalers eux-mêmes

Le fait le plus remarquable de la séquence DeepSeek (janvier 2025) : confronté à un modèle 10× moins cher, le marché a paniqué un jour, puis **Satya Nadella a tweeté** : « Jevons paradox strikes again! As AI gets more efficient and accessible, we will see its use skyrocket. » Meta a relevé son capex 2025 à 60-65 Md$ (+50 %). Le paradoxe de Jevons (1865 : l'efficacité accroît la consommation totale) est passé du statut d'objection écologiste à celui d'**argument d'investissement officiel**. Amodei l'invoque sur l'emploi (volet 20), Nadella sur l'énergie, la même figure sert à promettre que rien ne ralentira jamais.

La version académique (Luccioni et al. ACM FAccT 2025) : les gains d'efficacité (loi de Koomey) sont écrasés par le volume de compute ; les effets rebond rendent les impacts « structurels et non marginaux ». C'est la jonction formelle avec Limits to Growth : l'efficacité sans plafond est un accélérateur, pas un frein. D'où la distinction française utile sobriété/efficacité : la **sobriété numérique** (Parrique et al.) interroge l'usage en amont, jusqu'au renoncement, l'« IA frugale » étant jugée contradiction intrinsèque.

## 4. Le bilan « IA pour le climat » : 74 % d'affirmations non prouvées

Les deux pièces du dossier, à tenir ensemble :

- **À charge** : le rapport du consortium Beyond Fossil Fuels (Ketan Joshi, 17 février 2026, avant le sommet de New Delhi) analyse 154 affirmations de bénéfices climatiques de l'IA : **74 % non prouvées**, 36 % sans aucune citation, et **aucun exemple** où ChatGPT/Gemini/Copilot produisent des réductions d'émissions « matérielles, vérifiables et substantielles ». Distinction structurante : les bénéfices documentés viennent de l'IA « traditionnelle » (ML ciblé, réseaux électriques, météo), les dommages de l'IA *générative*. Le greenwashing consiste précisément à confondre les deux. Greenpeace East Asia classe NVIDIA **dernier** de la supply chain IA sur la décarbonation (émissions de fabrication de puces ×4,5 en un an).
- **À décharge (conditionnelle)** : l'étude Grantham/LSE + Systemiq (*npj Climate Action*, juin 2025) : l'IA *pourrait* réduire les émissions de 3,2-5,4 Gt CO₂e/an d'ici 2035 (réseaux, alimentation, transport), davantage que la hausse de consommation des datacenters. Mais le caveat des auteurs eux-mêmes est la clé : cela exige investissement public ciblé, données partagées, accès équitable ; « sans politique active, les incitations commerciales n'orienteront pas l'IA vers les usages socialement utiles ». Et le cas d'école réel existe : **GraphCast** (DeepMind) prévoit la météo à 10 jours en <1 min sur un TPU, ~1000× moins d'énergie que la prévision numérique, IA traditionnelle, entraînée une fois, exécutée souvent.
- **La synthèse honnête** : le récit « l'IA sauvera le climat » s'appuie sur un potentiel conditionnel à 2035 (Grantham) pour couvrir un bilan observé négatif en 2026 (BFF). Les deux études ne se contredisent pas : l'une décrit ce qui serait possible avec une politique publique que personne ne mène, l'autre ce qui se passe réellement.

## 5. Le nucléaire : l'inventaire 2026, deal par deal

**Les deals (tous réels, tous lointains)** :

| Deal | Contenu | Échéance réelle |
|---|---|---|
| Microsoft / Constellation | PPA 20 ans, redémarrage Three Mile Island Unit 1 (« Crane Clean Energy Center », 835 MW). Investissement Constellation **1,6 Md$** (⚠️ le « 16 Md$ » qui circule est l'apport au PIB de Pennsylvanie, pas le deal) + prêt fédéral DOE 1 Md$ | 2027-2028 |
| Google / Kairos | Jusqu'à 500 MW de SMR (6-7 réacteurs) | Premier réacteur ~2030, flotte 2035 |
| Amazon / X-energy | 700 M$ investis, jusqu'à 12 réacteurs Xe-100 + campus Susquehanna 20 Md$ | FID Dow/Texas ~2028, déploiement 2030s |
| Meta | Le plus gros engagement : PPA 20 ans Clinton (1 121 MW, juin 2027) + Vistra/Oklo/TerraPower jusqu'à 6,6 GW | 2027 (existant) à 2035 (nouveau) |

Au printemps 2026, 13 projets engagent >9,8 GW ; Amazon, Google et Meta ont signé l'engagement de tripler la capacité nucléaire mondiale d'ici 2050.

**L'état réel des SMR** : **aucun SMR commercial occidental en service début 2026.** NuScale : seul design certifié NRC, mais projet phare (Idaho) annulé en 2023 pour coûts (~89 $/MWh), revenus réacteur pas avant les années 2030. Oklo (présidé par Sam Altman avant son passage au capital) : pipeline de 14 GW, pré-revenu. TerraPower (Gates) : Natrium repoussé 2030+, goulot transversal : la pénurie de combustible **HALEU**. X-energy : IPO avril 2026 (1,02 Md$ levés), décision finale d'investissement ~2028. LCOE des premiers exemplaires : 90-160 $/MWh, au-dessus de l'éolien/solaire. **La seule exception est chinoise** : Linglong One (ACP100, Hainan) visait l'exploitation commerciale au S1 2026, non confirmée comme connectée au réseau à la date de ce rapport. La Chine a 29 réacteurs en construction, ~la moitié du total mondial.

**La fusion** : aucune installation au monde ne produit d'électricité nette commerciale. ITER ne produira *jamais* d'électricité (pas de turbine), calendrier D-T glissé à 2039. Helion (Altman) a signé le premier PPA fusion au monde (Microsoft, 50 MW, « 2028 », avec pénalités) ; CFS/SPARC vise le net energy en 2027 et un plant en Virginie début 2030s (PPA >1 Md$ avec Eni). Analyse ETH Zurich (Nature Energy, 2026) : taux d'apprentissage trop optimistes, la fusion pourrait ne pas concurrencer solaire+batteries avant 2040. À traiter comme pari, pas comme plan.

**Les fondamentaux du débat de fond** :
- **Coût** (Lazard LCOE+ 2025, non subventionné) : éolien terrestre 37-86 $/MWh, solaire utility 38-217, gaz CCGT 48-109, **nucléaire 141-220**. Solaire/éolien les moins chers pour la 10e année consécutive.
- **Délais** (l'EPR comme avertissement) : Flamanville 3 à pleine puissance en décembre 2025, ~12 ans de retard, ~23,7 Md€ (vs 3,3 prévus). Hinkley Point C : 36-40 Md£ (vs 18). Olkiluoto-3 : 14 ans de retard. Programme EPR2 français : plafond révisé à **72,8 Md€** (+40 % vs 2022), premier béton 2029, mise en service **2038**.
- **Sûreté** (Our World in Data) : charbon ~24,6 morts/TWh, gaz ~3, **nucléaire <0,1**, comme le solaire et l'éolien. Le nucléaire tue 99,8 % moins que le charbon. Sur ce critère, le débat est tranché.
- **Déchets** : aucun dépôt géologique définitif n'a jamais ouvert dans le monde. Le premier, Onkalo (Finlande), attend sa licence d'exploitation (décision STUK ~fin juin 2026) ; Cigéo (Bure) vise une phase pilote en 2035. « Polluant éternel » est rhétoriquement vrai (confinement promis : 100 000 ans, invérifiable par construction) mais le volume est minuscule comparé aux déchets fossiles dispersés dans l'atmosphère, l'asymétrie des deux pollutions (concentrée/gérée vs diffuse/subie) est le cœur honnête du débat.
- **Uranium** : flambée début 2026 (>100 $/lb), demande +28 % d'ici 2030 ; le consensus WNA/IAEA est que la contrainte est le sous-investissement, pas la géologie (sources en partie intéressées, Sprott et al.).

## 6. Le verdict nucléaire : ni mirage ni solution, un alibi temporel

La réponse à la question posée (« mirage ? polluant éternel ou vraiment bon ? ») tient en quatre propositions documentées :

1. **Sur le fond, le nucléaire est défendable** : bas carbone, pilotable, sûr (<0,1 mort/TWh), avec une question des déchets réelle mais gérée à une échelle sans commune mesure avec les fossiles. La taxonomie verte UE l'a classé transitionnel (le veto parlementaire a échoué : 278 pour, 328 contre) et la CJUE a confirmé. Le clivage écologiste historique (Allemagne sortie en 2023... en augmentant son gaz) relève davantage de l'histoire politique que de la physique.
2. **Sur la temporalité, c'est un mismatch structurel** : la demande IA arrive en 3-5 ans, le nucléaire neuf livre en 10-15 (EPR2 : 2038 ; SMR : début 2030s au mieux ; fusion : spéculative). L'IEA est explicite : le nucléaire ne joue un rôle qu'« en fin de décennie et au-delà » ; d'ici là, renouvelables ~moitié de la demande additionnelle, puis **gaz et charbon**. MIT Tech Review : même en vantant le nucléaire, les tech « s'appuieront largement sur les fossiles, garderont des centrales charbon ouvertes, construiront du gaz qui restera des décennies ».
3. **Donc la fonction réelle des deals nucléaires en 2024-2026 est narrative** : un pipeline d'accords *conditionnels* sur une technologie non éprouvée à l'échelle (25 GW fin 2024 → 45 GW mi-2026) sert de récit de décarbonation pendant que l'expansion réelle tourne au gaz (Memphis, +70 % de turbines commandées) et au charbon (Chine). La hiérarchie de crédibilité : **redémarrages (quasi sûrs, 2027-28) > nouveau nucléaire (2030s) > SMR (paris industriels) > fusion (pari scientifique)**. Seuls les redémarrages (TMI, Clinton) sont des mégawatts probables à horizon utile.
4. **La figure synthétique** : Sam Altman préside le double pari (fission Oklo + fusion Helion), l'IA finance l'énergie qui justifiera l'IA. Fatih Birol (IEA) offre le cadrage techno-optimiste (« l'IA n'est plus seulement un preneur d'énergie, elle devient un faiseur d'énergie ») ; le clivage de gauche est documenté entre écomodernistes (Breakthrough Institute, Monbiot, Brand, « seule techno zéro-carbone pilotable démontrée ») et écosocialistes (Joshua Frank, Spectre : « fausse solution »). Position de travail pour ce dossier : le nucléaire est une bonne réponse à la mauvaise question. La question n'est pas « comment alimenter la croissance infinie du compute » mais « quel volume de compute est justifié, pour quoi », et c'est exactement la question que les deals nucléaires servent à ne pas poser.

## 7. Décroissance, sobriété, moratoires : la contre-position

- **Le corpus intellectuel** : Hickel (« exnovation » : réallouer les capacités productives), Saito (*Slow Down*, 500k+ ventes, « locking technology », l'efficacité capitaliste comme machine à surproduction), Parrique (sobriété numérique). ⚠️ Honnêteté documentaire : ni Saito ni Parrique n'ont de position publiée *spécifiquement* sur l'IA vérifiée par cette recherche, leurs cadres s'y appliquent, l'attribution directe serait abusive. Le « digital degrowth » est un corpus émergent, pas stabilisé.
- **La pratique** : c'est le terrain local qui porte la contre-position réelle, moratoire irlandais (2021, levé déc. 2025 sous conditions : génération sur site, 80 % renouvelable), restrictions néerlandaises durables (hyperscale ≥70 MW cantonnés), **Virginie** (≥25 datacenters annulés en 2025, ~4× 2024 ; Loudoun County supprime le zonage « by-right » ; 60+ projets de loi en 2026 dont un moratoire jusqu'en 2028 ; 35 % seulement des électeurs favorables aux nouveaux datacenters), Memphis (procès NAACP, volet 21). Data Center Watch : ~64-100 Md$ de projets bloqués/retardés (confiance moyenne).
- **La demande politique structurée** : la déclaration « **Within Bounds** » (130+ organisations, sommet de Paris, février 2025), infrastructure IA « fossil-free » et plafonds de ressources compatibles avec les limites planétaires. C'est la traduction politique de Meadows : non pas « mieux », mais « dans les bornes ».
- **Le point de jonction avec le reste du dossier** : l'Irlande (22 % de l'électricité nationale dans les datacenters) a fini par rouvrir sous conditions, démonstration que même les moratoires qui tiennent quatre ans cèdent à la pression du capex. Sans plafond *global* (compute cap, conditionnalité énergétique), les victoires locales déplacent les datacenters plus qu'elles ne les arrêtent. La question des solutions est traitée au volet 25.

---

## 8. Sources

**Empreinte**
- [IEA, Energy and AI](https://www.iea.org/reports/energy-and-ai/energy-demand-from-ai) · [IEA, Key Questions](https://www.iea.org/reports/key-questions-on-energy-and-ai/executive-summary) · [Computer Weekly, émissions Microsoft/Google](https://www.computerweekly.com/news/366592778/Microsoft-and-Googles-GHG-emissions-gains-call-viability-of-net-zero-targets-into-question) · [Earth.org, rapport ONU eau](https://earth.org/9-3-trillion-liters-of-water-un-report-exposes-unfathomable-footprint-of-data-centers-as-ai-booms/) · [GreenIT, impacts IA](https://www.greenit.fr/2025/10/21/quels-sont-les-impacts-environnementaux-et-sanitaires-de-l-ia/)

**Limites et Jevons**
- [Herrington 2021, Update to limits to growth](https://www.researchgate.net/publication/346635923_Update_to_limits_to_growth_Comparing_the_World3_model_with_empirical_data) · [Nebel et al. 2024, Recalibration of World3](https://onlinelibrary.wiley.com/doi/10.1111/jiec.13442) · [Luccioni et al. Jevons/FAccT 2025](https://arxiv.org/abs/2501.16548) · [AI Proem, Nadella et Jevons](https://aiproem.substack.com/p/the-jevons-paradox-in-ai-infrastructure)

**IA et climat**
- [Beyond Fossil Fuels, 74 % non prouvé](https://beyondfossilfuels.org/2026/02/17/report-exposes-big-techs-ai-climate-hoax-74-of-industrys-claims-about-ais-climate-benefits-are-unproven/) · [LSE Grantham, Green and Intelligent](https://www.lse.ac.uk/granthaminstitute/news/new-study-finds-ai-could-reduce-global-emissions-annually-by-3-2-to-5-4-billion-tonnes-of-carbon-dioxide-equivalent-by-2035/) · [DeepMind, GraphCast](https://deepmind.google/blog/graphcast-ai-model-for-faster-and-more-accurate-global-weather-forecasting/) · [Greenpeace, AI energy](https://www.greenpeace.org/international/story/82486/ai-energy-environment-democracy/) · [Within Bounds](https://beyondfossilfuels.org/2025/02/07/within-bounds-limiting-ais-environmental-impact/)

**Nucléaire**
- [Introl, deals nucléaires hyperscalers](https://introl.com/blog/nuclear-power-ai-data-centers-microsoft-google-amazon-2025) · [Constellation, Crane](https://www.constellationenergy.com) · [Utility Dive, Meta 6,6 GW](https://www.utilitydive.com/news/meta-nuclear-deal-oklo-vistra-terrapower) · [SMR Intel, pipeline](https://smrintel.com/nuclear-data-center-deals/) · [Eurasia Review, SMR expectations vs reality](https://www.eurasiareview.com/17122025-small-modular-reactors-smrs-and-nuclear-power-bridging-expectations-and-reality-oped/) · [WNN, Linglong One](https://www.world-nuclear-news.org/articles/chinese-smr-completes-non-nuclear-steam-start-up-test) · [Science|Business, ITER](https://sciencebusiness.net/news/iter-fusion-project-confirms-more-delays-and-eu5b-cost-overrun) · [S&P, Helion Orion](https://www.spglobal.com/energy/en/news-research/latest-news/electric-power/073025-helion-energy-breaks-ground-on-fusion-power-plant-slated-to-be-online-in-2028) · [Lazard, LCOE+ 2025](https://www.lazard.com/media/uounhon4/lazards-lcoeplus-june-2025.pdf) · [Our World in Data, safest energy](https://ourworldindata.org/safest-sources-of-energy) · [Gaz d'aujourd'hui, EPR2 72,8 Md€](https://www.gazdaujourdhui.fr/edf-fixe-a-728-milliards-deuros-le-cout-plafond-des-six-epr2/) · [IAEA, Onkalo](https://www.iaea.org/newscenter/news/finlands-spent-fuel-repository-a-game-changer-for-the-nuclear-industry-director-general-grossi-says) · [MIT Tech Review, nucléaire et fossiles](https://www.technologyreview.com/2025/05/20/1116339/ai-nuclear-power-energy-reactors/) · [Asuene, taxonomie UE/CJUE](https://asuene.com/us/blog/the-eu-taxonomy-after-the-court-ruling-can-nuclear-and-gas-be-truly-sustainable) · [Spectre, The Left Goes Nuclear](https://spectrejournal.com/the-left-goes-nuclear/) · [Heinrich Böll, SMR](https://eu.boell.org/en/small-modular-reactors)

**Moratoires**
- [Bloomberg, Irlande lève le moratoire](https://www.bloomberg.com/news/articles/2025-12-12/ireland-set-to-end-moratorium-on-new-power-links-to-data-centers) · [DCD, Amsterdam](https://www.datacenterdynamics.com/en/analysis/the-ongoing-impact-of-amsterdams-data-center-moratorium/) · [American Prospect, moratoires](https://prospect.org/2025/12/22/demands-for-data-center-moratoriums-surge/) · [Data Center Watch](https://www.datacenterwatch.org/report) · [SELC, xAI Memphis](https://www.selc.org/news/resistance-against-elon-musks-xai-facility-in-south-memphis-gets-stronger/)

### Notes de méthode
Vérification adversariale, corrections intégrées : Three Mile Island = investissement Constellation **1,6 Md$** (le « 16 Md$ » répandu est l'apport au PIB de Pennsylvanie) ; Meta/Clinton = 1 121 MW confirmé, 6,6 GW en janv. 2026 ; le « 1 000 TWh en 2026 » re-daté ; Microsoft « abandon objectif 2030 » = envisagé/rapporté, non confirmé ; Saito et Parrique = cadres applicables, pas de position IA directe vérifiée ; Linglong One = imminent, NON confirmé opérationnel.

### Voir aussi
[Volet 16, L'empire matériel](./empire-materiel-sud-global-compute.md) · [Volet 21, La gauche mondiale](./gauche-mondiale-ia.md) · [Volet 23, NVIDIA et Huawei](./nvidia-huawei-deux-empires.md) · [Volet 25, Les solutions](./solutions-bifurcations.md)

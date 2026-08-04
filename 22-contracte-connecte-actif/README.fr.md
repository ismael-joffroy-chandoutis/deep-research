**Français. English version: [README.md](README.md)**

# Contracté, connecté, actif

### Le vocabulaire du calcul en 2026, et l'écart entre les gigawatts annoncés et les machines qui tournent

*Ismaël Joffroy Chandoutis*

*Juillet 2026*

---

Le débat public sur l'infrastructure de l'intelligence artificielle est saturé d'erreurs d'unités. On additionne des gigawatts comme s'il s'agissait de consommation, on compare des FLOPS qui ne mesurent pas la même chose, on met en regard des chiffres chinois de 2025 et des chiffres américains de 2024. Ces erreurs ne sont pas anodines : elles déterminent si l'on croit à un mur physique imminent ou à une expansion soutenable.

Il se trouve que l'industrie elle-même publie, dans ses documents réglementaires, le vocabulaire exact qui permet de trancher. Il suffit de le lire.

## Les trois capacités

Nebius Group N.V., dans son rapport annuel déposé auprès de la SEC le 30 avril 2026, ne définit pas une notion de capacité mais **trois** :

> « **Contracted power** is capacity that has been secured by land and contracted power commitments. […] **Connected power** is capacity that has power connected into data centers; and […] **Active power** is capacity being consumed by IT equipment and available for revenue generation. »

Contractée, connectée, active. Trois états successifs qui, dans les communiqués de presse, portent le même nom : « gigawatts ».

L'écart entre le premier et le troisième est l'information la plus utile de tout le dossier. Nebius annonce plus de 2 GW contractés en février 2026, pour environ **170 MW de puissance active** au 31 décembre 2025. Un rapport d'environ douze.

CoreWeave, dans son 10-K déposé le 2 mars 2026, permet de refaire le calcul sur une autre entreprise :

> « As of December 31, 2023, we operated 10 data centers with approximately 70 MW of active power. […] As of December 31, 2025, we operated 43 data centers with **over 850 MW of active power**. As of December 31, 2025, our **total contracted power capacity was approximately 3.1 GW**, which we expect to deploy over future periods. »

Rapport contracté sur actif : environ 3,6.

Toute agrégation médiatique de « gigawatts annoncés » surestime donc la capacité réellement en service d'un facteur compris entre trois et douze selon l'opérateur. Ce n'est pas de la tromperie — les documents sont publics et précis — c'est une négligence de lecture, et elle est systématique.

Le même soin s'impose pour convertir la puissance en énergie. À charge maximale et 8 760 heures par an, les 850 MW actifs de CoreWeave plafonnent à 7,45 TWh par an ; ses 3,1 GW contractés, à 27,2 TWh. Ce sont des plafonds théoriques : le facteur de charge réel n'est pas publié, et il n'est jamais de cent pour cent.

## Puissance et énergie

La confusion fondamentale du débat tient en une phrase qu'on lit partout : « ce centre de données consomme un gigawatt ». Un gigawatt n'est pas une consommation, c'est un appel de puissance instantané. La consommation se mesure en térawattheures sur une période.

Trois autres distinctions doivent être tenues en permanence. La capacité installée, exprimée en gigawatts de plaque signalétique, ne dit rien de ce qui est produit. La production, en térawattheures, n'est jamais égale à la capacité multipliée par 8 760 heures. Et la pointe — la puissance appelée à l'instant le plus tendu — est ce que le réseau doit couvrir, pas la moyenne.

Côté calcul, l'erreur dominante de 2025-2026 est arithmétique au sens propre : comparer des FLOPS en FP4 ou FP8 à des FLOPS en FP64. Les chiffres de performance des accélérateurs récents sont publiés dans des précisions basses qui multiplient mécaniquement les nombres. Un « exaflop » n'a de sens qu'accompagné de sa précision, et de la mention de savoir s'il s'agit d'un maximum théorique ou d'une mesure soutenue.

## Ce que l'on compare quand on compare les réseaux

L'affirmation la plus répandue sur l'énergie — la Chine produit plus du double de l'électricité américaine — est juste, mais les chiffres qui circulent pour l'étayer sont souvent hétérogènes.

Chine, 2025 : **10 420 TWh produits**, 10 368 TWh consommés. C'est le premier pays de l'histoire à dépasser les dix mille térawattheures de consommation annuelle. Les deux nombres circulent indifféremment alors qu'ils mesurent des choses différentes.

États-Unis, 2025 : **4 430 TWh** en production à grande échelle, auxquels s'ajoute environ 93 TWh de solaire diffus — que les tableaux principaux de l'agence américaine excluent, alors que la Chine, elle, compte son photovoltaïque distribué. Comparer sans ce correctif fausse la comparaison.

Le chiffre de « 4 300 TWh » pour les États-Unis, très répandu, est celui de **2024**, pas de 2025. Mettre en regard la Chine de 2025 et les États-Unis de 2024 gonfle artificiellement l'écart. Sur des bases homogènes, le rapport est d'environ 2,3, pas de 2,5.

La comparaison des capacités installées appelle la même prudence : la Chine publie en plaque signalétique et inclut le solaire distribué ; l'agence américaine publie principalement la puissance garantie en été, inférieure d'environ 7 % à la plaque. Le rapport « trois fois » que l'on lit partout dépend entièrement de la convention retenue.

Un chiffre est plus instructif que tous les autres : le **facteur de charge**. Chine, 2025 : environ 30,6 % sur l'ensemble du parc. États-Unis : environ 38,2 %. Le parc chinois est beaucoup plus grand et tourne beaucoup moins. Les heures d'utilisation publiées par le Conseil chinois de l'électricité le confirment dans le détail — 4 346 heures pour le charbon, 7 809 pour le nucléaire, mais 1 979 pour l'éolien et **1 088 pour le solaire**. Et l'écrêtement augmente pour la deuxième année consécutive : 5,7 % pour l'éolien, 5,2 % pour le solaire à l'échelle nationale, jusqu'à 16,6 % pour le solaire au Xinjiang.

L'avantage énergétique chinois est donc réel en volume, et beaucoup plus fragile en disponibilité au bon endroit et au bon moment — ce qui est précisément la contrainte d'un centre de calcul, qui n'accepte pas d'être écrêté.

## Ce que les projections valent

Le rapport *Energy and AI* de l'Agence internationale de l'énergie, publié en avril 2025, reste la référence du domaine. Ses chiffres méritent d'être cités entiers :

> « In total, electricity consumption from data centres is estimated to amount to around **415 terawatt hours (TWh)**, or about **1.5% of global electricity consumption in 2024**. It has grown at 12% per year over the last five years. »

> « In the Base Case, electricity consumption from data centres rises to around **945 TWh by 2030**, more than doubling from the 2024 level. »

Mais l'agence publie quatre scénarios, et l'écart entre eux est ce qu'il faut retenir : **670 TWh** dans le scénario *Headwinds*, **1 260 TWh** dans le scénario *Lift-Off* — un facteur 1,9 entre les bornes. À l'horizon 2035, la fourchette s'étend de 700 à 1 720 TWh.

Citer « 945 TWh en 2030 » sans la fourchette, ce qui est l'usage dominant, revient à transformer un intervalle de confiance en prophétie. L'incertitude n'est pas un défaut du rapport : elle est son résultat principal.

Il faut aussi tenir le premier chiffre en tête quand on parle de mur physique. En 2024, l'ensemble des centres de données du monde — pas seulement ceux dédiés à l'IA — représentait **1,5 % de la consommation électrique mondiale**. C'est considérable en croissance, modeste en niveau.

## Le vocabulaire qui se déplace

Un glissement lexical mérite d'être noté, parce qu'il n'est pas seulement cosmétique.

L'industrie parlait de **centres de données**. Elle parle de plus en plus d'**usines à intelligence** ou de **centres de calcul**. Le déplacement dit quelque chose de juste : un bâtiment qui entraîne des modèles ne stocke pas des données, il transforme de l'électricité en paramètres. Sa contrainte dimensionnante n'est plus la surface au sol ni la bande passante, mais la puissance électrique disponible et l'évacuation de la chaleur. C'est une usine, au sens propre : une machine à convertir de l'énergie.

Le partage entre **entraînement** et **inférence** redistribue par ailleurs les cartes. L'entraînement est un pic concentré, tolérant à la latence, indifférent à la localisation — il peut se faire loin, là où l'énergie est bon marché. L'inférence est diffuse, permanente, sensible à la latence, et doit être proche des utilisateurs. C'est cette seconde charge qui pousse vers le **calcul en périphérie** et les architectures hybrides, et c'est elle qui croît le plus vite à mesure que les usages se banalisent. Un raisonnement fondé uniquement sur le coût d'entraînement des grands modèles rate donc la moitié de la question.

## Campus AI, ou la souveraineté au conditionnel

La France a son projet, et il concentre toutes les ambiguïtés du domaine.

**Campus AI** associe Bpifrance, Mistral, le fonds émirati **MGX** et **NVIDIA** dans une coentreprise visant jusqu'à **3 GW** de capacité de calcul répartis sur le territoire, présentée comme le plus grand campus d'IA d'Europe. Le site pilote est prévu à **Fouju**, en Seine-et-Marne, à l'est de Paris. Les travaux doivent démarrer au second semestre 2026, la mise en service à l'horizon 2028.

Trois remarques s'imposent, et elles découlent directement de ce qui précède.

D'abord, « 3 GW » est une capacité visée, c'est-à-dire au mieux de la puissance *contractée*, et à ce stade même pas cela. Sur les ratios observés chez Nebius et CoreWeave, la puissance active à la mise en service sera d'un tout autre ordre. Ce n'est pas une critique du projet, c'est une lecture correcte de son annonce.

Ensuite, la structure du tour de table interroge le mot « souveraineté ». Le capital vient pour partie d'un fonds d'Abou Dabi, le matériel vient de NVIDIA, et le modèle vient de Mistral. Sur les trois couches — capital, silicium, poids — une seule est française. C'est mieux que zéro, et c'est exactement la position qu'occupe l'Europe : souveraine sur la couche qui se copie, dépendante sur les deux qui ne se copient pas.

Enfin, la contrainte réelle sera le raccordement. En France comme ailleurs, le facteur limitant n'est plus le foncier ni le capital mais le délai d'accès au réseau et la disponibilité des équipements électriques de haute tension. C'est ce qui explique qu'environ la moitié des centres de données américains prévus pour 2026 soient retardés ou annulés — non par manque de demande, mais par manque de transformateurs et de créneaux de raccordement.

## Le dossier adverse

**Les entreprises ne mentent pas sur leurs chiffres.** Nebius et CoreWeave publient les trois notions de capacité dans des documents réglementaires engageant leur responsabilité. L'écart entre contracté et actif est documenté par les intéressés eux-mêmes. Le problème est du côté de la lecture, pas de l'émission.

**La capacité contractée n'est pas fictive.** Elle représente du foncier sécurisé et des engagements de fourniture réels, qui se transformeront en capacité active sur plusieurs années. Traiter les gigawatts contractés comme du vent serait l'erreur symétrique de celle qui consiste à les traiter comme actifs. Ce sont des promesses gagées, à échéance incertaine.

**Le facteur de charge chinois faible n'est pas seulement une faiblesse.** Un parc surdimensionné avec beaucoup de renouvelable intermittent produit mécaniquement un facteur de charge bas. C'est le prix d'une transition rapide, pas nécessairement un symptôme d'inefficacité. La conclusion honnête est que cet avantage est plus difficile à convertir en alimentation stable de centres de calcul qu'il n'y paraît — pas qu'il est illusoire.

**La fourchette de l'IEA est large parce que l'avenir est ouvert.** Reprocher à un scénario d'avoir un facteur deux entre ses bornes revient à reprocher à l'incertitude d'exister. Ce qui est critiquable, c'est l'usage sélectif de la borne qui arrange l'argument que l'on défend — dans les deux sens.

## Ce qui se joue réellement

**Le goulot s'est déplacé du silicium vers le cuivre.** Pendant trois ans, la question était l'accès aux accélérateurs. Elle est devenue l'accès à la puissance électrique, aux transformateurs, aux postes de raccordement et aux délais d'instruction administrative. C'est un domaine où l'argent n'accélère presque rien : les délais de fabrication d'équipements haute tension et les procédures de raccordement ne se paient pas pour être raccourcis.

**L'inflation des composants pollue les chiffres.** Une part significative de la hausse des dépenses d'investissement annoncées par les hyperscalers en 2026 est de l'inflation sur la mémoire et les composants, et non de la capacité additionnelle. Les chiffres bruts de capex surestiment la croissance de capacité réelle — un correctif rarement appliqué dans le débat sur la bulle.

**La métrologie est une position politique.** Choisir de parler en gigawatts annoncés plutôt qu'en mégawatts actifs, en FP4 plutôt qu'en FP64, en capacité de plaque plutôt qu'en facteur de charge, ce n'est pas neutre : chacun de ces choix multiplie le nombre par un facteur connu, et sert un argument. Les documents réglementaires, eux, sont contraints à la précision. Ils sont ennuyeux et ils sont exacts, et c'est pour cela qu'on ne les lit pas.

## Ce qui reste

Le vocabulaire dont l'industrie s'est dotée pour ses propres besoins comptables — contracté, connecté, actif — est plus utile au débat public que tout ce que le débat public a produit sur le sujet. Il dit qu'entre l'annonce et la machine qui tourne, il y a trois états, plusieurs années, et un facteur trois à douze.

Cela ne règle pas la question de savoir si la trajectoire est soutenable. Cela déplace simplement le curseur : le mur physique dont on parle depuis deux ans n'est pas encore une contrainte de production d'électricité, il est déjà une contrainte de raccordement et d'équipement. Ce n'est pas la même chose, cela n'appelle pas les mêmes réponses, et cela se mesure sur une échelle de temps que ni les communiqués ni les cycles trimestriels ne savent représenter.

*Dans la continuité des volets [02](../02-sovereignty-machine/), [16](../16-le-robinet-et-la-boucle/) et [20](../20-avec-de-gros-ordinateurs/).*

---

## Sources

Primaires :

- [Nebius Group N.V., Form 20-F, exercice 2025, déposé le 30 avril 2026](https://www.sec.gov/Archives/edgar/data/1513845/000110465926052948/nbis-20251231x20f.htm) — définitions de *contracted*, *connected* et *active power*.
- [CoreWeave, Inc., Form 10-K, exercice 2025, déposé le 2 mars 2026](https://www.sec.gov/Archives/edgar/data/1769628/000176962826000104/crwv-20251231.htm) — série historique de puissance active et capacité contractée.
- [Agence internationale de l'énergie, *Energy and AI*, avril 2025](https://www.iea.org/reports/energy-and-ai) — [rapport intégral en PDF](https://iea.blob.core.windows.net/assets/dd7c2387-2f60-4b60-8c5f-6563b6aa1e4c/EnergyandAI.pdf).
- [U.S. Energy Information Administration, *Electric Power Monthly*, tableau 1.1 (publication du 23 juillet 2026)](https://www.eia.gov/electricity/monthly/epm_table_grapher.php?t=epmt_1_01) et [tableau 1.1.A pour le solaire diffus](https://www.eia.gov/electricity/monthly/epm_table_grapher.php?t=epmt_1_01_a).
- [EIA, « U.S. electricity generation in 2025 hit a record, again », 5 mars 2026](https://www.eia.gov/todayinenergy/detail.php?id=67284).
- [Administration nationale de l'énergie de Chine, statistiques 2025, 17 janvier 2026](https://www.nea.gov.cn/20260121/715f79826488476a9162da7c8bd77c80/c.html) et [China Electricity Council, 2 février 2026](https://cec.org.cn/detail/index.html?3-353833) ; [reprise officielle en anglais](https://english.www.gov.cn/archive/statistics/202601/17/content_WS696b548ec6d00ca5f9a08a0e.html).

Sur Campus AI :

- [Communiqué de l'École polytechnique, « MGX, Bpifrance, Mistral AI and NVIDIA launch joint venture to build Europe's largest AI campus in France »](https://polytechnique.edu/en/press-room/press-releases/mgx-bpifrance-mistral-ai-and-nvidia-launch-joint-venture-build-europes-largest-ai-campus-france).
- [DataCenterDynamics, « MGX, Bpifrance, Nvidia and Mistral AI plan 1.4GW Paris data center campus »](https://www.datacenterdynamics.com/en/news/mgx-bpifrance-nvidia-and-mistral-ai-plan-14gw-paris-data-center-campus/).
- [L'Usine digitale, « Jusqu'à 3 GW de capacité de calcul : un an après, le projet de campus IA s'accélère »](https://www.usine-digitale.fr/intelligence-artificielle/ia-generative/jusqua-3-gw-de-capacite-de-calcul-un-an-apres-le-projet-de-campus-ia-soutenu-par-bpifrance-mistral-ai-et-nvidia-saccelere.DKSA2S2V6NACDO5LFZMIYBJB5Y.html).

Les chiffres de dépenses d'investissement des hyperscalers cités ici proviennent de compilations de documents déposés auprès de la SEC et non des documents eux-mêmes. Les données chinoises d'écrêtement et d'heures d'utilisation proviennent d'un centre de planification chinois relayé par une synthèse tierce, et non de la publication d'origine. Les conversions de puissance en énergie sont des plafonds théoriques à charge maximale : aucun opérateur ne publie son facteur de charge réel, de sorte que la consommation effective est nécessairement inférieure, dans une proportion inconnue. Le calendrier et la capacité de Campus AI sont des objectifs annoncés par les porteurs du projet, à une date où aucune construction n'a commencé.

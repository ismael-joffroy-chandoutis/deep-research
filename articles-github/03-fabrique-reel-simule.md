# La fabrique d'un réel simulé
## Des différents usages du deepfake

**Entretien avec Ismaël Joffroy Chandoutis**
Réalisé par Antonio Somaini

*Entretien initialement conduit en juin 2024. Mis à jour en février 2026 pour intégrer les évolutions du projet et du contexte technologique.*

---

## 1. Découverte des deepfakes

**Antonio Somaini** : Quand et comment es-tu arrivé à t'intéresser aux deepfakes ? Quel aspect de leur diffusion initiale a attiré ton attention ?

**Ismaël Joffroy Chandoutis** : J'ai commencé à réfléchir aux deepfakes alors que je terminais *Swatted* (2018), un film qui traite d'un phénomène de trolling spécifique : des personnes mal intentionnées appellent la police en se faisant passer pour quelqu'un d'autre et font des déclarations du type « j'ai tué ma mère avec un fusil AR-15 », dans le seul but de faire intervenir les forces de l'ordre et de flanquer une sacrée trouille aux victimes dont l'identité a été ainsi usurpée. C'est véritablement au début de l'année 2019 que j'ai analysé en profondeur les usages des deepfakes pour préparer une intervention dans un colloque intitulé « L'humain qui vient », organisé autour d'un groupe de recherche sous la coordination de Joseph Cohen, Olivier Perriquet et Raphael Zagury-Orly. En pensant à l'avenir de l'humain, il m'est apparu déterminant d'effectuer une articulation entre l'intelligence artificielle et mon travail, qui oscille toujours entre investigation journalistique et pratique artistique.

J'ai été tout d'abord très frappé par l'énorme décalage entre les publications scientifiques consacrées à l'IA et la manière dont elles sont traduites et discutées dans la sphère médiatique. Dans la presse généraliste traitant de l'IA, tout est placé sous le signe de la menace, alors qu'il s'agit dans la plupart des cas de projections relevant de la science-fiction — mais il est vrai que dans une économie basée sur l'attention, la peur constitue une stratégie efficace pour vulgariser (et déformer) les recherches scientifiques. C'est dans ce cadre qu'un phénomène a retenu mon attention : le deepfake.

Cette technologie permet, par l'entremise d'une suite d'algorithmes, de manipuler des images et des sons et d'en transformer le sens initial. Le terme d'IA est souvent appliqué, de façon excessive, aux technologies de deepfake en raison de leur utilisation de techniques de deep learning pour analyser et reproduire les traits d'un visage, une tâche qui imite une forme d'intelligence « visuelle » ou « perceptive ». Toutefois, il est important de garder à l'esprit que ces systèmes, aussi impressionnants soient-ils, fonctionnent principalement comme des outils sophistiqués de traitement de l'image qui nécessitent une importante intervention humaine pour guider et affiner leur travail. Le rôle qu'y accomplit l'IA relève donc davantage de l'assistance que d'une entité autonome capable de créativité ou de compréhension à part entière.

Dans le deepfake, on peut prendre le corps et le visage de quelqu'un pour lui faire prononcer des paroles ou produire des actions. Il m'est apparu comme la seule technologie intéressante à aborder, parmi toutes celles qui mobilisent l'IA, en raison de son caractère non spéculatif. Le deepfake n'est qu'une nouvelle itération des problématiques de l'ère de la post-vérité. Surtout, c'est une technologie complètement accessible car les outils qui la gouvernent sont pour beaucoup en open source. Financièrement, elle est donc abordable : il suffit de disposer d'un ordinateur de moyenne gamme, d'un peu de temps et de maîtriser le langage Python à un niveau débutant.

---

## 2. Usages des deepfakes

**A. S.** : Le champ des deepfakes se présente comme un terrain conflictuel, dans lequel se font face les producteurs de deepfakes d'une part et les systèmes d'autre part qui essaient de les repérer et de les identifier, ou d'en rendre la réalisation impossible en « sécurisant » des vidéos. Que penses-tu de ces combats autour de cette nouvelle forme audiovisuelle ?

**I. J. C.** : Si l'on prend les statistiques connues à ce jour, 99 % des deepfakes sont à caractère pornographique et impliquent des femmes sans leur consentement, à leur insu. Outre les conséquences parfois désastreuses pour les victimes, la détection de ces deepfakes donne lieu à un véritable jeu du chat et de la souris : au moment même où des moyens techniques permettant d'identifier des deepfakes sont mis en place, des parades sont inventées pour les contourner. Les programmeurs s'appuient notamment sur leur connaissance des techniques de data forensics utilisées pour détecter les deepfakes. Ils tentent par exemple de réduire les écarts de bruit numérique et de luminosité entre le corps et le visage, qui sont des indices révélateurs pour les enquêteurs spécialisés. Ils s'attaquent également à d'autres paramètres comme la cohérence de réflexion des yeux, la pulsation du sang dans les veines ou la gestique faciale. En somme, les programmeurs de deepfakes s'efforcent d'identifier et de gommer tous les éléments sur lesquels s'appuient les techniques de détection issues de la criminologie numérique, dans une course permanente pour contourner ces méthodes d'authentification.

**A. S.** : Lors de nos échanges préalables à cet entretien, tu as souligné la possibilité d'utiliser des deepfakes dans le cadre de stratégies d'action politique : par exemple, pour protéger l'anonymat de personnes — des militants politiques, des dissidents — qui ne souhaitent pas être identifiées par des systèmes de reconnaissance faciale. Peux-tu évoquer ces usages politiques « positifs » des deepfakes, qui offrent un contrepoint à la tendance générale à dénoncer les deepfakes ?

**I. J. C.** : Je crois qu'il est important de protéger les lanceurs d'alertes tout en conservant leur humanité. Or la technique habituelle de floutage pour garantir l'anonymat de personnes filmées m'a toujours hautement déplu ; on dit au spectateur : « voyez, on ne peut pas vous montrer cela », et on ne fait rien d'autre que de regarder cette zone floutée. C'est un procédé très hypocrite, qui déconcentre le spectateur et déshumanise les personnes filmées. Je considère que le deepfake permet de remédier à ce problème. Je pense à cet égard au film *Z32* d'Avi Mograbi (2008), qui m'apparaît comme un précurseur au niveau conceptuel : la réhumanisation du visage n'est pas seulement technique ou émotionnelle, elle est sujet.

---

## 3. Deepfakes et blockchain

**A. S.** : Ce volume des *Carnets du BAL*, intitulé *L'image à l'épreuve des machines*, analyse toute une série d'opérations rendues possibles par de nouveaux croisements entre machines et images, en faisant référence à la notion d'« images opératoires » élaborée par Farocki au début des années 2000. Parmi les opérations que les deepfakes permettent d'effectuer, on compte celles qui offrent la possibilité de ranimer des personnes disparues ou de rajeunir comme de vieillir des personnes encore en vie. Qu'est-ce que ces phénomènes t'inspirent ?

**I. J. C.** : On peut effectivement animer les défunts en combinant la technologie du deepfake avec une IA alimentée par la « mémoire » du défunt — ses traces textuelles, visuelles et audiovisuelles. Dans la série *Black Mirror*, une production britannique rendue célèbre pour son exploration dystopique des nouvelles technologies, figure un épisode dans lequel c'est même le corps tout entier du défunt qui est reconstitué, selon une perspective fortement technophobe. Je me montre plus optimiste à cet égard car je crois que de telles technologies, si elles sont bien employées, pourraient permettre de mieux affronter l'étape du deuil, dans le cadre d'un accompagnement psychologique résolument novateur. Le potentiel est énorme.

Mais demeure le problème d'un éventuel piratage du dispositif ; des hackers pourraient profiter de la faiblesse de personnes endeuillées pour leur soutirer de l'argent. Il faudrait aussi se questionner sur le design de l'IA employée, s'interroger sur les procédures selon lesquelles elle a été entraînée. Car les biais peuvent être nombreux, à commencer par ceux inhérents au commerce lucratif qu'une telle technologie rend possible. Par exemple, une IA entraînée principalement sur des données issues d'une culture ou d'un milieu social donné pourrait produire des résultats peu représentatifs d'autres contextes. C'est l'une des limites d'une telle simulation. Pour ma part, je pense utiliser des technologies open source, en local — c'est-à-dire que mes données seront stockées uniquement sur mes disques durs et ne seront pas exploitées par des sociétés commerciales ni ne circuleront sur des serveurs tiers.

**A. S.** : Comment envisages-tu les relations entre la forme audiovisuelle des deepfakes et la technologie de la blockchain ? Soit entre un outil de simulation et un outil d'authentification ?

**I. J. C.** : Leurs relations sont placées sous le signe d'une certaine ambivalence. D'une part, la blockchain pourrait aider à certifier l'authenticité d'un signal audiovisuel par une empreinte unique appelée « hash file ». Cela confère une robustesse et un caractère immuable au signal, qui garantit qu'il n'a pas été altéré. La technologie blockchain fonctionne comme une combinaison de BitTorrent et d'un système cryptographique similaire aux DCP : un hash file est envoyé depuis une adresse vers une autre tandis que la conformité du transport est certifiée par des machines décentralisées. Ce transport peut concerner n'importe quel élément : texte, image, son, vidéo. C'est pourquoi les NFT sont particulièrement appropriés pour authentifier et horodater un objet, et une blockchain comme Ethereum est très adaptée pour proposer différents services, tels que le streaming décentralisé.

Pour autant, les NFT ont un rapport ambivalent à l'authenticité. D'un côté, la blockchain sur laquelle ils reposent assure une traçabilité : elle enregistre de manière transparente et immuable chaque transaction, chaque changement de propriétaire. Si le fichier lié au token est modifié, cela laisse une trace visible dans l'historique du NFT.

Mais de l'autre, rien n'empêche techniquement le propriétaire d'un NFT de modifier le fichier associé, tout en conservant le lien vers ce nouveau fichier. Ainsi, un NFT peut servir à authentifier un deepfake tout en rendant très difficile son retrait, puisqu'il faudrait l'accord du propriétaire. Les NFT apparaissent donc comme une arme à double tranchant : ils certifient l'origine d'un fichier sans garantir son intégrité.

C'est pourquoi les NFT soulèvent des questions inédites pour les deepfakes : en les mintant sous forme de jetons non fongibles, on les inscrit dans un registre décentralisé qui leur confère une forme d'authenticité et une visibilité difficiles à effacer, quand bien même il s'agirait de contenus mensongers ou préjudiciables.

Au-delà de tous ces aspects techniques, il convient également de conserver un regard critique sur l'idéologie sous-jacente aux NFT et à la blockchain. Les NFT reposent sur une logique spéculative et libertarienne au service du marché. À l'inverse, des solutions alternatives comme git — un système de gestion de versions distribuées très utilisé en développement logiciel — pourraient être plus pertinentes et éthiques pour certifier l'authenticité d'un contenu. Avec git, on peut tracer et vérifier l'origine et l'intégrité d'un fichier de manière distribuée, sans tomber dans les travers de la spéculation et de l'ultra-individualisme propres aux blockchains et aux NFT.

Enfin, Adobe avait lancé une autre initiative pour certifier l'authenticité des contenus avec son Content Authenticity Initiative (CAI), sans recourir à la blockchain — mais celle-ci n'a pas réellement pris, pour des raisons multiples : complexité d'utilisation pour l'utilisateur lambda, absence de cas d'usage réel en dehors de niches professionnelles, et un système finalement assez simple à contourner.

> **Note de mise à jour (2026)** : Cet entretien date de juin 2024. Depuis lors, le marché des NFT s'est effondré et leur usage comme outil de certification de contenu n'a pas trouvé de débouché significatif. Les enjeux d'authentification des médias synthétiques ont, eux, considérablement gagné en acuité — notamment avec la multiplication des deepfakes dans les contextes électoraux et informationnels. Les réflexions formulées ici restent pertinentes dans leur structure, mais le paysage technique et économique a profondément évolué.

En somme, blockchain et deepfakes cristallisent les enjeux contemporains autour de la notion de vérité à l'ère numérique, une époque tiraillée entre la quête d'une origine certifiée et la prolifération de simulacres. Mon travail artistique cherche précisément à explorer cette tension entre l'artificiel et le réel, entre l'authenticité et sa mise en doute.

---

## 4. Deepfakes dans la création artistique

**A. S.** : Quel rôle jouent les deepfakes dans ton travail actuel ?

**I. J. C.** : Je mobilise le deepfake dans le cadre de recherches autour de l'identité numérique, sur la fabrique du vrai et du faux, et sur l'impact émotionnel de toutes ces technologies dans notre rapport au réel. J'ai d'abord approché le deepfake à travers trois projets : une commande pour un long métrage documentaire visant à anonymiser des personnes sans recourir au floutage pour ne pas les déshumaniser ; un film intime sur le deepfake comme néo-rituel de deuil, comme je le précisais précédemment ; et une œuvre plus grand public, *Deepfake*, un thriller dont la narration tourne autour d'une streameuse en pleine ascension qui voit sa réputation menacée par l'apparition d'un deepfake d'une troublante véracité.

Durant le processus d'écriture de *Deepfake* avec ma co-scénariste Perrine Prost, nous avons réalisé qu'il fallait diffracter les points de vue et inclure aussi bien celui de la communauté réagissant aux vidéos que celui de l'antagoniste — créateur du deepfake originel — avec une approche rappelant celle de mon précédent film *Swatted* ou encore celle de *Zodiac* de David Fincher (2007). L'enjeu est de montrer la diversité des réceptions possibles d'un même contenu deepfake, entre adhésion et résistance, ainsi que les motivations parfois troubles de leurs créateurs. C'est en essayant de déterminer le statut et l'identité d'un tel protagoniste que je suis tombé sur le cas réel de Joshua Ryne Goldberg, un troll ayant endossé plus d'une centaine de personas différentes en usurpant l'identité de personnes réelles.

Intrigué, je suis entré en contact avec lui alors qu'il purgeait une peine de dix ans de prison. La relation que j'ai nouée avec lui a considérablement influencé mon projet, à tel point que j'ai décidé de faire un spin-off du film *Deepfake* intitulé *Madotsuki_the_Dreamer*, un corpus d'œuvres hybrides offrant plusieurs regards sur l'un des trolls les plus prolifiques et influents de l'histoire d'Internet. Ce travail, présenté par itération, a depuis évolué vers un projet de plus grande envergure intitulé *The Goldberg Variations*.

J'ai commencé par une installation pour la Biennale d'art numérique Nemo (Paris, 2023), qui plongeait le spectateur dans sa chambre, avec une vidéo se concentrant sur sa persona djihadiste, laquelle a mené à son arrestation en 2015 pour projet d'attentat terroriste. En 2024, j'ai présenté une autre installation au Port des créateurs (Toulon), incluant une série de photos générées par IA inspirées de nos échanges, ainsi qu'une datavisualisation produite à partir d'une base de données construite en récupérant toutes les traces laissées par Joshua sur le web 2.0 : des milliers de contributions sur IMDb (c'est un grand cinéphile), des centaines d'entrées sur Wikipedia et Reddit (certaines de ses personas géraient la modération de 150 subreddits).

> *Note : le projet continue d'évoluer.*

La prochaine version du projet sera constituée d'une installation avec une vidéo générative, un journal intime sous la forme d'un deepfake qui se transforme sous nos yeux, de façon à insister sur son caractère insaisissable. Le projet aboutira sur une dernière œuvre : un long métrage linéaire.

Malgré l'utilisation de techniques de manipulation de l'image, ma démarche s'inscrit dans un geste post-documentaire et cherche paradoxalement à révéler une vérité.

Je crée un « réel simulé » à travers les images générées par IA — un espace latent nourri d'images authentiques dans lequel je me pose en observateur de ce qui peut émerger d'artificiellement « juste » — avant de sélectionner et d'assembler la matière pour construire la structure narrative. Cela peut paraître étrange, mais quand je travaille de cette manière, je n'ai que Frederick Wiseman et ses réalité-fictions en tête.

---

## Annexe : repères lexicaux

**Deep learning** : sous-domaine de l'apprentissage automatique utilisant des réseaux de neurones artificiels à plusieurs couches pour analyser et reproduire des données complexes (visages, voix, textes).

**Deepfake** : technique de synthèse d'image ou de son basée sur le deep learning, permettant de substituer le visage ou la voix d'une personne dans une vidéo existante. Contraction de *deep learning* et *fake*.

**Data forensics** : ensemble des techniques d'investigation numérique permettant d'analyser des fichiers pour en déterminer l'authenticité ou l'origine, souvent utilisé en criminologie numérique.

**Hash file** : empreinte numérique unique générée à partir du contenu d'un fichier. Toute modification du fichier produit une empreinte différente, permettant de vérifier son intégrité.

**NFT (Non-Fungible Token)** : jeton numérique unique enregistré sur une blockchain, utilisé pour certifier la propriété ou l'authenticité d'un fichier numérique.

**Blockchain** : base de données distribuée et décentralisée dans laquelle les transactions sont enregistrées de manière transparente et immuable, sans autorité centrale.

**Git** : système de gestion de versions décentralisé, permettant de tracer l'historique des modifications d'un fichier et d'en vérifier l'intégrité.

**Open source** : désigne un logiciel dont le code source est librement accessible, modifiable et redistribuable.

**Post-documentaire** : pratique cinématographique qui questionne les conventions du documentaire classique en intégrant des procédés de fiction, de reconstruction ou de manipulation de l'image tout en maintenant un ancrage dans le réel.

---

*Ismaël Joffroy Chandoutis est cinéaste et artiste. Son travail a été présenté au Festival de Cannes, à la Berlinale et au Centre Pompidou. Il est lauréat d'un César (2022). Il développe actuellement* The Goldberg Variations, *un projet hybride entre documentaire, installation et long métrage.*

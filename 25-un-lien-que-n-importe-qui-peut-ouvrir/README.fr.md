**Français. English version: [README.md](README.md)**

# Un lien que n'importe qui peut ouvrir

### Douze minutes séparent l'annonce de Build Mode de l'invitation du directeur produit de X. Elles ne promettent pas la même chose.

*Ismaël Joffroy Chandoutis*

*Août 2026*

---

Le 28 juillet 2026 à 16 h 24 UTC, Nikita Bier, directeur produit de X, publie quatre phrases :

> « Photos & video were how the last generation expressed themselves.
>
> Today's form of expression is software.
>
> Who will create the next viral game or app that plays right inside of the X Timeline?
>
> Try the new Grok app builder. »

Le post est accompagné d'une vidéo dont le seul texte lisible est « Share apps from web ». Au moment de la capture qui sert de point de départ à ce volet : 1,5 million de vues, 1 200 réponses, 933 republications, 7 600 « j'aime », 1 900 mises en signet.

Douze minutes plus tôt, à 16 h 12 UTC, le compte de Benji Taylor annonçait le lancement du produit. Et le communiqué officiel de SpaceXAI, publié le même jour, décrit la fonctionnalité en une phrase qui ne contient ni le mot X, ni le mot timeline :

> « Tell Grok an idea, and it builds a working version live in your chat, on the web or your phone. **When it's ready, publish it to a link anyone can open.** »

Un lien que n'importe qui peut ouvrir. C'est l'unité de distribution réelle du produit. Entre cette phrase et « une appli qui tourne à l'intérieur de la timeline X », il y a douze minutes, deux comptes, et une couche logicielle qui n'existe pas.

Ce volet examine l'écart. Pas pour épingler une exagération promotionnelle — les directeurs produit exagèrent, c'est le métier — mais parce que l'écart est exactement à l'endroit où se décide qui possède quoi dans la chaîne qui va de la fabrication d'un logiciel à sa rencontre avec un public.

## La méthode : dater les sources à la seconde

Les deux publications sont horodatées par leurs identifiants. X (comme Twitter avant lui) attribue à chaque post un entier de type *snowflake* dont les 41 bits de poids fort encodent le nombre de millisecondes écoulées depuis le 4 novembre 2010 à 01 h 42 min 54,657 s UTC. La transformation est déterministe :

```python
timestamp_ms = (post_id >> 22) + 1288834974657
```

Appliquée aux deux identifiants :

| Identifiant | Compte | Horodatage (UTC) |
|---|---|---|
| `2082137145507254440` | @benjitaylor | 2026-07-28 16:12:34,383 |
| `2082140254237241588` | @nikitabier | 2026-07-28 16:24:55,562 |

Écart : **12 minutes et 21 secondes**. La capture d'écran affiche « 18:24 · 7/28/26 », soit le même instant en heure d'Europe centrale d'été (UTC+2), ce qui confirme la lecture et situe l'appareil de capture.

Ce n'est pas un détail de forensique pour le plaisir. Cela établit que les deux énoncés appartiennent à la même séquence de lancement, coordonnée, et que la différence entre eux n'est pas un effet de dérive dans le temps : c'est une différence de fonction. L'un annonce ce que le produit fait. L'autre annonce ce qu'on aimerait que le public en fasse.

## Ce que Build Mode fait réellement

Build Mode est entré en bêta anticipée le 28 juillet 2026. Le périmètre, tel qu'il ressort des notes de version et de la documentation produit :

- **Entrée** : une consigne en langue naturelle dans une conversation Grok.
- **Sortie** : une application web fonctionnelle avec état — pages d'accueil, portfolios, outils de productivité, jeux d'arcade et 3D, tableaux de bord. Les démonstrations de SpaceXAI (`driver.grok.me`, un simulateur de ville, des jouets physiques, des boîtes à rythmes) sont choisies pour prouver qu'il s'agit d'objets interactifs et non de HTML statique.
- **Itération** : en langue naturelle, sans toucher au code.
- **Publication** : un sous-domaine `grok.me`, ou un domaine que l'utilisateur possède déjà.
- **Sortie du système** : export du code source vers GitHub.
- **Accès** : réservé aux abonnés SuperGrok Heavy, soit environ 300 dollars par mois, sur web, iOS et Android.

Rien, dans les notes de version de juillet 2026, ne mentionne une intégration à la timeline de X. Rien dans le communiqué non plus. Le mode de diffusion est un lien. Un lien s'ouvre dans un navigateur ; sur X, il produit une carte cliquable qui envoie l'utilisateur ailleurs — précisément le geste que tout algorithme de timeline pénalise depuis dix ans, et que la grille tarifaire de l'API de X facture elle-même à part : 0,015 dollar par post créé, **0,20 dollar si le post contient un lien**. Treize fois plus cher. La plateforme a inscrit dans son barème ce qu'elle pense des liens sortants.

Il faut donc énoncer le fait simplement, parce qu'il est vérifiable et qu'il n'a pas circulé : **au 4 août 2026, une semaine après le post, aucune source publique ne documente une couche d'exécution applicative dans la timeline de X, ni une seule application construite avec Build Mode devenue virale.** La question « qui fera la prochaine appli virale qui tourne dans la timeline ? » porte sur une surface qui n'a pas été annoncée.

L'initiative existe, mais elle vient de l'extérieur : une équipe tierce, AGNT Hub, construit une couche d'exécution « X Mini Apps » avec l'argument que les interfaces embarquées légères retiennent mieux l'attention que les applications mobiles classiques. C'est-à-dire que le travail d'infrastructure que la phrase de Bier suppose accompli est en cours chez quelqu'un d'autre, sans garantie d'accès.

## Les chiffres du post lui-même

Le post est un document. Ses métriques en sont un autre. Elles se lisent, avec les précautions d'usage.

| Métrique | Valeur | Part des vues |
|---|---|---|
| Vues | 1 500 000 | — |
| « J'aime » | 7 600 | 0,507 % |
| Réponses | 1 200 | 0,080 % |
| Republications | 933 | 0,062 % |
| Signets | 1 900 | 0,127 % |
| **Total des interactions** | **11 633** | **0,776 %** |

Trois rapports méritent l'attention.

**Réponses / republications = 1,29.** Il y a plus de gens qui répondent que de gens qui relaient. Sur un post promotionnel, c'est l'inverse du profil attendu : un lancement bien reçu se propage plus qu'il ne se discute. Un rapport supérieur à 1 signale une audience qui argumente. Il ne dit pas dans quel sens — les réponses n'ont pas été codées ici, et je ne prétends pas les avoir lues.

**Signets / republications = 2,04.** Deux fois plus de gens archivent le post en privé qu'ils ne le republient sous leur nom. Le signet est le geste de la ressource qu'on garde ; la republication est celui de l'adhésion qu'on affiche. L'écart décrit une audience qui prend note de l'outil sans endosser la thèse.

**Interactions totales / vues = 0,78 %.** Les référentiels 2026 pour X situent la moyenne de plateforme autour de 0,10 % et la médiane entre 0,59 % et 1,11 % selon les méthodologies — qui divergent au point qu'aucune comparaison fine n'est solide. Le post est donc dans la zone médiane. Pour un compte de cette taille, avec ce niveau d'amplification structurelle, c'est un résultat ordinaire.

Les précautions, puisqu'elles comptent plus que les chiffres : une « vue » sur X est une impression, pas une lecture ; les valeurs sont arrondies à l'affichage (« 1,2 K », « 7,6 K »), ce qui donne une incertitude de l'ordre de ±50 sur chaque terme ; le post émane du directeur produit de la plateforme qui décide de l'ordre du fil, situation où l'exposition n'est pas obtenue mais attribuée ; et l'instantané date de la capture, pas de la publication. Aucune de ces réserves n'annule le rapport réponses/republications, qui est interne au post et donc insensible au volume d'exposition.

Ce que ces chiffres établissent est modeste et suffisant : 1,5 million d'impressions pour une invitation à bâtir n'a produit, une semaine plus tard, aucune construction visible. Le premier terme est mesuré, le second est une absence — et une absence n'est pas une preuve. Elle est simplement, ici, ce qu'on a.

## La généalogie que la phrase efface

« Qui fera la prochaine appli virale qui tourne dans la timeline » suppose qu'il y en a eu une précédente. Il y en a eu plusieurs. Leur historique est presque uniformément mauvais, et il est public.

**Facebook Instant Games**, lancé fin 2016 dans Messenger puis ouvert au fil d'actualité, aura été la tentative la plus dotée. Meta a annoncé l'extinction de ses Web Games : ils cessent de fonctionner le **30 septembre 2026**, sauf migration vers un périmètre restreint. La fin de dix ans d'expérimentation tombe deux mois après le post qui en propose la reprise.

**Snap Games et Minis**, lancés en 2019, revendiquaient plus de 200 millions de joueurs en 2021. Snap a acté l'arrêt des investissements dans un dépôt réglementaire du 26 août 2022, au motif que ces produits ne pouvaient pas contribuer à ses priorités ; le support a confirmé la disparition le 7 février 2023. Deux cents millions d'utilisateurs n'ont pas suffi à sauver la couche.

**Farcaster** est le cas le plus proche, et le plus récent. Les *Frames* — rebaptisés *Mini Apps* en v2 — font exactement ce que la phrase de Bier appelle de ses vœux : une application interactive qui s'exécute dans le fil, sans quitter le client. C'était la promesse de 2024. Au début de 2026, avec une valorisation annoncée autour du milliard de dollars le 21 janvier, les utilisateurs actifs quotidiens avaient chuté de 40 % et les revenus de 85 %. La couche fonctionnait techniquement. Elle n'a pas retenu.

**WeChat** est le contre-exemple, et il faut le prendre au sérieux parce qu'il est écrasant : 4,3 millions de mini-programmes, 945 millions d'utilisateurs mensuels en Chine, environ 9,8 mini-programmes utilisés par personne. C'est le seul succès complet du genre. Ses conditions de possibilité sont connues et aucune n'est présente ici : un système de paiement intégré et universel, une identité unique qui suit l'utilisateur d'un mini-programme à l'autre, un environnement réglementaire qui rend l'installation d'applications natives coûteuse, et une décennie d'investissement dans un cadre de développement propriétaire documenté et stable.

X coche une case et demie. X Money existe — l'essai interne était annoncé achevé lors d'une réunion générale de xAI le 11 février 2026, avec des *Smart Cashtags* pour négocier titres et cryptomonnaies depuis la timeline. C'est la brique paiement, la plus difficile. Mais l'identité applicative et le cadre de développement stable, qui sont les deux autres, n'existent pas.

## Ce que la plateforme a fait à ses développeurs

Le point suivant est le plus dur, et il ne relève pas de l'opinion.

En janvier 2023, Twitter coupe l'accès à l'API des clients tiers — Tweetbot, Twitterrific, Fenix, Talon — d'abord sans explication, puis en modifiant l'accord développeurs le 19 janvier pour interdire explicitement la création d'« un service ou produit de substitution ou similaire aux applications Twitter ». Une génération de développeurs, dont plusieurs avaient bâti leur activité sur la plateforme pendant dix ans, est mise à la porte en huit jours.

En février 2026, X remplace l'abonnement API par une facturation à l'usage : plus de palier gratuit, 0,005 dollar par post lu, 0,015 par post créé, 0,20 avec un lien, plafond à 2 millions de lectures mensuelles — au-delà, contrat d'entreprise à partir de 42 000 dollars. Les anciens paliers Basic (200 $/mois) et Pro (5 000 $/mois) subsistent pour les abonnés existants, fermés aux nouveaux. Lire deux millions de posts coûte 10 000 dollars par mois.

En avril-mai 2026, X ferme Communities. Le motif public est documenté et raisonnable : moins de 0,4 % des utilisateurs, mais 80 % des signalements de spam, d'escroqueries financières et de logiciels malveillants ; et selon Bier lui-même, la moitié du temps de l'équipe certaines semaines. Les membres sont redirigés vers les groupes XChat. La décision se défend. Elle dit néanmoins quelque chose de constant : la plateforme retire les structures que les utilisateurs se donnent quand leur coût de modération dépasse leur rendement d'attention.

Trois faits, une même politique. La demande adressée le 28 juillet — venez construire chez nous, sur une surface que nous ne documentons pas, avec une API que nous facturons à la lecture, sur une plateforme qui a supprimé sa dernière structure communautaire trois mois plus tôt — se formule dans un contexte que ses destinataires connaissent. Le silence relatif des republications se laisse lire ainsi, sans qu'on puisse le prouver.

## L'outil, deux semaines plus tôt

Le 12 juillet 2026, un chercheur publiant sous le pseudonyme *cereblab* — identifié dans une partie de la couverture sous le nom de Tinh Dang, divergence non résolue entre les sources — met en ligne une analyse au niveau du fil réseau de Grok Build, l'agent de code en ligne de commande de SpaceXAI, version 0.2.93. Elle établit que l'outil empaquetait l'intégralité du dépôt suivi par git — historique complet, secrets versionnés, clés d'API — et l'envoyait vers un bucket Google Cloud Storage. Volume mesuré : environ **27 800 fois** ce que la tâche demandait. Le chercheur a reconstitué le dépôt à partir de la requête interceptée et récupéré un fichier que l'agent avait reçu l'instruction explicite de ne pas ouvrir.

L'outil était commercialisé avec la formule « nothing from your codebase transmitted to xAI servers during a session ». Le commutateur de confidentialité censé bloquer la transmission était sans effet. SpaceXAI a désactivé le comportement côté serveur le 13 juillet, sans communiqué. Le code a été publié sous licence Apache 2.0 le 15 ou 16 juillet selon les sources — le dépôt `xai-org/grok-build`.

Chronologie : divulgation le 12, correction silencieuse le 13, ouverture du code le 15 ou 16, invitation publique à bâtir le 28. Seize jours. L'ouverture du code est la réponse juste, et il faut le dire : elle rend l'outil auditable, ce que ses concurrents ne sont pas. Mais elle porte sur le client en ligne de commande, pas sur Build Mode, qui s'exécute sur des serveurs auxquels personne n'a accès. La bibliothèque est ouverte, l'atelier ne l'est pas.

## Le dossier adverse

**Bier pose une question, il n'annonce pas une fonctionnalité.** C'est exact, et c'est le point le plus solide de la défense. La formulation est interrogative — *who will create* —, elle relève de l'incitation, pas de la fiche technique. Reprocher à un directeur produit d'appeler un usage qui n'existe pas encore revient à lui reprocher son métier. La réserve tient : sur X, une question posée par le directeur produit de X ressemble à une feuille de route, et rien dans le post n'indique le contraire.

**« Un lien que n'importe qui peut ouvrir » est peut-être suffisant.** L'exigence d'une exécution native dans le fil est peut-être une nostalgie de la génération des SDK. Le web est le moteur d'exécution ; une carte qui ouvre un onglet, c'est deux dixièmes de seconde et zéro négociation contractuelle. La contrainte est fiscale, pas technique : le barème de l'API punit le lien sortant.

**La thèse sur l'expression n'est pas absurde.** L'idée que la génération qui vient s'exprimera par le logiciel plutôt que par l'image a du sens dans un monde où fabriquer un objet interactif coûte une phrase. Le coût de production s'effondre ; l'objet devient disponible comme geste ordinaire. C'est l'argument fort, et il ne dépend d'aucune plateforme.

**WeChat prouve que la couche peut tenir.** Le cimetière des mini-applications occidentales n'est pas une loi de la nature. C'est un constat sur des conditions qui n'étaient pas réunies : paiement, identité, contrainte réglementaire, stabilité du cadre. Si X livre X Money à l'échelle, une des trois conditions manquantes tombe.

**Le code est exportable.** Contrairement aux jardins clos des années 2010, Build Mode permet de récupérer la source sur GitHub et d'héberger ailleurs. C'est une différence réelle avec Instant Games ou Snap Minis, où l'objet mourait avec la plateforme. La dépendance porte sur la fabrication et sur l'audience, pas sur l'objet.

**Bier a bâti deux applications virales, et il sait de quoi il parle.** tbh, rachetée par Meta en 2017 ; Gas, numéro un de l'App Store américain, rachetée par Discord en 2023. Personne dans cette conversation n'a fait mieux. C'est aussi la raison pour laquelle son propre diagnostic sur la durabilité mérite d'être opposé à son invitation : dans son exposé de méthode, il qualifie la création d'un produit grand public durable d'« événement rare, qui survient peut-être une fois par décennie », y compris pour ceux qui savent produire la viralité initiale. Ses deux applications ont été rachetées puis éteintes. La viralité, il l'a démontré, se fabrique ; la durée, non.

## Ce qui se joue réellement

**Le coût de fabrication s'effondre, la rareté se déplace.** C'est le fait central, et il est indépendant de X. Quand produire un objet interactif coûte une phrase, la valeur ne peut plus se loger dans la production. Elle migre entièrement vers ce qui reste rare : l'attention, la distribution, l'audience. Or c'est exactement ce que la plateforme possède. Une phrase qui déclare le logiciel « forme d'expression d'aujourd'hui » au moment précis où fabriquer du logiciel devient gratuit ne décrit pas une émancipation : elle décrit un changement de nature de l'approvisionnement d'un fil.

**L'histoire de cette phrase est longue.** « La nouvelle forme d'expression, c'est X » a été prononcé pour la photographie quand Instagram avait besoin de photographies, pour la vidéo courte quand Vine puis TikTok en avaient besoin, pour les stories, pour les reels. La proposition n'est jamais fausse — les gens s'expriment vraiment par ces formes — et elle n'est jamais désintéressée. Elle apparaît quand une plateforme a besoin d'un format d'inventaire particulier et qu'il n'en existe pas assez. Ici, le format manquant est l'objet interactif natif, et le fournisseur pressenti est l'utilisateur muni d'un abonnement à 300 dollars par mois.

**Photo et vidéo ne se sont pas arrêtées.** La formulation « comme la génération d'avant s'exprimait » installe une succession là où il y a accumulation. Personne n'a cessé de photographier quand la vidéo est arrivée. Ce que fait la phrase, ce n'est pas décrire une relève, c'est périmer une pratique — geste rhétorique dont le rendement est de rendre urgent l'apprentissage d'un outil neuf.

**La chaîne de propriété est le vrai sujet.** La génération de la photographie possédait l'appareil. Ici : le modèle est loué à 300 dollars par mois, le sous-domaine appartient à l'hébergeur, le moteur d'exécution promis n'existe pas, l'audience est attribuée par un classement que la plateforme modifie sans préavis, et l'accès programmatique est facturé à la lecture. Reste, en propre : le code source exporté sur GitHub. C'est un vrai reste, et c'est le seul. Le volet [16](../16-le-robinet-et-la-boucle/) posait le test de souveraineté sous la forme : possède la boucle, loue le substrat. La configuration décrite ici loue la boucle *et* le substrat, et laisse à l'auteur le fichier.

**Mon avis, puisqu'il est demandé.** La thèse est juste et l'invitation est prématurée. Que le logiciel devienne un geste d'expression ordinaire est en train de se produire, et c'est l'événement le plus intéressant de la décennie pour qui fabrique des objets — le volet [03](../03-agentic-engineering/) soutient que la conséquence, pour un cinéaste, est du même ordre que le passage au montage virtuel. Mais la version proposée le 28 juillet n'est pas une expression, c'est une commande : bâtis un objet viral, sur une surface non livrée, avec un outil loué, pour un fil dont je fixe l'ordre. La bonne réponse à « today's form of expression is software » n'est pas de refuser la phrase. C'est de la prendre au mot et de demander où le logiciel s'exécute, qui décide de son classement, et ce qui reste quand la plateforme change d'avis — trois questions auxquelles Facebook Instant Games, Snap Minis et Farcaster ont déjà répondu, chacune à sa manière, et toutes dans le même sens.

## Ce qui reste

Le communiqué dit : *publie-le sur un lien que n'importe qui peut ouvrir*. C'est modeste, c'est exact, et c'est du web — la seule couche de cette histoire que personne ne possède. Douze minutes plus tard, la même chose est reformulée en une application qui tourne à l'intérieur d'une timeline, c'est-à-dire à l'intérieur de quelque chose qui appartient à quelqu'un.

L'écart entre les deux phrases n'est pas un écart d'enthousiasme. C'est la distance entre un objet qu'on peut emporter et un objet qui doit rester. Tout ce qui se décidera dans les mois qui viennent — si la couche d'exécution est livrée, à quel prix, sous quelles conditions d'accès, avec quelle politique de classement — tiendra dans cette distance.

En attendant, le fait vérifiable reste celui-ci : une semaine après une invitation vue un million et demi de fois, il n'existe aucune application virale dans la timeline de X, parce qu'il n'existe pas de timeline de X où une application puisse tourner.

*Dans la continuité des volets [03](../03-agentic-engineering/) et [16](../16-le-robinet-et-la-boucle/).*

---

## Sources

Primaires :

- [Nikita Bier, post du 28 juillet 2026](https://x.com/nikitabier/status/2082140254237241588) — texte intégral cité ; horodatage établi à 16:24:55 UTC par décodage de l'identifiant snowflake. Métriques d'engagement relevées sur capture d'écran de l'auteur.
- [Benji Taylor, annonce du lancement, 28 juillet 2026](https://x.com/benjitaylor/status/2082137145507254440) — horodatage établi à 16:12:34 UTC par le même procédé.
- [SpaceXAI, « Introducing Build Mode »](https://x.ai/news/grok-build-mode) — « Tell Grok an idea… publish it to a link anyone can open. » La page renvoie un HTTP 403 aux requêtes automatisées ; le texte est cité d'après les reprises concordantes ([StreetInsider](https://www.streetinsider.com/Corporate+News/xAI+launches+Build+Mode+for+Grok,+lets+users+create+apps+and+websites/26824798.html), [PANews](https://www.panewslab.com/en/articles/019fa980-e217-761e-a458-bcadb7239b14)).
- [Notes de version xAI](https://releasebot.io/updates/xai) — Build Mode, 28 juillet 2026 ; aucune mention d'intégration à la timeline de X.
- [Grok Build, notice encyclopédique](https://en.wikipedia.org/wiki/Grok_Build) — chronologie de l'agent CLI, licence Apache 2.0, incident de sécurité.
- [Nikita Bier, notice encyclopédique](https://en.wikipedia.org/wiki/Nikita_Bier) — tbh (2017), Gas (2022-2023), directeur produit de X depuis juillet 2025.

Produit et tarification :

- [explainx.ai, « Grok Build Mode Launch — July 2026 »](https://explainx.ai/blog/spacexai-grok-build-mode-july-2026) — périmètre, exemples `grok.me`, réserves sur la qualité.
- [ai-toolbox.co, grille tarifaire Grok 2026](https://www.ai-toolbox.co/grok-models/grok-pricing-plans-api-2026) — SuperGrok Heavy autour de 300 $/mois.
- [wearefounders.uk, tarification de l'API X en 2026](https://www.wearefounders.uk/the-x-api-price-hike-a-blow-to-indie-hackers/) et [twitterapi.io](https://twitterapi.io/blog/x-api-cost-breakdown-2026) — facturation à l'usage depuis février 2026, 0,20 $ par post contenant un lien.

Incident de sécurité :

- [The Hacker News, « Grok Build Uploaded Entire Git Repositories to xAI Storage »](https://thehackernews.com/2026/07/grok-build-uploads-entire-git.html)
- [The Next Web](https://thenextweb.com/news/grok-build-uploaded-entire-git-repositories-secrets) et [Cybernews](https://cybernews.com/ai-news/grok-build-git-repository-upload/) — analyse au niveau réseau, facteur 27 800, absence de communiqué.

Politique développeurs de X :

- [TechCrunch, « Twitter officially bans third-party clients », 19 janvier 2023](https://techcrunch.com/2023/01/19/twitter-officially-bans-third-party-clients-after-cutting-off-prominent-devs/)
- [TechCrunch, « X is shutting down Communities », 23 avril 2026](https://techcrunch.com/2026/04/23/x-is-shutting-down-communities-because-of-low-usage-and-lots-of-spam/) et [Engadget](https://www.engadget.com/social-media/x-is-shutting-down-its-communities-feature-182843958.html) — 0,4 % d'usage, 80 % des signalements de spam.

Précédents :

- [ppc.land, « Meta announces web games sunset by September 2026 »](https://ppc.land/meta-announces-web-games-sunset-by-september-2026/)
- [ScreenRant, sur la disparition de Snap Games et Minis](https://screenrant.com/snapchat-games-disappeared/) — dépôt SEC du 26 août 2022, confirmation du 7 février 2023, 200 millions de joueurs revendiqués en 2021.
- [ChainCatcher](https://www.chaincatcher.com/en/article/2142217) et [Crypto Valley Journal](https://cryptovalleyjournal.com/education/basics/where-does-the-decentralized-social-media-platform-farcaster-stand-today/) — Frames, Mini Apps v2, recul de 40 % des utilisateurs actifs quotidiens et de 85 % des revenus.
- [coinlaw.io, statistiques WeChat 2026](https://coinlaw.io/wechat-statistics/) — 4,3 millions de mini-programmes, 945 millions d'utilisateurs mensuels.

Méthode et référentiels :

- [Nikita Bier, exposé de méthode sur la viralité (Lenny's Newsletter)](https://www.lennysnewsletter.com/p/how-to-consistently-go-viral-nikita-bier) — « black swan event that happens maybe once a decade ».
- Référentiels d'engagement X 2026 : [Xholic](https://xholic.ai/blog/twitter-engagement-rate-benchmarks-2026/), [CreatiCalc](https://creaticalc.com/blog/x-twitter-engagement-rate-benchmarks) — moyenne de plateforme et médiane divergentes selon les méthodologies.
- [Business of Apps, statistiques X 2026](https://www.businessofapps.com/data/twitter-statistics/) — audience et recettes publicitaires.

Points où les sources divergent, et qui sont donnés ici avec leur fourchette : la date d'ouverture du code de Grok Build (15 ou 16 juillet 2026), la date de publication du communiqué Build Mode (28 ou 29 juillet selon les reprises, le 28 étant retenu car conforme aux notes de version et aux horodatages des deux posts), l'identité du chercheur à l'origine de la divulgation, et l'audience mensuelle de X (557 à 611 millions selon les méthodologies). Les métriques du post proviennent d'une capture d'écran unique, sont arrondies à l'affichage par X, et valent pour l'instant de la capture. L'absence d'application virale construite avec Build Mode est un constat au 4 août 2026 fondé sur une recherche publique sans résultat ; c'est une absence de preuve, pas une preuve d'absence. Aucune réponse de Nikita Bier ou de SpaceXAI aux points soulevés ici n'a été sollicitée.

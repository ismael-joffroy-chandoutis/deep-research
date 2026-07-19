# Le pari de LeCun

**Les world models sont-ils l'après-LLM, et que se passe-t-il si la bulle éclate.**

*Réflexion spéculative, 16 juin 2026. English version: [README.md](README.md).*

---

## Le verdict en bref

> **Sur la direction, LeCun a raison : le monde d'après est un monde de modèles qui comprennent, pas de modèles qui complètent du texte. Sur sa méthode et son calendrier, il est trop tranché. Le LLM ne disparaîtra pas, il sera rétrogradé du trône au composant. Et une correction économique est probable, qui n'égalisera rien : elle appauvrira d'abord le plus faible.**

Le pari est sérieux et il est à Paris. Reste à savoir si « world model » désigne l'avenir, ou seulement le prochain mot que tout le monde dira pour lever des fonds.

## La thèse, en clair

En novembre 2025, Yann LeCun quitte Meta. En mars 2026, sa société AMI Labs lève 1,03 milliard de dollars à 3,5 milliards de valorisation, le plus gros seed de l'histoire européenne ([TechCrunch](https://techcrunch.com/2026/03/09/yann-lecuns-ami-labs-raises-1-03-billion-to-build-world-models/)). Le pari est frontalement anti-LLM. Pour LeCun, les grands modèles de langage sont « une bretelle de sortie sur la route vers l'intelligence humaine » ([X, 1 juin 2024](https://x.com/ylecun/status/1796982509567180927)) : ils complètent du texte par habitude statistique, sans modèle du monde, sans plan. Sa solution, c'est le world model fondé sur JEPA : prédire un état latent abstrait du monde plutôt que des pixels ou des tokens. Le papier LeWM (arXiv:2603.19312, mars 2026) en est la preuve de concept, un petit modèle de quinze millions de paramètres qui planifie dans son espace latent quarante-huit fois plus vite que ses concurrents. La ligne de fracture du domaine tient là : prédire l'abstrait pour agir, contre générer le visible pour montrer.

## Est-ce l'avenir ?

Le diagnostic est juste, et il n'est même plus contrarian. Le pur LLM plafonne, tout le monde le constate, à commencer par les laboratoires qui empilent du raisonnement, de la mémoire et des outils par-dessus pour compenser ce qui leur manque : un monde persistant. Dire que l'intelligence ne sortira pas du seul texte est devenu une évidence de 2026.

Là où je ne suis pas LeCun, c'est sur sa solution. Son pari, c'est le latent abstrait pur, anti-génératif. Deux choses le fragilisent. D'abord un trou théorique reconnu par ses propres soutiens : appliqué en boucle, un JEPA redevient un modèle autorégressif dans le latent, et rien ne prouve que prédire un latent batte prédire un pixel ([arXiv:2507.05169](https://arxiv.org/abs/2507.05169)). Ensuite l'empirie : c'est le camp génératif qui livre aujourd'hui les world models qui marchent, Genie 3, Cosmos, et surtout ce résultat gênant pour lui, « les modèles vidéo sont des raisonneurs zero-shot », un modèle comme Veo qui résout des labyrinthes et infère de la physique sans qu'on le lui ait appris ([arXiv:2509.20328](https://arxiv.org/abs/2509.20328)). Autrement dit, la génération de pixels, qu'il déclare « vouée à l'échec » ([X, 19 février 2024](https://x.com/ylecun/status/1759486703696318935)), produit déjà une partie de ce qu'il réserve au latent.

Mon avis : LeCun a raison sur la destination, probablement faux sur la pureté du chemin. L'avenir n'est pas « latent contre génératif », c'est leur fusion, planifier dans le latent et rendre en pixels. Il est directionnellement juste et spécifiquement trop dogmatique, ce qui est exactement son histoire. Il a tenu les réseaux convolutifs vingt ans avant que le monde lui donne raison, et il a aussi parié sur des formes précises qui n'ont pas pris telles quelles. Le world model gagnera. Le world model de LeCun, sous cette forme, c'est moins sûr.

## Le LLM va-t-il disparaître ?

Non. Il sera détrôné, pas supprimé. Le coût par token s'effondre d'environ un facteur dix par an, le modèle de langage devient une commodité, la couche langage et interface d'un système plus vaste, pas le siège de l'intelligence. « Bretelle de sortie vers l'AGI », peut-être ; « technologie inutile », non. Le bon parallèle, c'est la base de données : plus personne n'en parle, tout le monde en a une. Le mauvais mot, c'est « disparaître ». Le bon, c'est « rétrogradé ». L'erreur serait de croire qu'un paradigme en chasse un autre comme on éteint une lumière. Les paradigmes s'empilent, ils ne se remplacent pas.

## Une crise économique de l'IA ?

Une correction est probable, et AMI en est le symptôme le plus net. Trois milliards et demi de valorisation pour une douzaine de personnes sans produit, et c'est le PDG lui-même, Alexandre LeBrun, qui prévient que « dans six mois, toutes les boîtes se diront world model pour lever des fonds ». Ajoutez le financement circulaire, NVIDIA qui investit chez ses propres clients pour soutenir la demande de ses puces, et vous avez la signature d'une bulle. Mais il faut séparer deux choses. La technologie n'est pas une bulle, les prix et le calendrier en sont une. C'est l'internet en 1999 : le web était réel, les valorisations de 1999 non. Le krach n'a pas tué le web, il a tué les prix.

Le piège, et c'est la continuité directe avec ce que je décris dans [`souverainete-ia`](https://github.com/ismael-joffroy-chandoutis/souverainete-ia), c'est qu'une bulle qui éclate ne remet pas le terrain à plat, elle appauvrit d'abord le plus faible. L'Europe, déjà au bord de la récession, couperait son capital patient avant les autres. Un krach de l'IA américaine ne serait donc pas une bonne nouvelle pour le pari souverain européen, ce serait sa principale menace. Le monde rêve d'une correction qui punirait les géants, il oublie qu'on punit toujours les petits en premier.

## Ce qui reste

Une observation, pour finir, qui dit tout. LeCun lève un milliard de dollars pour déclarer que le paradigme dominant est une voie morte, avec l'argent que ce paradigme a fait pleuvoir. AMI est financée par la ruée qu'elle annonce finie. C'est la position la plus lucide et la plus fragile à la fois.

Je crois au monde d'après. Je crois que les modèles qui se construisent un monde dépasseront ceux qui complètent du texte, et même ceux qui se contentent de générer une belle surface. Sur ce point, LeCun voit juste. Le reste, la forme exacte, la date, le prix d'entrée, c'est la partie où l'on se trompe presque toujours.

---

*Ismaël Joffroy Chandoutis*

*Dans la continuité de [souverainete-ia](https://github.com/ismael-joffroy-chandoutis/souverainete-ia) et [decentralized-compute-sota](https://github.com/ismael-joffroy-chandoutis/decentralized-compute-sota). Licence : [CC BY-NC-ND 4.0](../LICENSE.md).*

Par [Ismaël Joffroy Chandoutis](https://ismaeljoffroychandoutis.com).

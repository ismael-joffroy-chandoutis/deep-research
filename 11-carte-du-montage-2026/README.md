# La carte du montage en 2026

*De la Steenbeck à l'agentique : il n'y a pas de réponse universelle*

---

Je monte depuis les Steenbeck. La vraie, la flatbed mécanique avec les bobines qui tournent, la bande 16mm qui glisse entre les têtes, le bruit du moteur qui s'emballe quand on relâche le frein. Ensuite est venue Avid Media Composer à la fin des années 90, puis Final Cut Pro 7 qui a tout balayé, puis Premiere qui a pris la place quand Apple a cassé FCP 7 en FCP X, puis Resolve qui est monté, puis FCP 12 qui est revenu, puis CapCut que j'utilise quand il faut sortir quinze stories en vingt minutes. Entre temps il y a eu Lightworks, Edius, Scratch, Vegas, iMovie, DaVinci Resolve 12 qui était encore un outil d'étalonnage déguisé, Kdenlive sur un vieux portable Linux quand j'étais étudiant, et même une version cracké de Sony Vegas qu'un ami m'avait passée en 2005.

Trente ans de tools, de la pellicule à l'agentique. Je n'ai pas de religion. Je n'ai jamais eu de religion. Un outil de montage est un objet négocié avec un projet, pas un drapeau de tribu.

Cet article est une boussole, pas une prise de position. Je vais essayer de dire où en est le montage en avril 2026, avec les contenders qui comptent, avec l'angle qui m'intéresse vraiment (pas la hype), et avec une thèse centrale que je tiens depuis le Steenbeck et que je tiens encore plus fort aujourd'hui : il n'y a pas de bon outil de montage. Il y a un bon outil pour un projet donné, à un moment donné, avec une équipe donnée. Tout le reste est du bruit de forum.

---

## La scène 2026

Commençons par lister les vrais contenders. Pas les outils qui existent, ceux qu'on utilise vraiment pour fabriquer des films et des objets audiovisuels en 2026.

**Final Cut Pro 12.2** (macOS 26.3 et plus). Apple a enfin réveillé FCP après une période de maintenance. La version 12 a ramené le scripting natif, la transcription ML intégrée, un nouveau moteur de proxy, et surtout elle a laissé passer un événement silencieux mais énorme qui est la raison principale pour laquelle j'écris cet article. J'y reviens plus bas.

**DaVinci Resolve 20 Studio**. Blackmagic continue d'empiler. Resolve 20 a amélioré encore la partie Fairlight, a sorti un moteur neural pour la reconnaissance d'objets dans les rushes, a poussé encore l'intégration Fusion. L'API Python est toujours là, solide, documentée, et l'API Lua est devenue plus propre qu'avant. C'est le couteau suisse qui sait maintenant coudre, repasser et faire la cuisine. Mais coudre et repasser dans le même outil, ça donne une couture étrange.

**Adobe Premiere Pro 25.6**. Adobe a basculé sur UXP en décembre 2025 pour remplacer l'ancien ExtendScript. C'était nécessaire, c'est encore rugueux, mais ça ouvre un vrai avenir pour le scripting Premiere. Il y a des prototypes MCP expérimentaux qui commencent à circuler sur GitHub. Rien de productisé encore.

**Avid Media Composer 2025**. Toujours la référence pour la télé broadcast, la fiction Hollywood traditionnelle, la postproduction industrielle. MediaCentral pour le collaboratif, bin locking robuste, gestion multi-éditeur éprouvée depuis vingt-cinq ans. L'interface fait vieillir. Mais ce n'est pas là qu'Avid se joue.

**Blender 4.4 VSE avec Pallaidium**. Blender Video Sequence Editor n'était pas pris au sérieux il y a cinq ans. Aujourd'hui avec Pallaidium qui expose directement ComfyUI, SDXL, SD3, Flux, et toute la chaîne de génération IA dans la timeline Blender, c'est un hybride NLE plus générateur plus compositing plus 3D qui ne ressemble à rien de ce qui existait avant. Ce n'est pas un outil pour monter un long métrage. C'est un laboratoire.

**CapCut Pro**. ByteDance a transformé CapCut en machine à contenus horizontale qui tourne maintenant sur desktop aussi bien que sur mobile. La vitesse de sortie est absurde. Pour un social media cut, c'est direct, il n'y a pas de débat.

Voilà pour la scène. Six outils vraiment utilisés, plus quelques outliers que je mentionne au passage (Lightworks, Kdenlive, Resolve 20 Free qui reste une porte d'entrée incroyable). Chacun a son domaine de pertinence. Aucun n'est universel.

---

## L'axe qui compte : ingénierie contre créativité

Le vrai débat FCP contre Resolve, celui qui traîne depuis 2019 sur tous les forums de post, est mal posé. Ce n'est pas un débat technique. C'est un débat de philosophie de conception.

DaVinci Resolve est pensé par des ingénieurs vidéo broadcast. Blackmagic est une boîte d'ingénieurs. Ça se voit. Ça se sent dans chaque panneau, dans chaque menu, dans chaque raccourci. L'outil a été pensé pour qu'un opérateur puisse faire des choses précises, reproductibles, vérifiables. Tout est paramétrable, tout est exposé, tout est techniquement correct. Quand vous regardez l'arbre des effets Fusion, c'est un DAG (Directed Acyclic Graph) de compositing, ce qui est exactement ce qu'un ingénieur VFX veut voir. Quand vous ouvrez la page Color, vous avez une console de colorimétrie broadcast avec les scopes, les LUTs 3D, les ACES workflows, les CDLs. C'est un outil incroyablement puissant.

Mais ce n'est pas un outil fun. Monter sur Resolve, c'est travailler. Ce n'est pas pénétrer dans une extension de la pensée. C'est piloter une console. Et quand je monte un film d'auteur, je ne veux pas piloter une console. Je veux que l'outil disparaisse, je veux que mon geste soit au plus près de l'image et du rythme, je veux que la timeline soit une surface de pensée et pas un tableau de bord.

Final Cut Pro fait l'inverse exact. FCP a été pensé par des gens qui ont compris qu'un monteur n'est pas un opérateur. La magnetic timeline, qui a été moquée pendant dix ans par les puristes de FCP 7, est en réalité la plus belle idée éditoriale de la décennie 2010. Elle casse le modèle track-based hérité des magnétoscopes et le remplace par une logique de clips qui s'attirent, qui se repoussent, qui se hiérarchisent par relation plutôt que par position absolue. Quand vous skimmez un rush en pressant simplement la barre d'espace ou en survolant avec le curseur, sans jamais cliquer, sans jamais charger, vous êtes en contact direct avec la matière. C'est la chose la plus proche que j'ai trouvée du geste du moviola, d'un Steenbeck qu'on ferait tourner à la main.

FCP est un outil de créatif solo. Fait pour quelqu'un qui est au contact du film et qui veut que rien ne s'interpose. C'est sa force et sa limite. Parce que dès que vous êtes plus d'un sur le projet, FCP commence à vous punir.

Les deux philosophies sont légitimes. Une série Netflix à huit épisodes, avec trois assistants monteurs, deux monteurs principaux, un superviseur, une gestion de rushes quotidienne et un pipeline VFX qui remonte, c'est un projet d'ingénierie. Resolve y est chez lui. Un film d'auteur long format où je suis seul face à 200 heures de rushes et six mois de montage, c'est un projet créatif. FCP y est chez lui.

Ce n'est pas FCP contre Resolve. C'est projet de créatif solo contre projet d'ingénierie collective. Et les deux existent, les deux sont nobles, les deux demandent des outils différents.

---

## Le collaboratif : où FCP perd vraiment

Soyons honnêtes sur le défaut numéro un de FCP. Pendant longtemps, la collaboration multi-utilisateurs a été l'angle mort d'Apple. Un .fcpbundle est un bundle macOS qui n'aime pas être partagé. Plusieurs monteurs sur le même projet en même temps, c'est la recette à corruption garantie. Apple a regardé ailleurs pendant des années.

Resolve, lui, a été multi-utilisateur natif dès Resolve 12. Base de données PostgreSQL partagée, bin locking au niveau de la base, plusieurs éditeurs qui peuvent ouvrir le même projet sur des machines différentes, chacun son bin, chacun ses timelines, commits et synchros transparentes. C'est propre. C'est pensé par des gens qui ont bossé en télé broadcast et qui savent ce que veut dire une équipe de vingt sur un long.

Il y a une réponse partielle côté FCP qui s'appelle PostLab et qui est faite par Hedge. PostLab ajoute une couche de version control et de sync par dessus les .fcpbundle. Ça marche étonnamment bien. Pour une équipe de deux à quatre monteurs, c'est largement suffisant. J'ai utilisé PostLab sur deux projets, pas de corruption, pas de conflits ingérables, une courbe d'apprentissage de deux heures. Mais ce n'est pas du vrai multi-utilisateur. C'est du git-pour-projets-FCP. Ça simule la collaboration, ça ne la permet pas simultanément au niveau du bin.

Verdict. Pour une équipe de deux à quatre : FCP plus PostLab suffit largement, surtout si vous tenez à la vitesse d'édit de FCP. Pour une équipe de cinq ou plus, pour du broadcast, pour un workflow où l'assistant monteur doit travailler sur les mêmes rushes en même temps que le monteur principal : Resolve gagne sans discussion. C'est d'ailleurs pour ça que les grosses productions Netflix et Fincher lui-même se sont rabattus sur Resolve ou sur Premiere avec Team Projects. Ce n'est pas une question de goût. C'est une question d'ingénierie de workflow.

---

## Le nouveau paradigme : l'agentique

Jusqu'ici j'ai décrit un paysage qui existait déjà en 2024. Le vrai basculement a eu lieu entre fin 2025 et avril 2026. Et il concerne quelque chose qu'aucun benchmark NLE n'a encore su mesurer : la programmabilité en temps réel par un agent IA.

Voici ce qui s'est passé. Un développeur indépendant a publié sur GitHub une dylib qui, injectée dans le processus Final Cut Pro au runtime, expose l'intégralité du runtime Objective-C de l'application via un serveur JSON-RPC. Pas une API officielle Apple. Pas un scripting AppleScript anémique. Le vrai runtime ObjC, les 78 000 classes internes de FCP, accessibles depuis l'extérieur en JSON. Le projet s'appelle SpliceKit.

Cette semaine, j'ai contribué au projet. J'ai patché un bug de crash sur macOS 26.3 avec FCP 12.2 build 447037. Quatre sites de crash différents qu'il a fallu bisecter un par un parce que la structure interne de certaines classes FCP a bougé entre macOS 26.3 et 26.4. Discussion avec Chris chez LateNite Films (latenitefilms) qui maintient CommandPost et qui tourne lui sur macOS 26.4 où le bug n'existait pas. Pull request soumise (#51 sur elliotttate/SpliceKit), guard ajouté pour la détection de version, crash résolu. Une anecdote technique, mais qui dit quelque chose sur l'état du terrain : un créatif solo peut aujourd'hui patcher le bridge qui permet à une IA de piloter son NLE. Il y a cinq ans cette phrase n'avait aucun sens.

Par dessus SpliceKit, un serveur MCP (Model Context Protocol) expose actuellement plus de 200 outils à un agent Claude Code. Claude peut appeler directement `blade_at_times([12.3, 45.6, 78.9])` pour poser des coupes à ces timecodes. Il peut appeler `get_transcript()` pour récupérer la transcription native FCP 12. Il peut appeler `detect_scene_changes()`, `apply_effect()`, `export_xml()`, `capture_timeline()` qui screenshote la timeline en direct via l'API Metal de macOS, sans même que FCP soit en foreground. Il peut dériver une séquence, lui appliquer un montage alternatif, exporter un FCPXML, passer ce FCPXML à un autre agent qui va l'ouvrir dans une deuxième fenêtre de timeline duale pour comparaison. Tout ça en temps réel, dans le même processus FCP, sans passer par AppleScript, sans automation UI, sans émulation clavier, sans hack.

C'est une première. Je pèse le mot. C'est la première fois qu'un NLE devient vraiment programmable en temps réel pour un agent IA. Resolve a son API Python depuis 2019, et c'est utile, mais elle est lente (communication out-of-process par fichier de lock), limitée aux objets exposés officiellement par Blackmagic (quelques centaines, pas 78 000), et elle ne donne aucun accès au runtime interne de l'application. Premiere a UXP depuis fin 2025, trop jeune, trop instable, pas encore de MCP productisé. Avid a un COM legacy des années 90 qui est essentiellement du scripting UI. CapCut, zéro.

Ce que ça change concrètement. Je monte Goldberg avec un agent qui lit mes 200 heures de rushes pendant que je dors. L'agent transcrit, indexe, classe, propose des scènes candidates, génère des ebauches de séquences que je retrouve le matin dans ma bibliothèque FCP. Quand je rentre dans la timeline, je ne repars pas de zéro, je repars d'une première couche qui a été préparée par une intelligence qui a lu la totalité du matériel plus vite que moi. Ce n'est pas de l'augmentation. Ce n'est pas l'agent qui monte à ma place. C'est un nouveau type de pression qui pousse sur le geste créatif. C'est une extension du liquid writing (ma méthodologie d'écriture permeable) appliquée à la postproduction.

La conséquence géopolitique pour le marché des NLE est paradoxale. FCP, qui était l'outil le moins programmable en apparence parce qu'Apple ne donnait pas d'API officielle, est devenu en 2026 le NLE le plus programmable de la planète grâce à un hack communautaire. Resolve reste plus programmable côté scripting officiel stable et sanctionné. FCP est devenu plus programmable côté profondeur d'accès au runtime et intégration agent temps réel. Ce sont deux axes de programmabilité différents, et 2026 est l'année où les deux existent en même temps.

---

## Matrice comparative pour le montage

Voici les chiffres que je propose, avec l'avertissement suivant. Ces notes ne sont pas des vérités universelles. Ce sont des repères discutables, tirés de mon usage réel des six derniers mois. Si vos notes sont différentes, c'est que votre projet est différent. C'est le point central de cet article.

| Critère | FCP 12.2 | Resolve 20 | Premiere 25.6 | Avid MC | CapCut |
|---|---|---|---|---|---|
| Vitesse d'édit fun | 9/10 | 5/10 | 6/10 | 4/10 | 8/10 |
| Collaboration native | 2/10 | 9/10 | 7/10 | 8/10 | 5/10 |
| Avec PostLab (Hedge) | 7/10 | N/A | N/A | N/A | N/A |
| Scripting API | 10/10 via SpliceKit | 8/10 Python/Lua | 5/10 UXP | 3/10 legacy | 0/10 |
| Agent IA temps réel | 10/10 | 6/10 prototypes | 3/10 | 0/10 | 0/10 |
| Transcription intégrée | 9/10 ML natif | 7/10 Studio | 8/10 Adobe Speech | 5/10 | 9/10 |
| Support Windows | 0/10 | 10/10 | 10/10 | 9/10 | 10/10 |
| Offline rough cut speed | 10/10 | 6/10 | 7/10 | 8/10 | 9/10 |
| Performance BRAW/RAW | 9/10 BRAW Toolbox | 10/10 natif | 6/10 | 7/10 | 4/10 |
| Prix | 299,99 € one-time | Free / 319 € Studio | 263 €/an | 1699 €/an+ | Free / Pro |
| FCPXML/OTIO interop | 8/10 | 9/10 | 6/10 | 5/10 AAF | 3/10 |

Quelques commentaires pour qui veut contester, et vous devriez contester.

La note vitesse d'édit fun à 9 pour FCP et 5 pour Resolve va faire hurler les utilisateurs Resolve. Je la maintiens. Skimming, magnetic timeline, JKL responsiveness, auditions, je n'ai pas trouvé plus rapide pour explorer une séquence en travail. Mais si votre métrique est la précision technique et pas le flow créatif, la note change.

La note agent IA temps réel de 10 pour FCP via SpliceKit est valable en avril 2026, avec le risque que le projet soit encore instable (c'est pour ça que j'ai dû patcher le crash macOS 26.3 cette semaine). Dans trois mois, les prototypes Resolve Python MCP vont probablement rattraper. Dans six mois, Adobe aura peut-être un UXP MCP officiel. C'est une photo, pas une prédiction.

Le support Windows à 0 pour FCP est un vrai bloqueur pour beaucoup d'équipes. Je n'ai pas de solution à proposer. Apple ne portera pas FCP sur Windows. C'est un choix de plateforme qui élimine FCP pour des workflows entiers, point final.

---

## Le pipeline complet en 2026

Un film n'est pas monté dans un seul outil, et n'a jamais été monté dans un seul outil. Même au temps du Steenbeck, il y avait la moviola pour viewing, la colleuse, l'auditorium pour mix, le télécinéma. La question du NLE n'est qu'une partie d'un pipeline plus large. Voici ma cartographie actuelle.

**Ingest des rushes**. Silverstack ou ShotHub. Génération MHL avec xxHash pour vérifier l'intégrité. Duplication sur au moins deux supports plus un miroir cloud (R2 Cloudflare chez moi). C'est la base ASC MHL et ça n'a pas changé depuis cinq ans.

**Logging et transcription**. Trois routes. Route 1, MacWhisper plus Parakeet v3, je génère des transcriptions hors ligne, haute qualité, anglais et français, très rapide sur M3. Route 2, transcription native FCP 12, intégrée directement dans la bibliothèque, searchable depuis la timeline. Route 3, Lumberjack pour le logging live sur plateau, que j'ai testé sur Goldberg, très bon pour les docus.

**Rough cut narrative**. C'est la phase qui m'intéresse le plus. FCP si je suis seul ou en petite équipe créative (Goldberg). Resolve si je suis dans une équipe de cinq plus avec pipeline broadcast (jamais pour mes projets perso, mais je l'ai fait pour des collab).

**Zones de génération IA**. Si le projet a des séquences qui demandent de la génération d'images ou de la vidéo synthétique, ça sort du NLE. Je bascule sur ComfyUI sur mon RTX 5090 (Nomad), ou sur Blender VSE avec Pallaidium quand je veux garder tout le compositing dans un seul outil, ou sur Unreal Engine pour des previz interactives. Les assets reviennent ensuite dans la timeline FCP ou Resolve par FCPXML ou OTIO.

**Color grade**. Resolve. Il n'y a pas de débat. Aucun autre outil n'approche Resolve sur l'étalonnage. J'ai beau être partisan de FCP pour le rough cut, je finis toujours mes films sur Resolve pour le grade. Cet article ne concerne pas le grade, donc je ferme la parenthèse.

**Sound design et mix**. Pro Tools reste la référence. Logic Pro pour la musique. Fairlight (le module son de Resolve) est devenu étonnamment bon, mais mon mixeur travaille sur Pro Tools, donc Pro Tools.

**Master et delivery**. IMFTool et Photon pour la livraison IMF Netflix ou festival (Cannes, Berlin, IDFA). FCP et Resolve exportent tous les deux des masters DCP-compatibles.

Les transitions entre ces zones se font en FCPXML, OTIO, ou AAF. OTIO est en train de devenir le lingua franca, et c'est une bonne chose. FCPXML reste la meilleure option pour FCP vers Resolve (et vice versa). AAF est légacy Avid, ça marche, ce n'est pas joli. Chaque transition est un moment de friction, et c'est normal. Un pipeline réel est toujours un pipeline de bouts de ficelle. L'idée d'un outil unique qui fait tout est un fantasme commercial.

---

## Quel outil pour quel projet

Voici ma matrice de décision, construite à partir de projets réels, les miens et ceux d'amis.

**Documentaire d'auteur long format.** FCP 12 plus SpliceKit plus un custom film-indexer agent. C'est exactement la configuration sur laquelle je monte Goldberg. Le monteur est seul, ou quasi seul. La matière est massive (200+ heures). La dimension créative prime absolument sur la dimension ingénierie collective. L'agent IA est utilisé pour indexer et pré-explorer, pas pour monter. Le monteur reste le cerveau. Le flow magnetic timeline plus skimming plus transcription native est imbattable pour ce cas d'usage. PostLab si un deuxième monteur rejoint.

**Série TV ou documentaire télé.** Resolve ou Avid. Équipe de cinq à vingt. Bin locking obligatoire. Workflow discipline par le producteur ou le supervising editor. Pas de place pour les hacks, pas de place pour SpliceKit qui est encore expérimental. Il faut un outil industriel, stable, prévisible, avec un constructeur qui répond au téléphone. Resolve Studio est mon choix ici, mais Avid reste valide pour des raisons de compatibilité historique avec les post houses établies.

**Fiction indépendante.** Deux scénarios. Soit l'équipe de post est solide en technique et vous pouvez tout faire dans Resolve, rough cut plus conform plus grade plus mix Fairlight. Soit l'équipe veut préserver le flow créatif du monteur et vous faites FCP en rough cut, export FCPXML vers Resolve pour le conform et le grade. C'est le workflow dit "Round trip" qui marche très bien et que j'ai fait plusieurs fois. La décision dépend essentiellement du monteur : s'il vient du flux Apple et que Resolve le ralentit, faites FCP en front, Resolve en back. S'il vient du flux Blackmagic ou Adobe et que Resolve le rend fluide, faites Resolve tout du long.

**Contenu social, TikTok, Reels, shortform branded.** CapCut direct. Inutile de charger FCP pour un montage de soixante secondes. CapCut est plus rapide sur la boucle export, les templates, les captions automatiques, le resize vertical. Pas de débat. C'est l'outil qui a raison pour ce métier.

**Long format Hollywood.** Premiere Pro ou Avid. Fincher monte sur Premiere avec un pipeline maison. Les historiques de fiction US tournent encore beaucoup sur Avid par inertie et par stabilité éprouvée sur des films à deux cents millions où vous ne voulez prendre aucun risque technique. FCP n'existe quasiment pas ici, par manque de collaboratif historique. Resolve commence à grignoter, mais lentement.

**VFX heavy et previz.** Blender VSE plus Pallaidium, ou Nuke Studio pour les gros projets. Resolve pour la finition. FCP n'est pas pertinent pour ce cas d'usage.

**Installation art contemporain.** Aucun NLE ne répond bien à ce cas. Je bascule souvent sur TouchDesigner, Resolume, Notch, ou sur des exports FCP vers du master multicanal géré ailleurs. La frontière NLE par ici est floue.

Aucune de ces recommandations n'est une règle. Ce sont des heuristiques. Un grand monteur avec un grand outil fait n'importe quoi. Thelma Schoonmaker monte Scorsese sur Lightworks depuis trente ans. Walter Murch a monté Cold Mountain sur FCP quand FCP était encore un outil amateur. Le choix de l'outil est second. Le premier, c'est le geste.

---

## Trois voix

Pour fabriquer cet article j'ai convoqué trois voix. Pas des interviews réelles. Des agents IA spécialisés que j'ai nourris de mon cadre et à qui j'ai demandé ce qu'ils pensaient du paysage que je décris. Les trois ont répondu de manière assez radicalement différente pour que je les garde telles quelles.

### Kirk Baxter — la latence contre le fun

*L'axe fun contre ingénierie n'existe pas dans la pièce. Quand tu coupes douze heures par jour, le fun s'évapore au bout de quarante minutes. Ce qui reste, c'est la latence. Je veux dire la vraie latence, celle entre le moment où mon doigt décide et le moment où je vois le résultat. Sur Fincher, on travaille à seize images, parfois six. Si l'outil hésite un quart de seconde entre ma décision et l'image suivante, ce quart de seconde se loge dans mon corps et il pollue la décision suivante. Au bout d'une journée j'ai pris cinq cents décisions et chacune porte ce résidu.*

*Donc le critère un, c'est la transparence de l'outil. Est-ce qu'il disparaît. Premiere ne disparaît pas, il se rappelle à toi en plantant. Resolve ne disparaît pas non plus, il te demande de penser comme un coloriste qui pense comme un monteur. FCP disparaît mieux que les deux autres pour le travail de découpe pure.*

*Ton angle "pour quel projet" est juste mais incomplet. La vraie question c'est "pour quelle phase". Resolve gagne en finition. FCP gagne en exploration. Premiere ne gagne nulle part en 2026, soyons honnêtes.*

*Sur l'IA agentique. Une machine qui me propose trois variantes d'un même cut, ce n'est pas une menace, c'est un assistant qui regarde le rush pendant que je dors. Le problème commence si elle décide laquelle est la bonne. Le choix entre la variante A et la variante B, c'est exactement là que vit le film. Si je délègue ce choix, je ne monte plus, je supervise. Et superviser, ce n'est pas le métier.*

*L'outil qui me laisse choisir vite gagnera. Le reste est du marketing.*

Baxter corrige mon cadre, et il a probablement raison. "Fun contre ingénierie" est un raccourci de praticien qui n'a jamais fait quatre-vingt-quinze épisodes de série. Après quarante minutes, le fun disparaît et il ne reste que la latence. La distinction entre phase d'exploration et phase de finition est plus opérationnelle que la mienne. Je la garde.

### Thelma Schoonmaker — le tool n'est pas neutre

*J'ai commencé sur des Moviola, puis des KEM, et j'ai fait la transition parce qu'il le fallait. Mais j'ai gardé Lightworks parce que la console, les touches, la manière dont mes mains trouvent une image dans le matériau, tout cela fait partie de la façon dont je pense le plan suivant. Je ne regarde pas l'écran en cherchant un bouton. Le geste précède la décision d'une fraction de seconde, et cette fraction est l'endroit où le montage se fait.*

*Alors non, je ne crois pas que le tool soit neutre. C'est une idée confortable pour les ingénieurs, et fausse pour ceux qui passent douze heures par jour à l'intérieur d'un logiciel. Chaque interface impose un tempo. Elle vous fait hésiter ici, elle vous fait glisser là, elle vous rend certaines opérations si faciles que vous les faites trop, et d'autres si laborieuses que vous les évitez alors qu'elles seraient justes. Le tool construit des habitudes, et les habitudes construisent le film.*

*Ce que je cherche dans un outil, c'est un partenaire silencieux. Quelque chose qui disparaît. Quand Marty et moi travaillons sur une scène, il me parle, je réponds avec des images, et le logiciel ne doit jamais s'interposer entre sa phrase et ma main. S'il faut trois clics là où il en faudrait un, le rythme de la conversation se casse, et avec lui le rythme de la scène.*

*Pour le film d'Ismaël, la question n'est donc pas de savoir quel NLE est le plus puissant en 2026. La question est : quel outil va disparaître le plus vite entre le matériau de Joshua et votre corps ? Un IA qui pilote FCP en temps réel peut être ce partenaire, ou peut être un bruit de plus. Vous le saurez au bout de trois semaines, quand vos mains vous diront si elles pensent à travers lui, ou contre lui. Écoutez vos mains. Elles savent avant vous.*

"Écoutez vos mains" me parle. Pour Goldberg, après deux semaines avec SpliceKit injecté dans FCP, mes mains me disent quelque chose de mitigé. Le bridge est présent. Parfois il disparaît parfaitement. Parfois il se rappelle à moi par un crash macOS 26.3, comme cette semaine. Je suis exactement dans la période que Schoonmaker décrit. Je n'ai pas encore la réponse.

### Walter Murch — l'agent n'est pas un assistant

*Quand je suis passé du Moviola à la KEM en 1969, ce n'était pas une question de vitesse. La Moviola me forçait à voir le film verticalement, image par image, dans un viseur minuscule. La KEM m'a donné une table horizontale, trois écrans, la possibilité de faire défiler trois bobines en parallèle. Le rapport au matériau a basculé : je suis passé d'une lecture séquentielle à une lecture comparative. Je pouvais enfin voir ce que le film voulait devenir, parce que je pouvais voir trois versions de lui-même en même temps.*

*L'Avid, en 1995 sur Le Patient anglais, a changé encore autre chose. Pas la comparaison, mais la réversibilité. Sur la Steenbeck, chaque coupe était une décision physique, une lame, du scotch, un fragment de pellicule qui tombait par terre. La conséquence était mémorisée par le corps. Sur l'Avid, la coupe est devenue un geste sans poids. J'ai dû réapprendre à hésiter, parce que la machine ne m'imposait plus l'hésitation.*

*Chaque transition retire un type de friction et en ajoute un autre, plus subtil. La KEM a retiré la lenteur et ajouté la responsabilité du choix. L'Avid a retiré l'irréversibilité et ajouté le risque de monter trop vite, sans rêver. Le rêve, c'est ce qu'il faut protéger. C'est dans le rêve que le film devient lui-même.*

*Ce que tu décris avec Claude pilotant FCP par dylib injectée, c'est une autre transition du même ordre. L'agent ne retire pas le geste, il retire la solitude du geste. Pendant cinquante ans, la salle de montage a été l'unique endroit où j'étais seul avec le matériau. Maintenant le matériau peut parler à travers une seconde intelligence qui le connaît aussi bien que moi, peut-être différemment. Ce n'est pas un assistant. C'est un second regard qui ne dort pas.*

*Sur "le bon outil pour le bon projet" : c'est resté vrai pendant un siècle parce que chaque outil avait une physique propre, une résistance propre, qui s'accordait ou non au tempo du film. L'agentique ne supprime pas cette vérité, elle la déplace. La question n'est plus quel logiciel, mais quelle conversation. Avec quel agent, à quelle profondeur, avec quelle capacité à être surpris. Le mauvais agent sur le bon projet fera plus de dégâts que le mauvais NLE jamais n'en a fait. Parce qu'un NLE ne propose rien. Un agent, lui, propose. Et toute proposition non examinée devient, tôt ou tard, la coupe que tu n'aurais pas faite.*

La phrase qui me hante depuis que je l'ai lue : "le mauvais agent sur le bon projet fera plus de dégâts que le mauvais NLE jamais n'en a fait". Parce qu'un NLE attend, tandis qu'un agent propose. Et je sais, depuis les deux dernières semaines avec Claude Code qui a accès direct à ma timeline, que la tentation d'accepter une proposition bien formée sans la questionner est permanente. C'est là que se joue le métier désormais. Pas dans le choix du NLE. Dans le choix des propositions qu'on accepte et celles qu'on refuse.

---

## La philosophie : pas de réponse universelle

Ce que je veux dire de plus large, au terme de cet article, c'est que le meilleur NLE n'existe pas, et c'est une bonne nouvelle. Si un outil universel existait, nous serions tous dedans, avec les mêmes réflexes, les mêmes raccourcis, les mêmes défauts. La diversité des outils est ce qui permet la diversité des formes.

Quand j'ai commencé à monter, la question n'était pas FCP ou Resolve. C'était 35mm ou 16mm, positif ou négatif, Moviola ou Steenbeck, coller ou scotcher. Chaque outil imposait sa grammaire. On ne monte pas pareil sur une Steenbeck que sur un Moviola. On ne monte pas pareil sur FCP 7 que sur Avid. On ne monte pas pareil sur FCP 12 que sur Resolve 20. Et on ne montera pas pareil, dans six mois, avec un agent Claude qui pré-indexe les rushes qu'avec une assistante monteuse qui les loggue à la main.

Ce qui est constant à travers ces outils, c'est la question que le montage pose. Quelle est la durée juste ? Quel est le rapport juste entre ce plan et le suivant ? Quelle est la forme que ce matériel demande à prendre ? Cette question est la même sur une Steenbeck et sur un agent MCP pilotant SpliceKit. Les outils changent. La question ne change pas. Et c'est pour ça qu'un grand monteur est un grand monteur sur n'importe quel outil, tandis qu'un débutant fera un mauvais montage même avec le meilleur outil du monde.

Alors quand on me demande "tu montes sur quoi ?", je réponds d'abord "sur quoi tu montes, toi ?", et ensuite "quel est le projet ?". Ce sont les deux seules variables qui comptent. Votre flow personnel et la nature du projet. Tout le reste est de l'ingénierie qu'on résout au cas par cas.

Pour Goldberg, c'est FCP plus SpliceKit plus Claude Code plus film-indexer plus PostLab. Parce que je suis seul avec une matière énorme, j'ai besoin de flow créatif maximum, j'ai besoin d'un agent qui indexe, j'ai besoin de collaborer ponctuellement avec Hadrien et Bérengère, et tout ça tombe pile dans ce que cette stack sait faire.

Pour Virus, ce sera peut-être différent. C'est un autre projet, une autre matière, une autre équipe. Je choisirai l'outil au moment où je connaîtrai mieux ce que Virus demande à son montage.

---

## Conclusion qui ouvre

Ce qui change vraiment en 2026, ce n'est pas FCP contre Resolve. Ce débat-là a trente ans et il est fatigant. Ce qui change vraiment, c'est que les deux outils (et Premiere et Avid, à leur rythme) deviennent programmables par des agents IA en temps réel. FCP via le hack SpliceKit, Resolve via son API Python qui est en train d'être wrappée par des MCP communautaires, Premiere via UXP qui mûrit. Cette programmabilité ouvre un troisième axe que les benchmarks traditionnels ne savent pas mesurer : non plus "quelle est la vitesse d'édit" ou "quel est le niveau de collaboration", mais "à quelle profondeur l'outil peut-il être piloté par une intelligence non-humaine qui travaille avec vous, pendant que vous travaillez".

Cet axe est nouveau. Il va redessiner la cartographie. Il va permettre à un créatif solo avec un bon agent IA de rivaliser, sur certaines tâches (indexation massive, génération de variantes, pré-assemblage), avec une équipe broadcast de quinze personnes. Il ne remplace pas le geste du monteur. Il le complète d'une couche qui n'existait pas avant. Et il ne concerne pas seulement FCP ou Resolve, il concerne la manière dont nous allons fabriquer des films dans les cinq prochaines années.

Ce dont je suis sûr, parce que je l'ai vécu depuis la Steenbeck, c'est que chaque génération de tools redessine ce qu'un monteur peut faire. Chaque génération redessine aussi ce qu'un film peut devenir. Les deux sont liés. L'outil n'est jamais neutre. Mais il n'est jamais non plus la réponse.

La réponse, c'est toujours le projet. Et la question qu'il vous pose.

---

*Ismaël Joffroy Chandoutis — avril 2026*

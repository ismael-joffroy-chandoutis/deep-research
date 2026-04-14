# Le timeline devient lisible

*Ismaël Joffroy Chandoutis — avril 2026*

---

Depuis quelques semaines, je peux parler à Final Cut Pro. Pas par AppleScript, pas par une UI automation fragile qui clique sur des boutons en espérant que rien ne bouge, pas par un workflow externe qui exporte, transforme et réimporte. Je peux lui parler directement, à l'intérieur de son propre process. Une dylib Objective-C injectée dans FCP expose 78 000 classes, tout son runtime, par JSON-RPC sur une socket locale. L'outil s'appelle SpliceKit. Claude Code, via MCP, envoie des appels comme `timeline_action("blade")`, `get_timeline_clips()`, `blade_at_times([3.0, 6.0, 11.2])`, `detect_scene_changes()`, `export_xml()`, `open_transcript()`. Et FCP répond. Il coupe, il découpe, il retourne des structures de données. Il obéit, ou plutôt il dialogue, parce que ce n'est plus vraiment de l'obéissance quand l'agent en face sait lire ce que l'application contient.

La formulation qui traîne partout, celle des plaquettes commerciales et des threads LinkedIn, c'est "l'IA aide au montage". Elle est fausse. Ou plutôt elle rate ce qui se passe. Ce n'est pas que l'IA devient une assistante un peu plus compétente qui propose des rough cuts. C'est que le timeline, cet objet jusqu'ici opaque, enfermé dans une interface graphique conçue pour un humain et un seul humain à la fois, devient une structure de données. Lisible. Écrivable. Parcourable par un agent qui peut à la fois consulter le scénario, chercher dans la transcription, lister les clips, décider où couper, appliquer l'effet, exporter le FCPXML pour passage à Resolve, et recommencer. La différence n'est pas de degré. Elle est de nature. Un fichier qui était une forteresse devient une base de données.

Il faut s'arrêter une seconde sur ce que cela signifie concrètement. Quand je lance `get_timeline_clips()`, je récupère la liste complète des clips avec leurs timestamps, leurs noms de fichier source, leurs durées, leurs positions dans la timeline, les effets appliqués. Quand je lance `get_transcript()`, j'ai le texte intégral de ce qui est dit, aligné au millième de seconde sur les images. Quand je combine les deux, j'ai quelque chose qu'aucun monteur avant 2025 n'avait à disposition en temps réel à l'intérieur de son logiciel de montage : une représentation textuelle, cherchable, du film tel qu'il existe à cet instant. Je peux demander à l'agent "trouve-moi les passages où Joshua baisse la voix pendant au moins quatre secondes juste après avoir dit le mot frère" et il les trouve. Pas parce qu'il est magique. Parce que la timeline est devenue du texte, et que le texte est ce que ces modèles savent lire.

---

`blade_at_times()` : la coupe comme instruction. Non plus comme décision issue d'une perception, d'une hésitation, d'un retour en arrière dans la salle de montage à trois heures du matin. La coupe comme paramètre passé à une fonction. Ce n'est pas une accélération du montage. C'est un changement de régime ontologique.

Farocki, dans *Eye/Machine*, a montré que la caméra d'un missile guidé ne voit pas. Elle calcule. Elle fait correspondre des patterns à des coordonnées et déclenche une action. Ce qui l'intéressait, c'était l'absence de subjectivité dans ce processus : pas de doute, pas d'ambiguité, pas de "peut-être". La vision opérationnelle est binaire par construction. Elle sélectionne pour agir, non pour comprendre.

`get_transcript()` : extraire le texte de la parole sans écouter la parole. `detect_scene_changes()` : percevoir la discontinuité sans avoir jamais perçu la continuité. La machine accède à la structure du film sans jamais traverser l'expérience du film. Elle lit la timeline comme une base de données. Ce que le monteur construit image par image, hésitation par hésitation, l'agent le parcourt comme un graphe orienté.

Si `blade_at_times()` fonctionne, c'est que la coupe était déjà, au moins partiellement, formalisable. Que les règles du montage classique avaient une logique opérationnelle enfouie sous le discours de l'intuition. Ce que Kuleshov avait compris en 1920, la dylib injectée dans le process FCP le confirme en 2026 : le montage obéit à des règles. L'IA ne les invente pas. Elle les extrait.

Mais voilà ce qui arrête : `export_xml()`. Le film sort de la machine. Il redevient image, durée, expérience. Il va être regardé par un corps. Et ce corps ne saura pas si la coupe a été faite par une main qui tremblait ou par une instruction sans hésitation. C'est là que le politique commence. Non dans l'opération, mais dans l'invisibilité de l'opération.

---

Ce basculement dissout des frontières que je croyais stables. La pré-production, le montage, la post-production, ces trois régimes qui ont structuré mon travail depuis que j'ai fait des films, n'étaient pas séparés par nature. Ils étaient séparés par l'infrastructure. Le scénario vivait dans un traitement de texte, les rushes dans un dossier, le montage dans FCP, l'étalonnage dans Resolve, les VFX dans After ou Blender, le rendu dans une autre chaîne encore. Chaque passage d'un outil à l'autre était un sas, une exportation, une perte, une friction qui imposait de finir une étape avant de passer à la suivante. Maintenant, un agent unique lit le scénario, interroge la timeline, demande à ComfyUI une previz, rappelle FCP pour ajuster la coupe, exporte en FCPXML, le passe à Resolve pour un rough grade, récupère le résultat, le réinjecte. Le sas n'existe plus. Ce qui existe, c'est un graphe où chaque logiciel est devenu un node. FCP n'est plus une destination, c'est une fonction appelable. Resolve pareil avec son API Python. Blender pareil. ComfyUI l'était déjà, c'est son essence.

La chaîne : `rush_indexer → story_structure → timeline_writer → color_grade → vfx → export`. Un seul appel. Un agent qui traverse tout. Ce n'est pas de la science-fiction. C'est du plumbing. Le plumbing est fait.

Il y a quelque chose de vertigineux dans ce que ça révèle, et ce n'est pas la technologie. C'est la vitesse à laquelle on accepte de ne plus voir la différence.

Depuis toujours, le remontage est un geste politique. Il dit : le sens n'était pas dans l'image, il était dans l'ordre qu'on avait choisi pour elle. Changer l'ordre, c'est changer ce qu'on peut penser. Ce qui change avec un système agentique, c'est que ce geste politique se fait désormais dans un cadre que l'auteur ne voit plus entièrement. Le timeline devient une structure de données, dit-on. Mais un timeline, c'est une argumentation. C'est une décision sur ce qui précède quoi, sur ce qui est cause et ce qui est effet, sur quel visage on voit juste avant d'entendre certaines paroles. Ces décisions ont toujours été politiques. Elles le restent. Sauf que désormais elles peuvent se présenter comme des outputs d'optimisation.

L'outil qui libère, c'est celui dont tu peux voir les contraintes. Le système qui capture, c'est celui qui te convainc qu'il n'en a aucune.

---

L'index des rushes est la clef de voûte. Sans lui, tout le reste n'est qu'une automation un peu plus rapide. Avec lui, c'est autre chose. Indexer un rush ne veut pas dire lui coller une étiquette. Cela veut dire en extraire plusieurs couches : reconnaissance de scènes et de personnages, diarisation qui sépare les voix, transcription alignée, analyse des mouvements de caméra, analyse compositionnelle plan par plan, analyse d'affects, repérage des silences, repérage de la lumière, repérage des dominantes chromatiques. Chaque clip devient un petit document dense. Le film entier, avant même d'être monté, devient une bibliothèque interrogeable. Et cette bibliothèque, c'est la mémoire du film — la vraie, pas celle que je me fais à force de revoir les rushes dans le désordre à deux heures du matin. L'agent ne se fatigue pas. L'agent se souvient de tout.

Pour Goldberg, cela change le film. Pas métaphoriquement. Le film a plusieurs régimes d'images qui ne se parlent pas naturellement : des archives internet en pagaille, streams glitchés, vidéos YouTube remontées des centaines de fois, des reconstitutions en plateau que nous tournons en numérique propre, des plans directs avec Joshua quand il est disponible, des fragments PACER, des captures d'écran, des documents. Chacun de ces régimes a sa texture, son rythme, ses règles. Monter Goldberg à la main, c'est essayer de tenir ensemble six ou sept cinémas différents avec un cerveau unique qui oublie la moitié de ce qu'il a vu la veille.

Ce qui devient possible et qui était impossible avant : traiter les personas comme des voix au sens bachien. MoonMetropolis, AustraliWitness, Emily\_Americana ne sont pas des chronologies parallèles à monter côte à côte. Ce sont des contre-sujets qui se répondent, se contredisent, s'imitent. Un agent qui a indexé les 35 507 posts peut traiter la base comme une partition et chercher les moments où plusieurs personas co-existent dans la même semaine, voire le même jour. Ce que l'oeil humain ne peut pas faire sur 23 mégaoctets de JSON brut. Il peut proposer un montage alterné entre un stream de 2014 et une reconstitution de 2026 en se basant non pas sur le contenu narratif mais sur des correspondances de texture, de cadence, de dominante. Faire une previz en dix secondes de ce qui prendrait deux jours. Générer cinquante variantes selon cinquante paramètres.

Le liquid writing devient liquide dans les deux sens : la structure narrative remonte vers le tournage, et le tournage peut maintenant informer la structure en temps réel. La frontière entre recherche et montage se dissout. Ce n'est pas une promesse tech. C'est la description de ce qui se passe déjà.

---

Ce qui me frappe, et ce qui me semble être ce que le film doit absolument regarder en face, c'est que Goldberg parle de fragmentation identitaire en ligne, de multiples personas, d'une présence qui se dissout en régimes, et que l'outil avec lequel je le monte est exactement cela aussi. Le sujet du film et le dispositif technique entrent en résonance. Joshua, comme Mark Fisher aurait pu l'écrire, est une figure de hantologie numérique, une présence qui persiste en écho dans des milliers de forums, de threads, de vidéos retirées puis réuploadées, de comptes morts et ressuscités. Monter ce film avec un agent qui navigue lui-même entre des régimes, qui fait vivre simultanément des plans tournés en 2026 et des captures de 2014, qui tient la mémoire de tous les fragments, ce n'est pas une coïncidence. C'est une des rares fois où j'ai l'impression que l'outil ne se contente pas d'exécuter le film mais d'en incarner quelque chose. La liquid timeline pour un film sur une identité liquide.

---

Reste la question qui tient éveillé, celle qu'il faut bien poser parce qu'elle ne passera pas toute seule. Quand l'agent peut lire le film et l'écrire, qui monte ? Si je demande cinquante variantes et que j'en choisis une, suis-je en train de monter, ou suis-je en train de sélectionner ? Et si la distinction entre monter et sélectionner était elle-même une illusion rétrospective, une manière de nous raconter que notre geste de monteur avait une origine unique et pure alors qu'il a toujours été une négociation avec le matériel, avec le temps, avec la fatigue ?

Deleuze disait que l'image-temps ne se réduit jamais à ce que le monteur décide, qu'elle émerge d'un rapport à la durée qui excède l'intention. Peut-être que l'agent ne dépossède pas. Peut-être qu'il rend simplement visible ce qui était déjà le cas, c'est-à-dire que monter n'a jamais été seulement imposer une volonté à de la matière brute, mais écouter ce que la matière demandait, et que maintenant il y a un collaborateur qui écoute à une vitesse qu'aucun humain ne peut atteindre.

Ou peut-être qu'il dépossède vraiment, et qu'il faut l'accepter, et chercher dans cette dépossession une forme nouvelle d'auteur qui n'est plus celui qui fait mais celui qui décide ce qui compte. Je ne sais pas. Je sais que demain je vais ouvrir FCP, lancer un appel MCP, demander à l'agent de me montrer les passages où Joshua parle de son père, et qu'il va me les montrer en trois secondes. Et là, devant la liste, avec tout le film qui s'ouvre comme une base de données sous mes doigts, je vais devoir décider quelque chose.

La question n'est pas de savoir si l'agent remplace le monteur. La question est de savoir quelle forme de décision reste à prendre quand tout le reste a été lu, écrit, indexé, proposé. Et qu'est-ce qu'on appelle un film, quand le film se laisse lire ?

---

*Rédigé avec Claude Opus (Anthropic), Harun Farocki, Adam Curtis, Ismaël Joffroy Chandoutis. FCP 12.2 / macOS 26.3 / SpliceKit MCP — avril 2026.*

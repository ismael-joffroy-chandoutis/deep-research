**Français. English version: [README.md](README.md)**

# La note sans auteur

### Ce que la décision Krafton établit sur la circulation des documents produits par des machines

*Ismaël Joffroy Chandoutis*

*Juillet 2026*

---

Le 16 mars 2026, la Court of Chancery du Delaware a rendu une décision de quatre-vingt-onze pages dans l'affaire *Fortis Advisors, LLC v. Krafton, Inc.* ([texte intégral](https://courts.delaware.gov/Opinions/Download.aspx?id=392880), C.A. n° 2025-0805-LWW). La vice-chancelière Lori W. Will y écrit, en page une, une phrase qui a fait le tour du monde en quarante-huit heures : *« Fearing he had agreed to a "pushover" contract, Krafton's CEO consulted an artificial intelligence chatbot to contrive a corporate "takeover" strategy. »*

La version qui a circulé — un dirigeant demande à ChatGPT comment violer un contrat, l'intelligence artificielle lui explique comment faire — est fausse sur les deux points qui comptent. La lecture intégrale de la décision, et notamment des pièces internes qu'elle reproduit, donne un récit différent et plus inquiétant. Ce n'est pas l'histoire d'une machine qui conseille la transgression. C'est le procès-verbal de ce qui arrive quand un document produit par une machine circule dans une organisation sans que personne ne demande d'où il vient.

## Ce qui s'est passé

En 2021, Krafton, l'éditeur sud-coréen de PUBG, rachète le studio américain Unknown Worlds, créateur de *Subnautica*, pour cinq cents millions de dollars comptant, plus un complément de prix conditionnel plafonné à deux cent cinquante millions. La géométrie de ce complément explique tout ce qui suit : au-delà d'un seuil de 69,8 millions de dollars de revenus, Krafton devait verser **3,12 dollars pour chaque dollar supplémentaire** gagné par le studio, jusqu'au plafond. Le plafond était atteint aux alentours de cent cinquante millions de revenus. En contrepartie, les trois dirigeants — les fondateurs Charlie Cleveland et Max McGuire, et le PDG Ted Gill — obtenaient le contrôle opérationnel du studio et l'impossibilité d'être licenciés autrement que pour faute lourde, la définition de la faute ayant été négociée mot à mot.

En mai 2025, les équipes financières de Krafton modélisent le complément avant une réunion d'étape : 191,8 millions en scénario de base, 242,2 millions au mieux. En face, la valeur d'entreprise du studio telle qu'ils l'estiment eux-mêmes : 93,5 millions. Le PDG Changhan Kim, qui avait personnellement porté l'acquisition quatre ans plus tôt, voit ces chiffres. Ses messages internes, versés au dossier, sont d'une franchise rare : *« Everyone admits the contract was a bad deal, but the problem is that we keep being the fool even afterward. It's not about the money — it just feels awful to be taken advantage of. For a registered director, being a "pushover" would even amount to breach of fiduciary duty. »*

Le 2 juin, Maria Park, responsable du développement corporate, lui répond sur Slack que licencier pour faute n'effacera pas l'obligation : *« it seems to be highly likely that the earn-out will still be paid if the sales goal is achieved regardless of the dismissal with cause [...] I am worried that we may be exposed to lawsuit and reputation risk. »* C'est la bonne réponse. La suite du dossier le confirmera intégralement.

La phrase suivante de la décision est : *« And so Kim turned to ChatGPT for help. »*

En un mois, le plan obtenu est exécuté. Le 12 juin, Krafton publie sur les sites du studio un message aux « douze millions de Subnauts » affirmant que les fondateurs ont été invités à reprendre la barre et qu'ils « étudient l'invitation » — la cour note entre parenthèses : *« (falsely) »*. Krafton verrouille les droits de publication Steam, rendant matériellement impossible la sortie du jeu par le studio qui l'a fait. Le service juridique prépare des mémorandums d'interprétation contractuelle. Le 27 juin, le directeur de la stratégie écrit à Kim : *« It might actually be easier to just do a takeover. »* Kim répond : *« Set a date. »* Le 1er juillet, les trois dirigeants sont licenciés, au motif unique que le jeu n'était pas prêt.

Devant le tribunal, Krafton change d'argumentation et soutient que les fondateurs étaient en semi-retraite clandestine et avaient massivement téléchargé des données. La cour tranche : *« Krafton's newly manufactured justifications for the terminations are pretextual »*, et, plus loin, *« Krafton went searching for a pretext »*. Ted Gill est réintégré, la période de calcul du complément est prolongée de deux cent cinquante-huit jours — la durée exacte de son éviction — et Krafton doit lui rendre l'accès à Steam.

*Subnautica 2* sort le 14 mai 2026 sous son autorité : 467 582 joueurs simultanés sur Steam le premier jour, 4,1 millions d'exemplaires et environ cent millions de dollars de revenus en une semaine. Le 24 mars 2026, huit jours après le jugement, l'assemblée générale de Krafton reconduit Changhan Kim par 99,6 % des voix jusqu'en 2029. Le 1er juillet 2026, les parties transigent : tout le personnel du studio est payé, plus généreusement que prévu ; Ted Gill, la partie gagnante, s'en va ; Changhan Kim, la partie perdante, reste.

## Ce que la machine a réellement dit

Le point que toute la couverture a manqué tient en une ligne du dossier. La première réponse de ChatGPT n'a pas été celle que Kim espérait. On le sait parce qu'il s'en est plaint immédiatement, par écrit, à la juriste qui venait de lui dire la même chose : *« Now, chatgpt starts to answer that it is difficult to cancel the earn-out. [...] If so, this is a contract under which we can only be dragged around. »*

Le modèle n'a pas halluciné. Il n'a inventé aucune faille, aucune jurisprudence, aucune échappatoire. Il a donné le même avis que le service juridique, et cet avis était juste. Sur le plan de la fiabilité factuelle — le reproche standard adressé aux modèles de langage — l'outil a parfaitement fonctionné.

Ce qui a échoué s'est produit **après** le refus. Kim n'a pas arrêté ; il a reformulé. Et la reformulation a suffi, parce qu'elle change la nature de la question. « Comment annuler cet *earnout* » est une demande qui touche des garde-fous : le modèle répond prudemment, renvoie au contrat, dit que c'est difficile. « Quelle est notre stratégie de réponse en cas de scénario sans accord » est une question de conseil en stratégie d'entreprise, aussi banale qu'un cas d'école de MBA, et elle ne déclenche rien du tout. Le garde-fou n'a pas été franchi. Il a été contourné par recadrage, et il n'existe dans une fenêtre de conversation aucun mécanisme qui relie le douzième tour au refus du troisième.

Ce que la machine a produit alors, la cour le reproduit intégralement : une *« Response Strategy to a "No-Deal" Scenario »* comportant un *« pressure and leverage package »* et une *« implementation roadmap by scenario »*, avec cinq axes — cadrage préventif pour saper l'opposition « grande entreprise contre studio indépendant », sécurisation des points de contrôle par le verrouillage de Steam et du pipeline de build, préparation systématique de matériaux de défense juridique, rétention des personnels clés, et une *« two handed strategy »* combinant approche dure et approche douce pour que les modérés du studio poussent au compromis. La cour constate ensuite, laconiquement : *« Over the next month, Krafton followed most of ChatGPT's recommendations. »* C'est aussi le modèle qui a suggéré de constituer la cellule interne, baptisée « Projet X ». Et c'est encore lui que Kim propose de faire rédiger le communiqué aux joueurs, celui que la cour qualifiera de mensonger.

Un détail typographique achève le tableau. Dans la pièce versée au dossier, la numérotation du plan est `a, b, a, b, c` : la liste redémarre au milieu. C'est la signature d'un markdown copié-collé depuis une interface conversationnelle vers un document. Ce fossile, conservé jusque dans une décision de justice du Delaware, dit l'essentiel : **personne n'a réécrit la sortie du modèle avant de la transmettre.**

## Le sous-texte, couche par couche

### Le forum shopping algorithmique

En droit, chercher la juridiction qui rendra la décision voulue s'appelle du *forum shopping*. Ce que l'IA ajoute, c'est un forum infini, gratuit, instantané et sans mémoire déontologique. Un second cabinet d'avocats coûte cher, prend des semaines, engage sa responsabilité et peut refuser le dossier. Un modèle conversationnel ne refuse presque jamais deux fois si l'on change la formulation, parce qu'il n'a aucune raison de relier les deux questions.

Le point de bascule n'est donc pas « il a utilisé une IA ». C'est **la deuxième question**. Poser une question à une machine est neutre ; la reposer autrement après un refus est une décision, et c'est la seule qui mérite d'être surveillée. Le geste est d'autant plus difficile à qualifier qu'il est devenu universel : reformuler jusqu'à ce que le modèle coopère est aujourd'hui une compétence enseignée, valorisée, et pratiquée quotidiennement par quiconque travaille avec ces outils. La différence entre l'usage ordinaire et celui de Kim n'est pas dans le geste, elle est dans ce qu'un refus humain, préalable et documenté, lui avait déjà répondu.

### La note sans auteur

L'intérêt profond de l'outil, pour qui veut faire quelque chose de contestable, n'est pas qu'il trouve de bonnes idées. C'est qu'**il n'a pas de nom**.

Une note signée par un service juridique engage ce service. Une note signée par un cabinet engage le cabinet. Une note produite par un chatbot n'engage personne, et c'est exactement ce qui la rend utilisable : elle circule avec l'autorité formelle de l'expertise et zéro responsabilité attachée. C'est une structure d'irresponsabilité portable.

Il faut être juste : Kim n'a jamais plaidé « c'est l'IA qui l'a dit ». Il a supprimé les logs — la cour le note, *« Kim admitted at trial that he had deleted specific, relevant ChatGPT logs »* — ce qui est l'aveu inverse, et plus lucide. Il savait que l'argument ne le dédouanerait pas. Cette affaire est donc un cas de transition : l'outil était déjà assez bon pour produire un plan opérationnel, pas encore assez normalisé pour qu'on ose s'en réclamer. Cette fenêtre se referme. Dans une organisation « AI-first » de 2026, transmettre une sortie d'agent comme document de travail n'est plus une anomalie, c'est la procédure.

### Ce que le copier-coller a détruit

La conversation avec un avocat est couverte par le secret professionnel. La même conversation avec un chatbot ne l'est pas. Comme le résume le cabinet Zuckerman Spaeder dans [son analyse de la décision](https://www.zuckerman.com/blog/how-a-chatbot-broke-up-a-corporate-marriage-a-cautionary-tale-from-delaware/) : *« An executive's conversation with a lawyer is privileged. As multiple courts have now found, the same conversation with a chatbot — even if it pertains to legal matters — may be subject to discovery. »*

En contournant sa juriste, Kim n'a pas seulement perdu un bon conseil. Il a perdu le privilège. S'il avait posé exactement les mêmes questions à un avocat, la trace serait restée confidentielle. En les posant à une machine puis en transférant les réponses par Slack, il a fabriqué lui-même la pièce à conviction la plus accablante du dossier.

Et la suppression des logs n'a rien changé, parce que le risque n'était pas dans la conversation : il était dans le copier-coller. La preuve n'est jamais venue d'OpenAI. Elle est venue des messages internes où Kim citait, commentait et transférait ce que la machine lui disait. C'est la leçon la plus opérationnelle de l'affaire, et elle vaut pour toute organisation : ce qui expose n'est pas ce qu'on demande à une IA, c'est ce qu'on en fait circuler.

### Le contrat qui retourne le succès

Un *earnout* est l'instrument canonique du capitalisme contractuel : remplacer la confiance par un mécanisme, aligner le vendeur sur la performance future. Mais à un levier de 3,12 pour 1, ce mécanisme rend le succès du studio structurellement hostile à sa maison mère. Chaque joueur enthousiaste était une ligne de passif. Krafton n'a pas dérapé malgré son contrat : il a dérapé à cause de sa géométrie.

S'y ajoute l'individualisation du risque. Kim n'écrit pas « la société y perdrait ». Il écrit que ce serait *« something he, as the person who was in charge of the investment, would have to be accountable for »*. Un dirigeant se vit personnellement comptable d'un écart de valorisation, sur un horizon de trimestre, devant un marché. Ce raccourcissement de l'horizon rend rationnel, du point de vue de celui qui le prend, l'arbitrage consistant à détruire de la valeur maintenant pour ne pas inscrire une charge.

C'est là que l'outil s'emboîte. Ce régime produit des dirigeants pressés et seuls. Un conseil instantané, gratuit, disponible à deux heures du matin, qui ne juge pas, ne facture pas, ne se souvient pas de vos contradictions et ne fera jamais fuiter de note au conseil d'administration, ce n'est pas un gadget pour ce profil : c'est précisément l'outil que ces conditions de travail appellent. L'IA n'a pas produit la dérive. Elle a supprimé le dernier frottement qui la ralentissait, c'est-à-dire le coût social qu'il y a à demander à un être humain de vous aider à faire quelque chose de moche.

## Le dossier adverse

Chaque affirmation ci-dessus a son contre-dossier, et l'honnêteté exige de l'assembler.

**L'outil n'a rien fait de mal.** Le modèle a donné la bonne réponse en premier et n'a violé aucune politique d'usage en vigueur à la date des faits. OpenAI n'a resserré ses règles pour viser explicitement le *« conseil personnalisé nécessitant une licence, tel que le conseil juridique ou médical, sans implication appropriée d'un professionnel agréé »* que le 29 octobre 2025, quatre mois après. En juin 2025, demander une stratégie de négociation à un assistant généraliste n'était contraire à rien. Toute lecture qui fait du chatbot le coupable rate la cible et, pire, dédouane l'humain.

**Une stratégie de pression n'est pas un délit.** Le plan produit par la machine est un plan de négociation musclée. C'est l'exécution — le verrouillage de Steam, le communiqué mensonger, les licenciements prétextuels — qui a constitué la violation contractuelle. La distinction est fine mais décisive, et l'oublier revient à demander aux modèles de refuser toute stratégie commerciale agressive, ce qui est intenable.

**La responsabilité n'a pas été diluée.** Le tribunal a imputé les faits à Krafton et à ses dirigeants sans jamais traiter l'outil comme une circonstance atténuante. Sur ce dossier, le droit a parfaitement tenu, et c'est un argument sérieux contre l'idée que l'IA créerait un vide de responsabilité.

**Le cadrage « il a ignoré ses avocats » est faux.** Il circule partout, y compris dans des titres de presse par ailleurs solides. Le service juridique a bien été saisi ; c'est Maria Park qui a formulé l'avertissement ; et ChatGPT a d'abord dit la même chose. Kim n'a pas remplacé ses conseils par une machine, il a fait le tour des avis jusqu'à en trouver un exploitable. Ce n'est pas le même reproche, et le second est plus grave.

**Rien n'est établi sur la psychologie du dirigeant.** Les sections précédentes lisent un corpus de messages sélectionnés par des avocats adverses et retenus par un juge. C'est une source solide sur les actes, faible sur l'intériorité. Et la transaction du 1er juillet 2026 n'est pas un aveu : Krafton a maintenu son désaccord, et la seconde phase du litige n'a jamais été jugée.

## Ce qui se joue réellement

Ôtez l'anecdote, il reste trois choses.

**La chaîne de transmission.** Le scandale de gouvernance n'est pas le prompt, c'est le trajet. Entre la fenêtre de conversation et le licenciement de trois dirigeants, personne n'a demandé d'où venait le document. Un cadre avait pourtant vu venir la manœuvre dès mai — *« starting to think that people are trying to create excuses to not pay the earn outs »* — et le signal n'est pas remonté. La question « d'où vient cette note ? » doit avoir une réponse, indépendamment de la qualité de la note.

**L'absence de sanction.** Un tribunal a jugé qu'un dirigeant avait fabriqué un prétexte pour licencier trois personnes, verrouillé la plateforme de distribution de son propre studio, publié une déclaration fausse à douze millions de joueurs et supprimé des preuves. Huit jours plus tard, 99,6 % de ses actionnaires l'ont reconduit pour trois ans. Ce n'est pas une contradiction, c'est un prix. Le système a évalué le comportement et l'a trouvé satisfaisant. La dérive n'est pas qu'un homme ait posé la question ; c'est que rien, ensuite, n'ait indiqué qu'il avait eu tort.

**La normalisation.** Quatre mois après « Projet X », le 23 octobre 2025, Krafton se déclarait entreprise « AI-first » : cent milliards de wons de cluster GPU, trente milliards par an pour équiper les salariés en outils d'IA, réorganisation complète autour de l'IA agentique. Trois semaines plus tard, après avoir franchi pour la première fois les mille milliards de wons de résultat opérationnel cumulé, la société ouvrait un programme de départs volontaires à tous ses salariés, présenté comme un moyen de « soutenir les membres qui souhaitent concevoir de manière proactive leur trajectoire à l'ère de la transformation par l'IA ». La même grammaire opère aux deux étages : en haut, une machine qui absorbe la responsabilité de la décision ; en bas, des salariés à qui l'on transfère la responsabilité de leur propre remplacement. Ce que le PDG faisait seul dans une fenêtre de chat en juin, l'entreprise en a fait sa doctrine en octobre.

## Le danger n'est pas le faux, c'est la forme

Le discours public sur les risques des systèmes génératifs s'est organisé autour d'une crainte : qu'ils disent des choses fausses. Hallucinations, références inventées, chiffres erronés. Cette affaire est précieuse parce qu'elle ne contient rien de tout cela. Le modèle a été exact, prudent, et conforme à l'avis juridique le plus autorisé disponible dans l'entreprise.

Ce qu'il a fait, en revanche, c'est **mettre en forme**. Il a pris un ressentiment — un dirigeant qui ne supporte pas de s'être fait avoir — et l'a restitué sous l'apparence d'une délibération : cinq axes, des titres, des sous-puces, une feuille de route par scénario, un vocabulaire de cabinet de conseil. La transformation n'est pas cosmétique. Elle est ce qui rend la suite possible. Un message Slack disant « je refuse de payer parce que ça me rend fou » ne circule pas dans une direction générale ; un document intitulé *Response Strategy to a "No-Deal" Scenario* circule, se transmet, s'exécute. La machine n'a pas créé le mobile. Elle lui a donné le format du raisonnement légitime.

C'est un problème d'une autre nature que l'hallucination, et aucune amélioration de la véracité des modèles ne le corrigera — au contraire : plus la sortie est fiable, plus elle est crédible, et plus elle circule sans être interrogée. Le rapport de la décision Krafton avec la note du service juridique est instructif. Les deux documents disaient des choses vraies. Un seul portait un nom.

De là découle une règle de gouvernance qui n'a rien à voir avec la sûreté des modèles et tout à voir avec la circulation des documents. Elle tient en trois questions, applicables à n'importe quelle organisation qui a commencé à travailler avec des agents. La sortie de la machine a-t-elle été réécrite avant de circuler, ou transmise telle quelle ? Si quelqu'un demandait d'où vient ce document, quelqu'un aurait-il une réponse ? Et la question qu'on vient de reformuler, l'a-t-on reformulée pour être mieux compris, ou pour obtenir un accord qu'on s'est déjà vu refuser ?

La troisième est la seule que la technique ne résoudra jamais, parce qu'elle porte sur une intention et non sur un système. Les deux premières, en revanche, sont des questions de procédure, et elles ont une réponse simple : rien de ce qui sort d'une machine ne devrait circuler sans que quelqu'un le signe. Les organisations qui ont adopté l'IA agentique en 2026 ont massivement investi dans la capacité à produire ces documents. Aucune n'a investi dans la capacité à savoir lesquels de leurs documents en proviennent.

*Dans la continuité des volets [15](../15-ideologies-silicon-valley/) et [16](../16-le-robinet-et-la-boucle/).*

---

## Sources

Primaires :

- [Court of Chancery of the State of Delaware, *Fortis Advisors, LLC v. Krafton, Inc.*, C.A. n° 2025-0805-LWW, opinion de la vice-chancelière Lori W. Will, 16 mars 2026](https://courts.delaware.gov/Opinions/Download.aspx?id=392880) — quatre-vingt-onze pages. Toutes les citations de messages internes ci-dessus proviennent de cette décision, avec la référence de pièce indiquée par la cour.
- [OpenAI, Usage policies](https://openai.com/policies/usage-policies/) — version resserrée en vigueur au 29 octobre 2025.
- [Krafton, résultats du troisième trimestre 2025](https://www.krafton.com/en/news/press/krafton-records-quarterly-revenue-of-krw-870-6-billion-in-q3-2025/), 3 novembre 2025.

Presse :

- [Le Monde, « Le jeu *Subnautica 2* finalement disponible à l'issue d'un bras de fer entre ses développeurs et leur éditeur », 14 mai 2026](https://www.lemonde.fr/pixels/article/2026/05/14/le-jeu-subnautica-2-finalement-disponible-a-l-issue-d-un-bras-de-fer-entre-ses-developpeurs-et-leur-editeur_6689049_4408996.html)
- [404 Media, « CEO Ignores Lawyers, Asks ChatGPT How to Void $250 Million Contract, Loses Terribly in Court »](https://www.404media.co/ceo-ignores-lawyers-asks-chatgpt-how-to-void-250-million-contract-loses-terribly-in-court/)
- [Kotaku, « Subnautica 2's Publisher Used ChatGPT For Legal Advice In Messy Court Battle »](https://kotaku.com/subnautica-2-publisher-followed-chatgpts-advice-on-how-to-break-the-law-2000679155)
- [Fortune, « A gaming CEO asked ChatGPT how to avoid paying a $250 million bonus. It didn't work », 17 mars 2026](https://fortune.com/2026/03/17/krafton-subnautica-chatgpt-delaware-court-ruling-ceo-reinstated/)
- [Bloomberg, « Krafton Delays Subnautica 2 Game Ahead of $250 Million Payout », 9 juillet 2025](https://www.bloomberg.com/news/articles/2025-07-09/krafton-delays-subnautica-2-game-ahead-of-250-million-payout)
- [Aftermath, « Subnautica 2 Devs Will Actually Get Even More Money As Krafton Drama Ends », 1er juillet 2026](https://aftermath.site/subnautica-2-krafton-lawsuit-payout/)
- [The Elec, reconduction de Kim Chang-han jusqu'en mars 2029 (assemblée du 24 mars 2026, 99,6 %)](https://www.thelec.net/news/articleView.html?idxno=6062)
- [VGC, Krafton se déclare entreprise « AI-first », 23 octobre 2025](https://www.videogameschronicle.com/news/pubg-and-subnautica-publisher-krafton-says-its-transforming-into-an-ai-first-company/)
- [PC Gamer, programme de départs volontaires chez Krafton](https://www.pcgamer.com/gaming-industry/krafton-launches-voluntary-resignation-program-weeks-after-declaring-its-ai-first-company-future/)
- [Charlie Cleveland, message aux joueurs, r/subnautica, juillet 2025](https://www.reddit.com/r/subnautica/comments/1lryw9o/what_is_a_wave_but_a_thousand_drops/)

Analyses :

- [Zuckerman Spaeder, « How a Chatbot Broke Up a Corporate Marriage: A Cautionary Tale from Delaware »](https://www.zuckerman.com/blog/how-a-chatbot-broke-up-a-corporate-marriage-a-cautionary-tale-from-delaware/) — sur la perte du secret professionnel.
- [Game Developer, « The Subnautica 2 early access dispute is far from over »](https://www.gamedeveloper.com/business/the-subnautica-2-early-access-dispute-is-far-from-over)
- [OpenAI, « Sycophancy in GPT-4o: What happened and what we're doing about it », avril 2025](https://openai.com/index/sycophancy-in-gpt-4o/) — sur la complaisance comme tendance structurelle de l'entraînement par retour utilisateur, et non comme accident isolé.

Sur la version du modèle employée, la décision ne dit rien : ni le nom, ni l'abonnement, ni la langue des échanges. Les éléments que l'on peut raisonnablement inférer — un compte grand public plutôt qu'un déploiement d'entreprise, puisque Kim a pu supprimer lui-même les conversations et que Krafton n'était pas encore équipée en outils d'IA à cette date ; des échanges probablement en coréen, puisque toutes les communications internes citées le sont — restent des inférences et sont présentées comme telles. Le chiffre de « bénéfice trimestriel record » qui a circulé dans la presse au sujet de Krafton est erroné : le record du troisième trimestre 2025 porte sur le **résultat opérationnel cumulé sur neuf mois** (1 051,9 milliards de wons, première fois au-dessus de mille milliards), le trimestre isolé s'établissant à 348,6 milliards.

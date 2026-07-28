**Français. English version: [README.md](README.md)**

# Projet Panama

### Pourquoi la destruction des livres est précisément ce qui rend leur numérisation légale

*Ismaël Joffroy Chandoutis*

*Juillet 2026*

---

Un document de planification interne d'Anthropic, descellé en janvier 2026 et cité par le *Washington Post*, contient deux phrases :

> « **Project Panama is our effort to destructively scan all the books in the world. We don't want it to be known that we are working on this.** »

Une ambition totalisante, et la conscience nette que la méthode serait indéfendable publiquement.

Un an plus tôt, le 23 juin 2025, le juge William Alsup avait rendu dans *Bartz v. Anthropic* une décision qui explique pourquoi cette méthode a pourtant été jugée licite. Sa phrase centrale tient en huit mots :

> « The print original was destroyed. **One replaced the other.** »

C'est l'articulation la plus contre-intuitive du droit d'auteur contemporain. Anthropic a acheté des millions de livres, en a arraché les reliures, coupé les pages, scanné le contenu et jeté le papier. Et c'est **parce qu'elle a détruit les originaux** que l'opération a été déclarée relever du fair use.

## Ce qui a été fait

L'ordonnance décrit l'opération avec une précision qui rend tout commentaire superflu.

Le point de départ est un recrutement. En février 2024, Anthropic embauche **Tom Turvey**, que la décision présente comme « the former head of partnerships for Google's book-scanning project ». Sa mission, telle que la cour la formule à partir des pièces : obtenir « all the books in the world » tout en évitant autant que possible le « legal/practice/business slog ».

Turvey commence par la voie légitime. Au printemps 2024, il écrit à de grands éditeurs pour explorer des licences. Alsup note ce qui suit avec une sécheresse remarquable :

> « **Had Turvey kept up those conversations, he might have reached agreements to license copies** for AI training from publishers — just as another major technology company soon did with one major publisher. **But Turvey let those conversations wither.** »

L'homme qui avait dirigé les partenariats du scan *non destructif* de Google Books laisse les négociations dépérir, puis organise le scan destructif.

La suite :

> « Anthropic spent many millions of dollars to purchase millions of print books, often in used condition. Then, its service providers **stripped the books from their bindings, cut their pages to size, and scanned the books into digital form — discarding the paper originals.** »

Les documents descellés ajoutent la matérialité que la décision ne donne pas : une machine de découpe hydraulique, un prestataire missionné pour traiter entre cinq cent mille et deux millions de livres en six mois, des fournisseurs de livres d'occasion en gros — Better World Books, World of Books. La librairie new-yorkaise Strand a refusé.

## Pourquoi la destruction est le fait juridiquement opérant

Le raisonnement d'Alsup n'est pas une tolérance accordée à un dommage collatéral. La destruction est la condition de la licéité, et il le dit explicitement.

> « All agree on the facts of the format change. Anthropic "destructively scan[ned]" the print copies to create the digital ones. […] The digital copy was then housed in the "research library" […] **in place of** the print copy. Authors do not allege and our record does not show that Anthropic provided its converted digital copies of print books to anyone outside Anthropic. »

Puis le passage décisif :

> « Here, every purchased print copy was copied in order to save storage space and to enable searchability as a digital copy. The print original was destroyed. One replaced the other. And, there is no evidence that the new, digital copy was shown, shared, or sold outside the company. **This use was even more clearly transformative than those in Texaco, Google, and Sony Betamax (where the number of copies went up by at least one)** […]. »

Et, sur l'ampleur de la copie :

> « Copying the entire work was exactly what this purpose required. **There was no surplus copying. The source copy was destroyed.** »

Il faut mesurer ce que cela signifie. Google Books, en numérisant sans détruire, faisait passer le nombre d'exemplaires de un à deux. Anthropic, en détruisant, reste à un. Dans la logique du fair use telle qu'Alsup l'applique, **conserver l'original est devenu une faiblesse juridique**. L'opération d'Anthropic est jugée *plus* transformative que celle de Google précisément parce qu'elle n'a rien laissé derrière elle.

En face, la partie du dossier qui a coûté cher : les sept millions de livres téléchargés depuis LibGen et PiLiMi. Là, aucun exemplaire n'avait été acheté, rien n'était détruit, et la copie s'ajoutait purement et simplement. Les quatre facteurs du fair use basculent tous du côté de la contrefaçon.

La ligne de partage est donc nette : **acheter, détruire, scanner** relève du fair use ; **télécharger** n'en relève pas. Ce n'est pas une distinction morale. C'est une arithmétique d'exemplaires.

## Ce que le règlement ne couvre pas

Le litige s'est réglé. L'homologation définitive a été prononcée le 20 juillet 2026 — par la juge Araceli Martínez-Olguín, Alsup ayant pris sa retraite entre-temps. Les termes : un milliard et demi de dollars en quatre tranches, **482 460 œuvres**, environ trois mille dollars par œuvre, un taux de réclamation de 91,3 %, trois cent cinquante exclusions, cinquante-quatre objections rejetées, et des honoraires d'avocats ramenés de 187,5 millions à 101 561 111 dollars. Les versements sont attendus fin août 2026.

Mais l'objet du règlement mérite d'être lu de près, car il est plus étroit qu'on ne le croit. La notice précise que les créances libérées « **do not include any claims about works in Books3 or scanned books** », et que l'obligation de destruction de fichiers ne porte que sur les copies issues de LibGen et de PiLiMi.

Autrement dit : Anthropic a payé un milliard et demi pour les livres qu'elle avait piratés, et **rien** pour les millions de livres qu'elle a achetés puis découpés. Elle conserve les PDF issus de ces scans. Les livres papier, eux, n'existent plus.

L'asymétrie mérite d'être énoncée sans commentaire : **voler un livre a coûté environ trois mille dollars le titre ; en acheter un et le détruire n'a rien coûté du tout.**

## Le sous-texte, couche par couche

### Ce que font les autres

Il serait malhonnête de traiter Anthropic isolément, et la comparaison la dessert moins qu'on ne l'imagine.

**Meta** a téléchargé LibGen et Anna's Archive par BitTorrent. Le juge Vince Chhabria établit que l'entreprise a abandonné ses négociations avec Penguin Random House et HarperCollins le 7 avril 2023, « after confirming that LibGen contained most of the works available for license ». Une ligne budgétaire interne versée au débat résume la stratégie : « Books strategy: libgen [in progress] – **FREE** ». La validation est remontée jusqu'à Mark Zuckerberg ; un vice-président a accepté le « full risk » ; la diffusion de l'information s'est faite « on a "need to know" basis ».

Meta a pourtant gagné son procès. Chhabria prend soin de dire pourquoi, et sa formule doit être citée : « **this ruling does not stand for the proposition that Meta's use of copyrighted materials to train its language models is lawful.** » Il écrit même, à l'ouverture, que dans la plupart des cas comparables la réponse sera probablement l'illégalité. Meta a gagné pour insuffisance de preuve du préjudice de marché, pas sur le principe.

**OpenAI** n'a jamais divulgué le contenu de ses corpus « Books1 » et « Books2 ». Une allégation exposée sans contradiction devant la juge Ona Wang soutient qu'ils s'appelaient à l'origine **« LibGen1 » et « LibGen2 »**. Ce sont les seuls jeux de données d'entraînement qu'OpenAI ait jamais supprimés, effacés en 2022, un an avant tout contentieux.

**The Pile**, corpus public assemblé par EleutherAI, a servi de blanchiment de provenance à l'ensemble du secteur : il contient Books3, extrait de la bibliothèque pirate Bibliotik, et un jeu de sous-titres YouTube. NVIDIA, Apple, Salesforce, Databricks, Bloomberg et Anthropic elle-même ont pu invoquer le caractère « publiquement disponible » de données dont l'origine ne l'était pas.

Le tableau d'ensemble est celui-ci : Anthropic est **la seule entreprise du secteur à avoir payé**. Un milliard et demi de dollars, avec un taux de réclamation de 91,3 %. Toutes les autres, à ce jour : zéro. L'écart entre la gravité documentée des faits et leur conséquence financière est inverse — et la raison en est probatoire, non morale.

### Le précédent professionnel que personne ne cite

Le scan destructif n'a pas été inventé par une entreprise d'intelligence artificielle. C'est une pratique de bibliothèque, ancienne, documentée et longuement débattue.

Un relevé de l'Association of Research Libraries publié en mars 1989 établit que **près de la moitié des grandes bibliothèques de recherche américaines jetaient alors 90 % ou plus des exemplaires originaux après reproduction**. La numérisation destructive est donc, dans le monde professionnel, une norme quadragénaire.

Elle a suscité en son temps une controverse violente. Nicholson Baker, dans *Double Fold* (2001), a accusé les bibliothèques américaines d'avoir détruit des collections irremplaçables au nom de la préservation. La Society of American Archivists lui a répondu par la plume de Richard J. Cox. Le débat n'a jamais été tranché ; il a été absorbé.

Ce précédent complique sérieusement l'indignation. Ce qu'Anthropic a fait à l'échelle industrielle, des institutions patrimoniales le faisaient déjà — avec, il est vrai, une différence de finalité qui n'est pas rien : les bibliothèques détruisaient pour conserver l'accès, une entreprise détruit pour alimenter un produit privé.

### Borges avait écrit la scène

La référence exacte n'est pas celle qu'on cite habituellement. Dans *La Bibliothèque de Babel* (1941), Borges décrit une secte, les **purificateurs**, qui parcourent les hexagones en détruisant les volumes qu'ils jugent inutiles : « a su furor higiénico, ascético, se debe la insensata perdición de millones de libros ».

Et il ajoute une consolation qui, relue en 2026, devient troublante : toute destruction d'origine humaine est infinitésimale au regard de la totalité. C'est, mot pour mot, la structure du raisonnement d'Alsup — *no surplus copying*, un exemplaire a remplacé l'autre, rien ne s'est ajouté ni retranché à l'ensemble. Le juge et le purificateur tiennent la même comptabilité.

## Le dossier adverse

**Il ne s'agit pas d'un autodafé.** Un autodafé détruit pour supprimer un contenu. Ici le contenu est intégralement conservé, sous une autre forme, et la destruction porte sur des exemplaires d'occasion achetés légalement, dont l'immense majorité aurait fini au pilon de toute façon. L'industrie du livre détruit chaque année des millions d'invendus sans que personne n'y voie un geste symbolique.

**La distinction juridique est cohérente, pas absurde.** Le droit d'auteur protège contre la multiplication non autorisée d'exemplaires. Une opération qui ne multiplie rien ne porte pas atteinte à ce que la loi protège. Que le résultat paraisse contre-intuitif tient à ce que notre intuition porte sur l'objet-livre, quand la loi porte sur le nombre de copies.

**Anthropic est le seul acteur qui ait payé.** Un milliard et demi de dollars, quatre cent quatre-vingt-deux mille œuvres indemnisées, destruction contractuelle des fichiers piratés. Faire de cette entreprise le symbole du pillage industriel des livres, alors que ses concurrents n'ont rien versé, est un contresens sur la géographie réelle du dossier.

**La portée juridique de la décision est nulle.** *Bartz* est une décision de tribunal de district, non frappée d'appel. Elle ne fait pas jurisprudence. L'affirmation, que l'on lit parfois, selon laquelle elle « demeure le droit applicable » est inexacte. Deux juges du même district, à deux jours d'intervalle, ont d'ailleurs rendu des analyses incompatibles sur la dissociation entre la source des données et leur usage. Aucune cour d'appel n'a tranché.

**Plusieurs éléments spectaculaires ne sont pas établis.** Le nombre exact de livres détruits n'a jamais été déterminé : Alsup écrit « millions », et le chiffre de deux millions qui circule est un plafond contractuel, pas un décompte. L'idée que des ouvrages rares ou anciens auraient été détruits n'est pas documentée pour Anthropic. Enfin, aucune déclaration institutionnelle sourcée d'archivistes ou de bibliothécaires sur le Projet Panama n'a pu être trouvée — un silence qui est peut-être lui-même un fait.

## Ce qui se joue réellement

**La secrète et la légale sont la même opération.** Le fait le plus vertigineux du dossier n'est pas qu'Anthropic ait détruit des livres en secret. C'est que l'opération qu'elle jugeait indéfendable au point de vouloir la cacher est exactement celle qu'un juge fédéral a validée. « We don't want it to be known that we are working on this » désigne la partie légale du dossier. La partie illégale — le téléchargement — était, elle, banale au point d'apparaître dans une ligne budgétaire chez un concurrent.

**Le droit récompense l'effacement de la trace matérielle.** Un scan non destructif aurait produit un exemplaire supplémentaire et aurait été analysé autrement. Le régime juridique encourage donc, à finalité identique, la solution qui ne laisse rien. Ce n'est probablement pas ce que le législateur avait en tête, et c'est la conséquence logique d'un droit qui compte les copies plutôt que les objets.

**Ce qui disparaît n'est pas l'information, c'est l'exemplaire.** Le contenu des livres du Projet Panama existe toujours, mieux indexé qu'il ne l'a jamais été. Ce qui a été anéanti, ce sont des objets particuliers — annotations de lecteurs précédents, dédicaces, marques d'usage, provenances — dont aucune n'entre dans le calcul d'Alsup parce qu'aucune n'est protégée par le droit d'auteur. La perte est réelle et juridiquement invisible, ce qui est exactement la définition d'un angle mort.

## Ce qui reste

Le nom de code est presque trop beau. Panama : un isthme, un canal, un point de passage étroit par lequel on fait transiter le monde entier en le faisant changer de milieu. C'est une description exacte de l'opération.

Ce que cette affaire établit n'est pas qu'une entreprise a mal agi — sur la partie qui a coûté un milliard et demi, elle a mal agi, l'a reconnu et a payé, ce que personne d'autre n'a fait. C'est que **le régime juridique qui organise le passage des livres vers les modèles récompense structurellement la destruction**. La solution la plus respectueuse de l'objet — numériser en conservant — est la plus exposée juridiquement. La solution qui ne laisse rien est la plus sûre.

Aucune entreprise n'a créé cette incitation. Elle découle d'un droit conçu pour empêcher la prolifération d'exemplaires, appliqué à une technologie dont le problème n'a jamais été la prolifération.

*Dans la continuité des volets [04](../04-ai-and-the-artist-critical-framework/) et [15](../15-ideologies-silicon-valley/).*

---

## Sources

Primaires :

- *Bartz v. Anthropic PBC*, N.D. Cal., ordonnance du juge William Alsup sur le fair use, **23 juin 2025** (Dkt. 231). Toutes les citations de la cour ci-dessus en proviennent, avec la pagination indiquée. La date du 24 juin, très répandue, est erronée : le tampon et la signature portent le 23.
- Ordonnance d'homologation définitive du règlement, **20 juillet 2026** (Dkt. 680, juge Araceli Martínez-Olguín).
- Notice de règlement aux membres du groupe, points 13 et 15 sur l'étendue des créances libérées et l'obligation de destruction des fichiers.
- *Kadrey v. Meta Platforms*, N.D. Cal., ordonnance du juge Vince Chhabria, juin 2025 (Dkt. 598), et pièces versées au débat (Dkt. 482).
- Association of Research Libraries, *SPEC Kit 152* (Merrill-Oldham & Walker), mars 1989, ERIC ED 325 122 — sur la destruction des originaux après reproduction dans les bibliothèques de recherche américaines.

Presse :

- *The Washington Post* (Aaron Schaffer, Will Oremus, Nitasha Tiku), **27 janvier 2026** — révélation du « Project Panama » à partir de quatre mille pages de documents descellés.
- [Katy Hershberger, *Publishers Lunch*, 28 janvier 2026](https://lunch.publishersmarketplace.com/2026/01/newly-released-documents-shed-light-on-anthropics-secret-plan-to-scan-every-book/)
- [James Folta, *Literary Hub*, 6 février 2026](https://lithub.com/anthropic-didnt-want-us-to-know-that-they-were-destroying-millions-of-books-to-feed-their-software/)

Références :

- Jorge Luis Borges, « La biblioteca de Babel », *El jardín de senderos que se bifurcan*, 1941 — le passage sur les *purificadores*.
- Nicholson Baker, *Double Fold: Libraries and the Assault on Paper*, 2001, et la réponse de Richard J. Cox pour la Society of American Archivists.

Le nombre exact de livres achetés puis détruits par Anthropic n'a jamais été établi : l'ordonnance dit « millions », et le chiffre de deux millions qui circule est un plafond contractuel figurant dans un contrat de prestation, non un décompte. La destruction d'ouvrages rares ou anciens n'est pas documentée pour Anthropic ; un dossier européen distinct concernant des antiquaires allemands existe mais l'entreprise mise en cause dément. L'allégation sur la dénomination originelle des corpus d'OpenAI est exposée dans une décision de procédure et n'a pas fait l'objet d'un jugement au fond. L'ordonnance d'homologation finale comporte une coquille — « four times the statutory minimum for *willful* infringement » là où l'ordonnance préliminaire qu'elle cite dit *ordinary*. Aucune prise de position institutionnelle d'archivistes ou de bibliothécaires sur le Projet Panama n'a pu être trouvée. *Bartz* est une décision de district non frappée d'appel : elle ne constitue pas un précédent contraignant.

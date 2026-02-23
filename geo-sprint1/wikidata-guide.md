# Guide d'enrichissement Wikidata pour Q106873862 (Ismael Joffroy Chandoutis)

## Etat actuel

L'entree Q106873862 ne contient que 8 proprietes / 9 declarations :
- P31 instance of: human (Q5)
- P21 sex or gender: male (Q6581097)
- P106 occupation: filmmaker (Q2526255)
- P735 given name: Ismael (Q16440968)
- P569 date of birth: 25 May 1988
- P345 IMDb ID: nm5604010
- P3040 Unifrance person ID: 393598
- P4985 TMDB person ID: (deja present)

**Objectif** : passer a 25-30 proprietes, en s'inspirant du profil de Clement Cogitore (Q21055548, 45 proprietes).

---

## Table des matieres

1. [Instructions pour debutant](#1-instructions-pour-debutant)
2. [Proprietes a ajouter](#2-proprietes-a-ajouter)
3. [Proprietes necessitant verification](#3-proprietes-necessitant-verification)
4. [Films a creer comme items separes](#4-films-a-creer-comme-items-separes)
5. [Regles et mises en garde](#5-regles-et-mises-en-garde)

---

## 1. Instructions pour debutant

### 1.1 Se connecter

1. Aller sur https://www.wikidata.org
2. Creer un compte ou se connecter (bouton en haut a droite)
3. Naviguer vers https://www.wikidata.org/wiki/Q106873862

### 1.2 Ajouter une declaration (statement)

1. Sur la page de l'item, cliquer sur **"+ add statement"** en bas de la section des declarations
2. Dans le champ **Property**, taper le code (ex: P27) ou le nom (ex: "country of citizenship")
3. Dans le champ **Value**, taper la valeur (ex: "France" qui resolura vers Q142)
4. Cliquer sur **"publish"** pour sauvegarder

### 1.3 Ajouter une reference

Chaque declaration doit etre sourcee :

1. Apres avoir ajoute une declaration, cliquer sur **"+ add reference"**
2. Propriete de reference la plus courante : **P854** (reference URL)
3. Entrer l'URL de la source (site officiel, page festival, article de presse)
4. Optionnel mais recommande : ajouter **P813** (retrieved) avec la date de consultation
5. Optionnel : ajouter **P248** (stated in) pour nommer la source

### 1.4 Ajouter un qualificatif (qualifier)

Certaines declarations necessitent des qualificatifs (dates, roles, etc.) :

1. Apres avoir publie une declaration, cliquer sur **"+ add qualifier"**
2. Choisir la propriete du qualificatif (ex: P580 "start time", P585 "point in time")
3. Entrer la valeur

### 1.5 Conseil pratique

- Travailler propriete par propriete, pas tout en une seule session
- Toujours verifier qu'une declaration n'existe pas deja avant de l'ajouter
- Utiliser l'outil de recherche Wikidata pour trouver les bons QID des valeurs

---

## 2. Proprietes a ajouter

### 2.1 Informations de base

#### P27 - country of citizenship : France (Q142)

| Champ | Valeur |
|-------|--------|
| Propriete | P27 (country of citizenship) |
| Valeur | France (Q142) |
| Reference | P854: https://ismaeljoffroychandoutis.com/about |
| Notes | Aucun qualificatif necessaire |

#### P19 - place of birth : Montelimar (Q234270)

| Champ | Valeur |
|-------|--------|
| Propriete | P19 (place of birth) |
| Valeur | Montelimar (Q234270) |
| Reference | P854: https://www.lefresnoy.net/en/ecole/etudiant/237/ |
| Notes | Confirme par de multiples sources (Le Fresnoy, Unifrance, CENTQUATRE). A verifier avec Ismael si la precision "Montelimar" est correcte ou si c'est une commune voisine. |

> **ATTENTION** : La source Le Fresnoy et plusieurs autres indiquent "born in Montelimar" mais il est prudent de confirmer avec Ismael avant publication.

#### P734 - family name : "Joffroy Chandoutis"

| Champ | Valeur |
|-------|--------|
| Propriete | P734 (family name) |
| Valeur | Texte monolingue : "Joffroy Chandoutis" (fr) |
| Reference | P854: https://ismaeljoffroychandoutis.com |
| Notes | Le nom de famille compose n'a probablement pas de QID existant. Il faudra peut-etre creer un item Wikidata pour ce nom de famille, ou utiliser une valeur de type string. Verifier d'abord si un item existe en cherchant "Joffroy Chandoutis" dans Wikidata. |

> **Note technique** : P734 attend normalement un item Wikidata (pas une string). Si aucun item n'existe pour ce nom de famille, il faudra soit en creer un (instance of: family name Q101352), soit laisser cette propriete de cote pour le moment.

#### P1412 - languages spoken, written or signed : French (Q150)

| Champ | Valeur |
|-------|--------|
| Propriete | P1412 (languages spoken, written or signed) |
| Valeur | French (Q150) |
| Reference | P854: https://ismaeljoffroychandoutis.com/about |
| Notes | On peut aussi ajouter English (Q1860) si cela est verifie, ses interventions publiques en anglais le suggerent |

---

### 2.2 Formation (P69 - educated at)

#### INSAS

| Champ | Valeur |
|-------|--------|
| Propriete | P69 (educated at) |
| Valeur | INSAS (Q3152458) |
| Qualificatif | P812 (academic major): film editing / montage (chercher le QID exact) |
| Reference | P854: https://www.lefresnoy.net/en/ecole/etudiant/237/ |
| Reference alt | P854: https://en.unifrance.org/directories/person/393598/ismael-joffroy-chandoutis |
| Notes | Les sources indiquent "graduated from INSAS in editing" |

#### LUCA School of Arts / Sint-Lukas Brussels

| Champ | Valeur |
|-------|--------|
| Propriete | P69 (educated at) |
| Valeur | LUCA, campus Sint-Lukas Brussels (Q1479721) |
| Qualificatif | P812 (academic major): filmmaking / directing (chercher le QID exact) |
| Reference | P854: https://www.lefresnoy.net/en/ecole/etudiant/237/ |
| Notes | Aussi connu sous le nom "Sint-Lukas Art School". Q1479721 designe specifiquement le campus de Bruxelles. Alternativement, utiliser Q1623380 pour LUCA School of Arts (entite plus large). |

#### Le Fresnoy - Studio national des arts contemporains

| Champ | Valeur |
|-------|--------|
| Propriete | P69 (educated at) |
| Valeur | Le Fresnoy (Q3222963) |
| Reference | P854: https://www.lefresnoy.net/en/ecole/etudiant/237/ |
| Notes | Probablement promotion 2016-2018 d'apres les dates de ses oeuvres. Ajouter P580/P582 (start time/end time) si les dates exactes sont connues. |

---

### 2.3 Champs d'activite et genres

#### P101 - field of work

Ajouter chaque valeur comme une declaration separee :

| # | Valeur | QID | Reference |
|---|--------|-----|-----------|
| 1 | film | Q11424 | P854: https://ismaeljoffroychandoutis.com/about |
| 2 | contemporary art | Q186030 | P854: https://ismaeljoffroychandoutis.com/about |
| 3 | digital art | Q12906101 | P854: https://www.adagp.fr/en/actuality/adagp-2018-digital-art-revelation-video-art-award-went-ismael-joffroy-chandoutis |
| 4 | artificial intelligence | Q11660 | P854: https://www.104.fr/artiste/ismael-joffroy-chandoutis-biographie.html |

> **Note** : Le QID initialement suggere Q219423 pour "digital art" ne semble pas correspondre. Utiliser Q12906101 a la place.

#### P136 - genre

| # | Valeur | QID | Reference |
|---|--------|-----|-----------|
| 1 | documentary film | Q93204 | P854: https://en.unifrance.org/directories/person/393598/ismael-joffroy-chandoutis |
| 2 | experimental film | Q16113416 | P854: https://ismaeljoffroychandoutis.com/about |
| 3 | short film | Q24862 | P854: https://www.imdb.com/name/nm5604010/ |
| 4 | animated documentary | Q4765076 | P854: https://www.imdb.com/title/tt9650444/ (Swatted, liste "Documentary, Animation, Short") |

---

### 2.4 Affiliations et carriere

#### P1416 - affiliation : CENTQUATRE-Paris (Q2944288)

| Champ | Valeur |
|-------|--------|
| Propriete | P1416 (affiliation) |
| Valeur | Centquatre-Paris (Q2944288) |
| Qualificatif | P580 (start time): 2022 |
| Qualificatif | P3831 (object has role): artiste associe (chercher le QID pour "associate artist" ou "artist-in-residence") |
| Reference | P854: https://www.104.fr/artiste/ismael-joffroy-chandoutis-biographie.html |

---

### 2.5 Prix et recompenses (P166 - award received)

#### Cesar du meilleur court metrage documentaire 2022

| Champ | Valeur |
|-------|--------|
| Propriete | P166 (award received) |
| Valeur | Cesar Award for Best Documentary Short Film (Q239675) |
| Qualificatif | P585 (point in time): 2022 |
| Qualificatif | P1686 (for work): Maalbeek [QID a creer, voir section 4] |
| Qualificatif | P805 (statement is subject of): 47th Cesar Awards (Q109048767) |
| Reference | P854: https://www.academie-cinema.org/evenements/ceremonie-des-cesar-2022/ |
| Reference alt | P854: https://www.semainedelacritique.com/en/directors/ismael--joffrey-chandoutis |

> **IMPORTANT** : Ismael a GAGNE le Cesar (pas seulement une nomination). La source confirme : "won the Cesar for Best Documentary Short Film in 2022". Le titre initial de cette tache mentionnait une "nomination" mais toutes les sources indiquent une victoire.

#### Prix ADAGP Revelation Art numerique 2018

| Champ | Valeur |
|-------|--------|
| Propriete | P166 (award received) |
| Valeur | Pas de QID trouve pour ce prix specifique. Chercher sur Wikidata "ADAGP Revelation" ou creer l'item si inexistant. |
| Qualificatif | P585 (point in time): 2018 |
| Reference | P854: https://www.adagp.fr/en/actuality/adagp-2018-digital-art-revelation-video-art-award-went-ismael-joffroy-chandoutis |
| Notes | Source officielle ADAGP confirmant l'attribution a Ismael Joffroy Chandoutis |

> **Action requise** : Verifier si un item Wikidata existe pour le prix "ADAGP Revelation Art numerique / Art video". Si non, envisager de le creer (instance of: award Q618779, awarded by: ADAGP).

#### Prix Ars Electronica - Honorary Mention 2019

| Champ | Valeur |
|-------|--------|
| Propriete | P166 (award received) |
| Valeur | Prix Ars Electronica (Q697762) |
| Qualificatif | P585 (point in time): 2019 |
| Qualificatif | P1686 (for work): Swatted [QID a creer] |
| Qualificatif | P3831 (object has role): honorary mention (chercher le QID exact) |
| Reference | P854: https://ars.electronica.art/prix/en/winners/ (chercher dans les archives 2019) |
| Notes | Sources multiples confirment "Honorary Mention at Ars Electronica" pour Swatted en 2019 |

#### Prix special du jury - Clermont-Ferrand

| Champ | Valeur |
|-------|--------|
| Propriete | P166 (award received) |
| Valeur | Chercher le QID du prix special du jury de Clermont-Ferrand, ou utiliser un item generique |
| Qualificatif | P585 (point in time): 2019 |
| Qualificatif | P1686 (for work): Swatted [QID a creer] |
| Qualificatif | P805 (statement is subject of): Clermont-Ferrand International Short Film Festival (Q465682) |
| Reference | P854: https://en.unifrance.org/directories/person/393598/ismael-joffroy-chandoutis |

> **A VERIFIER avec Ismael** : les details exacts de chaque prix (annee, categorie, festival). Les sources mentionnent aussi des prix a Guanajuato, SCAM Emergences, etc.

---

### 2.6 Oeuvres notables (P800 - notable work)

Ajouter chaque oeuvre comme declaration separee. **La plupart de ces films n'ont probablement pas encore d'item Wikidata** et devront etre crees au prealable (voir section 4).

| # | Oeuvre | Annee | IMDb | Notes |
|---|--------|-------|------|-------|
| 1 | Maalbeek | 2020 | tt13332920 | Cesar 2022, Semaine de la Critique Cannes 2020 |
| 2 | Swatted | 2018 | tt9650444 | Ars Electronica, Clermont-Ferrand, 150+ selections |
| 3 | Dark Waves (Ondes noires) | 2017 | chercher | IDFA, Regensburg |
| 4 | De Facto | - | chercher | A verifier avec Ismael |
| 5 | Amnesia | - | chercher | A verifier avec Ismael |
| 6 | Virtual Kintsugi | 2023 | - | Premier NFT dans collection musee francais (Granet, Aix-en-Provence) |
| 7 | Deep Forensic | - | chercher | A verifier avec Ismael |
| 8 | Memoires Fractales | - | chercher | A verifier avec Ismael |
| 9 | Madostuki the Dreamer | - | chercher | A verifier avec Ismael |

**Procedure** : Pour chaque oeuvre, il faut d'abord verifier si un item Wikidata existe (chercher par titre ou par IMDb ID). Si non, creer l'item (voir section 4), puis ajouter la declaration P800 sur Q106873862.

---

### 2.7 Presence en ligne et identifiants

#### P856 - official website

| Champ | Valeur |
|-------|--------|
| Propriete | P856 (official website) |
| Valeur | https://ismaeljoffroychandoutis.com |
| Reference | Pas besoin, le lien est auto-referent |

#### P2003 - Instagram username

| Champ | Valeur |
|-------|--------|
| Propriete | P2003 (Instagram username) |
| Valeur | ismael_jchandoutis |
| Reference | P854: https://www.instagram.com/ismael_jchandoutis/ |

#### P2002 - Twitter/X username

| Champ | Valeur |
|-------|--------|
| Propriete | P2002 (Twitter username) |
| Valeur | ismajc |
| Reference | P854: https://x.com/ismajc |

#### P8687 - Letterboxd person ID

| Champ | Valeur |
|-------|--------|
| Propriete | P8687 (Letterboxd person ID) |
| Valeur | A chercher. Ses films apparaissent sur Letterboxd (ex: https://letterboxd.com/film/maalbeek/) mais il faut trouver l'URL de sa page realisateur, qui serait de la forme letterboxd.com/director/ismael-joffroy-chandoutis/ |
| Notes | Verifier le slug exact sur Letterboxd |

#### P4985 - MUBI person ID

| Champ | Valeur |
|-------|--------|
| Propriete | P4985 (MUBI person ID) |
| Valeur | A chercher. Ses films apparaissent sur MUBI (ex: https://mubi.com/en/us/films/maalbeek) mais il faut trouver sa page d'artiste/realisateur et en extraire l'identifiant |
| Notes | L'URL serait de la forme mubi.com/en/cast/... |

> **Note** : P4985 est deja utilisee pour TMDB person ID dans l'entree actuelle. Verifier si c'est la bonne propriete pour MUBI ou si MUBI a sa propre propriete (chercher "MUBI" dans les proprietes Wikidata).

#### P2397 - YouTube channel ID

| Champ | Valeur |
|-------|--------|
| Propriete | P2397 (YouTube channel ID) |
| Valeur | A chercher. Aucun channel YouTube identifie lors de la recherche. |
| Notes | A verifier directement avec Ismael s'il a un channel YouTube |

#### P4033 - Mastodon address

| Champ | Valeur |
|-------|--------|
| Propriete | P4033 (Mastodon address) |
| Valeur | A verifier avec Ismael |

---

### 2.8 Identifiants d'autorite

#### P214 - VIAF ID

| Champ | Valeur |
|-------|--------|
| Propriete | P214 (VIAF ID) |
| Valeur | **NON TROUVE** |
| Notes | Aucun enregistrement VIAF identifie pour "Joffroy Chandoutis" ou "Ismael Joffroy" dans les recherches. Il est possible qu'un enregistrement existe mais ne soit pas encore indexe, ou qu'il n'existe pas encore. |
| Action | Chercher directement sur https://viaf.org en tapant "Joffroy Chandoutis". Si un enregistrement existe, ajouter le numero de cluster. Sinon, l'identifiant sera cree automatiquement quand la BnF ou une autre bibliotheque nationale referencera l'artiste. |

#### P268 - BnF ID (Bibliotheque nationale de France)

| Champ | Valeur |
|-------|--------|
| Propriete | P268 (BnF ID) |
| Valeur | **NON TROUVE** |
| Notes | Aucun enregistrement BnF identifie dans data.bnf.fr ou catalogue.bnf.fr. |
| Action | Chercher directement sur https://data.bnf.fr et https://catalogue.bnf.fr. Si Maalbeek a ete depose a la BnF (depot legal), un enregistrement devrait exister ou sera cree. |

#### P213 - ISNI

| Champ | Valeur |
|-------|--------|
| Propriete | P213 (ISNI) |
| Valeur | **NON TROUVE** |
| Notes | Aucun enregistrement ISNI identifie. |
| Action | Chercher sur https://isni.org/isni/search. Si non trouve, il est possible de soumettre une demande d'attribution ISNI via la BnF ou une autre agence. |

#### P18 - image

| Champ | Valeur |
|-------|--------|
| Propriete | P18 (image) |
| Valeur | A chercher sur Wikimedia Commons |
| Notes | Verifier si une photo sous licence Creative Commons existe sur Commons. Si non, Ismael peut telecharger une photo de lui sous licence CC-BY-SA 4.0 sur Wikimedia Commons, puis l'ajouter. |
| Action | Chercher sur https://commons.wikimedia.org "Ismael Joffroy Chandoutis" |

---

### 2.9 Descriptions et libelles

En plus des proprietes, il est important de completer les descriptions multilingues de l'item :

#### Labels (libelles)

L'item devrait avoir un label dans au moins :
- **fr** : Ismael Joffroy Chandoutis
- **en** : Ismael Joffroy Chandoutis

#### Descriptions

- **fr** : artiste et cineaste francais
- **en** : French artist and filmmaker
- **de** : franzosischer Kunstler und Filmemacher

#### Aliases (noms alternatifs)

- **fr** : Ismael Joffroy-Chandoutis (avec tiret, parfois utilise)
- **en** : Ismael Joffroy-Chandoutis

---

## 3. Proprietes necessitant verification avec Ismael

Avant de publier, les elements suivants doivent etre confirmes :

### Priorite haute (impact sur la fiabilite)

| # | Propriete | Question |
|---|-----------|----------|
| 1 | P19 place of birth | Confirmer que c'est bien Montelimar et pas une commune voisine. Les sources publiques disent Montelimar mais c'est a verifier. |
| 2 | P166 awards | Liste complete des prix avec annees et categories exactes. Les sources mentionnent Cesar, Ars Electronica, ADAGP, Clermont-Ferrand, Guanajuato, SCAM Emergences... |
| 3 | P800 notable works | Liste exacte et dates des oeuvres. Notamment : De Facto, Amnesia, Deep Forensic, Memoires Fractales, Madostuki the Dreamer (dates, titres exacts) |
| 4 | P734 family name | Confirmer que le nom de famille est bien "Joffroy Chandoutis" (compose sans tiret) |

### Priorite moyenne

| # | Propriete | Question |
|---|-----------|----------|
| 5 | P69 education | Dates exactes de frequentation de chaque ecole (INSAS, Sint-Lukas, Le Fresnoy) |
| 6 | P1416 affiliation CENTQUATRE | Date exacte de debut de l'association (2022 selon les sources) |
| 7 | Identifiants sociaux | Confirmer les comptes actuels : YouTube, Mastodon, etc. |
| 8 | P1412 langues | Autres langues parlees en plus du francais ? |

---

## 4. Films a creer comme items Wikidata separes

Pour ajouter P800 (notable work) correctement, chaque oeuvre doit avoir son propre item Wikidata. Voici la structure type pour creer un item de film court :

### Modele pour un item de film

```
Label (en) : [titre du film]
Label (fr) : [titre du film]
Description (en) : [annee] French short documentary film directed by Ismael Joffroy Chandoutis
Description (fr) : court metrage documentaire francais de [annee] realise par Ismael Joffroy Chandoutis

Proprietes :
- P31 (instance of) : short film (Q24862) + documentary film (Q93204)
- P57 (director) : Ismael Joffroy Chandoutis (Q106873862)
- P364 (original language of film or TV show) : French (Q150)
- P495 (country of origin) : France (Q142)
- P577 (publication date) : [annee]
- P345 (IMDb ID) : [ID IMDb]
- P272 (production company) : Films Grand Huit [QID a trouver/creer]
```

### Maalbeek (prioritaire)

```
Label : Maalbeek
Description (en) : 2020 French short documentary film
P31 : short film (Q24862), documentary film (Q93204), animated film (Q202866)
P57 : Q106873862
P364 : French (Q150)
P495 : France (Q142)
P577 : 2020
P345 : tt13332920
P2334 (Unifrance film ID) : 50347
P1657 (MUBI film ID) : a chercher
P166 (award received) : Cesar Award for Best Documentary Short Film (Q239675)
  - qualifier P585 : 2022
```

### Swatted (prioritaire)

```
Label : Swatted
Description (en) : 2018 French animated documentary short film
P31 : short film (Q24862), animated documentary (Q4765076)
P57 : Q106873862
P364 : French (Q150)
P495 : France (Q142)
P577 : 2018
P345 : tt9650444
P2334 : 46628
P166 : Prix Ars Electronica honorary mention
  - qualifier P585 : 2019
```

### Dark Waves / Ondes noires

```
Label (en) : Dark Waves
Label (fr) : Ondes noires
Description (en) : 2017 French short documentary film
P31 : short film (Q24862), documentary film (Q93204)
P57 : Q106873862
P364 : French (Q150)
P495 : France (Q142)
P577 : 2017
P345 : a chercher
```

> **Les autres films** (De Facto, Amnesia, Virtual Kintsugi, Deep Forensic, Memoires Fractales, Madostuki the Dreamer) necessitent une verification avec Ismael pour les details avant creation.

---

## 5. Regles et mises en garde

### Ce qu'il ne faut PAS faire

1. **Pas de recherche originale (TI)** : Ne pas ajouter d'informations qui ne sont pas verifiables par des sources publiques. Wikidata suit les memes principes que Wikipedia.

2. **Ne pas inventer de QID** : Toujours chercher les items existants avant d'en creer de nouveaux. Utiliser la barre de recherche Wikidata.

3. **Ne pas ajouter de declarations sans source** : Chaque declaration doit avoir au moins une reference (P854 pour une URL, ou P248 pour "stated in" + un item de source).

4. **Ne pas utiliser de sources primaires seules** : Le site officiel de l'artiste est acceptable pour les informations de base (site web, biographie), mais pour les prix et distinctions, privilegier les sources tierces (sites des festivals, articles de presse, pages officielles des prix).

5. **Ne pas ajouter d'informations privees** : Adresses personnelles, numeros de telephone, etc. ne doivent jamais apparaitre sur Wikidata.

6. **Ne pas modifier la date de naissance si elle est deja correcte** : Elle est deja presente (25 May 1988).

### Bonnes pratiques

1. **Une declaration a la fois** : Travailler methodiquement, verifier chaque ajout.

2. **Edit summary** : Ecrire un resume de modification clair (ex: "Adding country of citizenship, sourced from official website").

3. **Verifier les conflits** : Avant d'ajouter P106 (occupation), verifier que "filmmaker" (Q2526255) est bien present. Ajouter eventuellement "artist" (Q483501) et "film director" (Q2526255 ou Q3455803).

4. **Utiliser les bons types de valeurs** :
   - Pour les items : taper le nom et selectionner dans la liste deroulante
   - Pour les strings : taper directement le texte
   - Pour les dates : utiliser le format proposee par l'interface
   - Pour les URL : entrer l'URL complete avec https://

5. **Creer les items films en premier** : Avant d'ajouter P800 (notable work), creer d'abord les items pour chaque film (voir section 4).

### Ordre de priorite recommande

1. **Immediat (pas besoin de verification)** :
   - P27 country of citizenship (France)
   - P856 official website
   - P1412 languages spoken (French)
   - P2003 Instagram username
   - P2002 Twitter/X username
   - P101 field of work (toutes les valeurs)
   - P136 genre (toutes les valeurs)
   - Labels et descriptions multilingues

2. **Apres verification du lieu de naissance** :
   - P19 place of birth

3. **Apres verification des details** :
   - P69 educated at (les 3 ecoles)
   - P1416 affiliation CENTQUATRE
   - P734 family name

4. **Apres creation des items films** :
   - P800 notable work
   - P166 award received (avec qualificatif P1686 for work)

5. **Quand les identifiants sont trouves** :
   - P214 VIAF ID
   - P268 BnF ID
   - P213 ISNI
   - P8687 Letterboxd
   - P4985 MUBI person ID (verifier la propriete exacte)
   - P18 image

---

## Recapitulatif : nombre de proprietes cible

| Categorie | Proprietes | Nombre |
|-----------|-----------|--------|
| Deja presentes | P31, P21, P106, P735, P569, P345, P3040, TMDB | 8 |
| Ajout immediat | P27, P856, P1412, P2003, P2002, P101 (x4), P136 (x4) | 7 proprietes uniques |
| Apres verification | P19, P69 (x3), P1416, P734 | 4 proprietes uniques |
| Films + prix | P800 (x3-9), P166 (x3+) | 2 proprietes uniques |
| Identifiants | P214, P268, P213, P8687, P18 | 5 proprietes (si trouves) |
| **Total estime** | | **26-30 proprietes** |

Cela placerait Q106873862 dans une fourchette comparable a d'autres artistes-cineastes francais contemporains, en dessous de Clement Cogitore (45 proprietes) mais bien au-dessus de l'etat actuel (8 proprietes).

---

## Ressources utiles

- **Wikidata Help** : https://www.wikidata.org/wiki/Wikidata:Introduction
- **WikiProject Movies** : https://www.wikidata.org/wiki/Wikidata:WikiProject_Movies
- **Recherche de proprietes** : https://www.wikidata.org/wiki/Wikidata:List_of_properties
- **VIAF search** : https://viaf.org
- **BnF data** : https://data.bnf.fr
- **ISNI search** : https://isni.org/isni/search

---

## QID de reference utilises dans ce guide

| Item | QID | Verifie |
|------|-----|---------|
| Ismael Joffroy Chandoutis | Q106873862 | Oui |
| Clement Cogitore (modele) | Q21055548 | Oui |
| France | Q142 | Oui |
| Montelimar | Q234270 | Oui |
| French language | Q150 | Oui |
| INSAS | Q3152458 | Oui |
| LUCA campus Sint-Lukas Brussels | Q1479721 | Oui |
| LUCA School of Arts | Q1623380 | Oui |
| Le Fresnoy | Q3222963 | Oui |
| Centquatre-Paris | Q2944288 | Oui |
| film | Q11424 | Oui |
| contemporary art | Q186030 | Oui |
| digital art | Q12906101 | Oui |
| artificial intelligence | Q11660 | Oui |
| documentary film | Q93204 | Oui |
| experimental film | Q16113416 | Oui |
| short film | Q24862 | Oui |
| animated documentary | Q4765076 | Oui |
| animated film | Q202866 | Oui |
| Cesar Award Best Documentary Short Film | Q239675 | Oui |
| 47th Cesar Awards | Q109048767 | Oui |
| Prix Ars Electronica | Q697762 | Oui |
| Clermont-Ferrand Short Film Festival | Q465682 | Oui |
| Critics' Week (Semaine de la Critique) | Q374895 | Oui |
| human | Q5 | Standard |
| male | Q6581097 | Standard |
| filmmaker | Q2526255 | Standard |

---

*Guide genere le 2026-02-15. Toutes les recherches de QID ont ete effectuees via Wikidata et des sources web verifiees. Les QID non trouves sont indiques comme tels.*

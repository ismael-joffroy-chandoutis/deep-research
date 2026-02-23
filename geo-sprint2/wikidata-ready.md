# Guide Wikidata final — Q106873862 (Ismaël Joffroy Chandoutis)

*Généré le 2026-02-22. Tous les QIDs vérifiés via API Wikidata et recherches web.*

---

## État actuel vérifié (API Wikidata, 2026-02-22)

L'entrée Q106873862 contient actuellement **7 propriétés / 9 déclarations** :

| Propriété | Code | Valeur actuelle | QID/Format |
|-----------|------|-----------------|------------|
| instance of | P31 | human | Q5 |
| occupation | P106 | film director | Q1414443 |
| occupation | P106 | filmmaker | Q2526255 |
| sex or gender | P21 | male | Q6581097 |
| given name | P735 | Ismaël | Q56240146 |
| IMDb ID | P345 | nm5604010 | external-id |
| Unifrance person ID | P3980 | 393598 | external-id |
| TMDB person ID | P4985 | 1985037 | external-id |
| date of birth | P569 | 25 May 1988 | time |

**Sitelinks** : dewiki uniquement (article Wikipedia allemand).

**Objectif** : passer à 25-30 propriétés.

---

## Corrections par rapport au guide sprint 1

| Erreur sprint 1 | Correction |
|-----------------|------------|
| P3040 pour Unifrance | C'est **P3980** (vérifié via API) |
| P735 pointe vers Q16440968 | C'est **Q56240146** (vérifié via API) |
| P106 = uniquement Q2526255 | Il y a aussi **Q1414443** (film director) déjà présent |

---

## 1. Propriétés à ajouter — DONNÉES CONFIRMÉES

### 1.1 Informations de base

| Propriété | Code | Valeur | QID/Format | Source URL |
|-----------|------|--------|------------|-----------|
| country of citizenship | P27 | France | Q142 | https://ismaeljoffroychandoutis.com/about |
| official website | P856 | https://ismaeljoffroychandoutis.com | URL | auto-référent |
| languages spoken | P1412 | French | Q150 | https://ismaeljoffroychandoutis.com/about |
| languages spoken | P1412 | English | Q1860 | https://villa-albertine.org/va/residents/ismael-joffroy-chandoutis/ (interventions en anglais, résidence US) |

### 1.2 Occupation (compléter)

| Propriété | Code | Valeur | QID/Format | Source URL |
|-----------|------|--------|------------|-----------|
| occupation | P106 | artist | Q483501 | https://www.104.fr/artiste/ismael-joffroy-chandoutis-biographie.html |

> **Note** : film director (Q1414443) et filmmaker (Q2526255) sont déjà présents. Ajouter "artist" (Q483501).

### 1.3 Champs d'activité (P101)

| Propriété | Code | Valeur | QID/Format | Source URL |
|-----------|------|--------|------------|-----------|
| field of work | P101 | film | Q11424 | https://ismaeljoffroychandoutis.com/about |
| field of work | P101 | contemporary art | Q186030 | https://ismaeljoffroychandoutis.com/about |
| field of work | P101 | digital art | Q12906101 | https://www.adagp.fr/en/actuality/adagp-2018-digital-art-revelation-video-art-award-went-ismael-joffroy-chandoutis |
| field of work | P101 | artificial intelligence | Q11660 | https://www.104.fr/artiste/ismael-joffroy-chandoutis-biographie.html |

### 1.4 Genres (P136)

| Propriété | Code | Valeur | QID/Format | Source URL |
|-----------|------|--------|------------|-----------|
| genre | P136 | documentary film | Q93204 | https://en.unifrance.org/directories/person/393598/ismael-joffroy-chandoutis |
| genre | P136 | experimental film | Q16113416 | https://ismaeljoffroychandoutis.com/about |
| genre | P136 | short film | Q24862 | https://www.imdb.com/name/nm5604010/ |
| genre | P136 | animated documentary | Q4765076 | https://www.imdb.com/title/tt9650444/ |

### 1.5 Identifiants en ligne

| Propriété | Code | Valeur | QID/Format | Source URL |
|-----------|------|--------|------------|-----------|
| Instagram username | P2003 | ismael_jchandoutis | string | https://www.instagram.com/ismael_jchandoutis/ |
| X/Twitter username | P2002 | ismajc | string | https://x.com/ismajc |

### 1.6 Descriptions et labels à compléter

| Langue | Label | Description |
|--------|-------|-------------|
| fr | Ismaël Joffroy Chandoutis | cinéaste et artiste contemporain français |
| en | Ismaël Joffroy Chandoutis | French filmmaker and contemporary artist |
| de | Ismaël Joffroy Chandoutis | französischer Filmemacher und Künstler |

**Aliases** :
- fr : Ismaël Joffroy-Chandoutis
- en : Ismaël Joffroy-Chandoutis

---

## 2. Propriétés à ajouter — DONNÉES À VÉRIFIER AVEC ISMAËL

### 2.1 Lieu de naissance

| Propriété | Code | Valeur | QID/Format | Source URL |
|-----------|------|--------|------------|-----------|
| place of birth | P19 | Montélimar | Q234270 | https://www.lefresnoy.net/en/ecole/etudiant/237/ |

> **À CONFIRMER** : Plusieurs sources indiquent Montélimar. Vérifier que ce n'est pas une commune voisine.

### 2.2 Formation (P69 — educated at)

| Propriété | Code | Valeur | QID | Qualificatif | Source URL |
|-----------|------|--------|-----|-------------|-----------|
| educated at | P69 | INSAS | Q3152458 | P812: film editing (chercher QID exact) | https://www.lefresnoy.net/en/ecole/etudiant/237/ |
| educated at | P69 | LUCA School of Arts, campus Sint-Lukas Brussels | Q1479721 | P812: filmmaking/directing | https://www.lefresnoy.net/en/ecole/etudiant/237/ |
| educated at | P69 | Le Fresnoy | Q3222963 | P580/P582: dates à confirmer (prob. 2016-2018) | https://www.lefresnoy.net/en/ecole/etudiant/237/ |

> **À CONFIRMER** : Dates exactes de fréquentation de chaque école.

### 2.3 Nom de famille

| Propriété | Code | Valeur | QID/Format | Source URL |
|-----------|------|--------|------------|-----------|
| family name | P734 | Joffroy Chandoutis | à créer ou string monolingue | https://ismaeljoffroychandoutis.com |

> **Note technique** : P734 attend un item Wikidata. Si aucun item n'existe pour "Joffroy Chandoutis", soit en créer un (instance of: family name Q101352), soit passer pour le moment.

### 2.4 Affiliation

| Propriété | Code | Valeur | QID | Qualificatif | Source URL |
|-----------|------|--------|-----|-------------|-----------|
| affiliation | P1416 | CENTQUATRE-Paris | Q2944288 | P580: 2022 ; P3831: artiste associé | https://www.104.fr/artiste/ismael-joffroy-chandoutis-biographie.html |

### 2.5 Prix et récompenses (P166)

#### César 2022 — CONFIRMÉ

| Propriété | Code | Valeur | QID | Qualificatifs | Source URL |
|-----------|------|--------|-----|--------------|-----------|
| award received | P166 | César du meilleur court métrage documentaire | Q239675 | P585: 2022 ; P1686: Maalbeek [QID à créer] ; P805: Q109048767 (47e cérémonie) | https://www.academie-cinema.org/personnes/ismael-joffroy-chandoutis-238555/ |

#### Prix ADAGP Révélation Art numérique 2018 — CONFIRMÉ

| Propriété | Code | Valeur | QID | Qualificatifs | Source URL |
|-----------|------|--------|-----|--------------|-----------|
| award received | P166 | ADAGP Révélation Art numérique | PAS DE QID (à créer ou utiliser générique) | P585: 2018 ; P1686: Swatted [QID à créer] | https://www.adagp.fr/en/actuality/adagp-2018-digital-art-revelation-video-art-award-went-ismael-joffroy-chandoutis |

> **Item à créer potentiellement** : "ADAGP Digital Art Revelation" (instance of: Q618779 award).

#### Prix Ars Electronica — Honorary Mention 2019 — CONFIRMÉ

| Propriété | Code | Valeur | QID | Qualificatifs | Source URL |
|-----------|------|--------|-----|--------------|-----------|
| award received | P166 | Prix Ars Electronica | Q697762 | P585: 2019 ; P1686: Swatted [QID à créer] ; P3831: honorary mention (chercher QID) | https://archive.aec.at/prix/ (catégorie: Computer Animation) |

> **Catégorie précise** : Computer Animation, Honorary Mention, 2019.

#### Prix spécial du jury Labo — Clermont-Ferrand 2019 — CONFIRMÉ

| Propriété | Code | Valeur | QID | Qualificatifs | Source URL |
|-----------|------|--------|-----|--------------|-----------|
| award received | P166 | Special Jury Prize (Labo) | chercher QID ou générique | P585: 2019 ; P1686: Swatted ; P805: Q465682 (Clermont-Ferrand) | https://en.unifrance.org/directories/person/393598/ismael-joffroy-chandoutis |

#### Autres prix mentionnés (à vérifier détails avec Ismaël)

| Prix | Année | Film | Source |
|------|-------|------|--------|
| Prix SCAM Émergences | 2019 | Swatted | Unifrance, multiples sources |
| Best Int'l Documentary Short — Guanajuato | 2019 | Swatted (Oscar Qualifying) | Unifrance, ADAGP |
| Annie Awards nomination — Best Short Subject | 2022 | Maalbeek | Villa Albertine |
| Bayard du meilleur court — FIFF Namur | 2020 | Maalbeek | Semaine de la Critique |
| Prix Festivals Connexion — Clermont-Ferrand | ? | Dark Waves | film-documentaire.fr |
| Grand Prix + Prix du jury jeune — Regensburg | ? | Dark Waves | film-documentaire.fr |
| European Film Awards nomination | 2020 | Maalbeek | multiples sources |

---

## 3. Identifiants d'autorité — RÉSULTAT DES RECHERCHES

| Identifiant | Code Wikidata | Résultat | Action |
|-------------|--------------|----------|--------|
| VIAF ID | P214 | **NON TROUVÉ** (recherche API VIAF : 0 résultats) | Sera créé automatiquement quand BnF ou autre bibliothèque nationale référencera l'artiste |
| BnF ID | P268 | **NON TROUVÉ** (recherche data.bnf.fr et catalogue.bnf.fr : 0 résultats) | Sera créé lors du dépôt légal ou création notice BnF |
| IdRef (Sudoc) | P269 | **NON TROUVÉ** (recherche API IdRef/Solr : numFound=0) | Pas d'entrée IdRef/Sudoc |
| ISNI | P213 | **NON TROUVÉ** (isni.org bloqué par Cloudflare, pas de résultat web) | Chercher directement sur isni.org ou demander attribution via BnF |
| GND | P227 | **NON TROUVÉ** (recherche dnb.de : 0 résultats) | Probable absence, malgré article Wikipedia DE |

> **Analyse** : L'absence de tous les identifiants d'autorité bibliographiques est notable mais pas inhabituelle pour un artiste/cinéaste émergent travaillant principalement dans le court métrage et l'art contemporain. Le passage au long métrage et la création d'une page Wikipedia FR accéléreront la création de ces identifiants.

### Identifiants supplémentaires trouvés (non dans guide sprint 1)

| Identifiant | Propriété Wikidata | Valeur | Source URL |
|-------------|-------------------|--------|-----------|
| film-documentaire.fr person ID | chercher P-code | C_63939_F | https://www.film-documentaire.fr/4DACTION/w_liste_generique/C_63939_F |
| Académie des César person | pas de P-code standard | 238555 | https://www.academie-cinema.org/personnes/ismael-joffroy-chandoutis-238555/ |
| Letterboxd director slug | P8687 | ismael-joffroy-chandoutis (à vérifier) | https://letterboxd.com/film/maalbeek/ (films présents) |
| Cinando company (Films Grand Huit) | — | 236995 | https://cinando.com/en/Company/films_grand_huit_236995/Detail |
| CIFRA | — | ismaeljoffroychandoutis | https://cifra.com/account/ismaeljoffroychandoutis |

---

## 4. Items Wikidata à créer

### 4.1 Films (aucun n'a d'entrée Wikidata)

#### Maalbeek — PRIORITAIRE

```
Label (en): Maalbeek
Label (fr): Maalbeek
Description (en): 2020 French animated documentary short film directed by Ismaël Joffroy Chandoutis
Description (fr): court métrage documentaire animé français de 2020 réalisé par Ismaël Joffroy Chandoutis

Propriétés :
- P31 (instance of) : short film (Q24862) + documentary film (Q93204) + animated film (Q202866)
- P57 (director) : Q106873862
- P364 (original language) : French (Q150)
- P495 (country of origin) : France (Q142)
- P577 (publication date) : 2020
- P345 (IMDb ID) : tt13332920
- P3980 (Unifrance film ID) : 50347
- P166 (award received) : Q239675 (César), qualifier P585: 2022
- P2334 (film-documentaire.fr film ID) : 60102 (à vérifier P-code exact)
```

#### Swatted — PRIORITAIRE

```
Label (en): Swatted
Label (fr): Swatted
Description (en): 2018 French animated documentary short film directed by Ismaël Joffroy Chandoutis
Description (fr): court métrage documentaire animé français de 2018 réalisé par Ismaël Joffroy Chandoutis

Propriétés :
- P31 (instance of) : short film (Q24862) + animated documentary (Q4765076)
- P57 (director) : Q106873862
- P364 (original language) : French (Q150)
- P495 (country of origin) : France (Q142)
- P577 (publication date) : 2018
- P345 (IMDb ID) : tt9650444
- P3980 (Unifrance film ID) : 46628
- P166 (award received) : Q697762 (Prix Ars Electronica), qualifier P585: 2019, P3831: honorary mention
- P2334 (film-documentaire.fr film ID) : 54416
```

#### Dark Waves / Ondes noires

```
Label (en): Dark Waves
Label (fr): Ondes noires
Also known as (en): Ondes noires
Also known as (fr): Dark Waves
Description (en): 2017 French short documentary film directed by Ismaël Joffroy Chandoutis
Description (fr): court métrage documentaire français de 2017 réalisé par Ismaël Joffroy Chandoutis

Propriétés :
- P31 (instance of) : short film (Q24862) + documentary film (Q93204)
- P57 (director) : Q106873862
- P364 (original language) : French (Q150)
- P495 (country of origin) : France (Q142)
- P577 (publication date) : 2017
- P2334 (film-documentaire.fr film ID) : 22041
```

> **Les autres films** (De Facto, Amnesia, Virtual Kintsugi, Deep Forensic, Mémoires Fractales, Madostuki the Dreamer) nécessitent vérification avec Ismaël pour les détails avant création.

### 4.2 Entités liées (sans item Wikidata)

| Entité | Type | Notes |
|--------|------|-------|
| Films Grand Huit | production company (Q1شركة) | Fondée 2015, Paris. 3 Césars. Unifrance ID: 355323 |
| ADAGP Révélation Art numérique | award (Q618779) | Prix annuel ADAGP + Le Fresnoy depuis 2015 |

---

## 5. Ordre de priorité recommandé

### Phase 1 — Immédiat (pas besoin de vérification)

1. P27 country of citizenship
2. P856 official website
3. P1412 languages spoken (French, English)
4. P2003 Instagram username
5. P2002 Twitter/X username
6. P101 field of work (4 valeurs)
7. P136 genre (4 valeurs)
8. P106 occupation: ajouter artist (Q483501)
9. Labels et descriptions multilingues + aliases

### Phase 2 — Après vérification avec Ismaël

1. P19 place of birth
2. P69 educated at (3 écoles, avec dates)
3. P1416 affiliation CENTQUATRE
4. P734 family name

### Phase 3 — Après création des items films

1. Créer items Maalbeek et Swatted
2. P800 notable work (lier les films)
3. P166 award received (César, Ars Electronica, ADAGP, Clermont-Ferrand)

### Phase 4 — Quand disponibles

1. Identifiants d'autorité (VIAF, BnF, IdRef, ISNI, GND) — tous absents pour l'instant
2. P8687 Letterboxd (à confirmer slug)
3. P18 image (upload Wikimedia Commons si photo CC disponible)
4. Créer item Films Grand Huit puis lier via P272 sur les items films

---

## 6. QIDs de référence vérifiés

| Item | QID | Vérifié |
|------|-----|---------|
| Ismaël Joffroy Chandoutis | Q106873862 | ✅ API |
| human | Q5 | ✅ |
| male | Q6581097 | ✅ |
| film director | Q1414443 | ✅ API (déjà présent) |
| filmmaker | Q2526255 | ✅ API (déjà présent) |
| artist | Q483501 | ✅ |
| France | Q142 | ✅ |
| Montélimar | Q234270 | ✅ |
| French language | Q150 | ✅ |
| English language | Q1860 | ✅ |
| INSAS | Q3152458 | ✅ |
| LUCA campus Sint-Lukas Brussels | Q1479721 | ✅ |
| Le Fresnoy | Q3222963 | ✅ |
| CENTQUATRE-Paris | Q2944288 | ✅ |
| film | Q11424 | ✅ |
| contemporary art | Q186030 | ✅ |
| digital art | Q12906101 | ✅ |
| artificial intelligence | Q11660 | ✅ |
| documentary film | Q93204 | ✅ |
| experimental film | Q16113416 | ✅ |
| short film | Q24862 | ✅ |
| animated documentary | Q4765076 | ✅ |
| animated film | Q202866 | ✅ |
| César Best Documentary Short | Q239675 | ✅ |
| 47th César Awards | Q109048767 | ✅ |
| Prix Ars Electronica | Q697762 | ✅ |
| Clermont-Ferrand ISFF | Q465682 | ✅ |
| Semaine de la Critique | Q374895 | ✅ |
| family name (class) | Q101352 | ✅ |
| award (class) | Q618779 | ✅ |

---

## 7. Récapitulatif : nombre de propriétés cible

| Catégorie | Propriétés | Nombre déclarations |
|-----------|-----------|---------------------|
| Déjà présentes | P31, P21, P106 (x2), P735, P569, P345, P3980, P4985 | 9 |
| Phase 1 (immédiat) | P27, P856, P1412 (x2), P2003, P2002, P101 (x4), P136 (x4), P106 (+1) | +14 |
| Phase 2 (vérification) | P19, P69 (x3), P1416, P734 | +6 |
| Phase 3 (films + prix) | P800 (x3-9), P166 (x4+) | +7 min |
| **Total estimé** | | **36+ déclarations, ~26 propriétés uniques** |

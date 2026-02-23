# Framer Deployment Report - GEO Sprint 2

**Date** : 2026-02-22
**Site** : ismaeljoffroychandoutis.com (Framer)
**Statut MCP** : Non connecte (plugin Framer MCP non actif)

---

## Résumé

Le MCP Framer n'est pas accessible (le plugin doit etre ouvert dans l'editeur Framer). Toutes les actions ci-dessous sont donc **manuelles**. Chaque section contient les instructions exactes et les valeurs a coller.

---

## 1. Injection JSON-LD Schema dans le `<head>`

### Instructions

1. Ouvrir le projet dans **Framer** (https://framer.com)
2. Aller dans **Site Settings** (icone engrenage en bas a gauche)
3. Cliquer sur **General**
4. Scroller jusqu'a la section **Custom Code**
5. Dans le champ **End of `<head>` tag**, coller le contenu complet ci-dessous
6. Cliquer **Save**

### Valeur a coller (End of `<head>` tag)

```html
<!-- Schema.org JSON-LD - Ismael Joffroy Chandoutis -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Person",
  "@id": "https://ismaeljoffroychandoutis.com/#person",
  "name": "Ismael Joffroy Chandoutis",
  "alternateName": ["Ismael Joffroy Chandoutis", "IJC"],
  "url": "https://ismaeljoffroychandoutis.com",
  "image": "https://ismaeljoffroychandoutis.com/portrait.jpg",
  "jobTitle": ["Filmmaker", "Contemporary Artist", "Digital Artist"],
  "description": "French filmmaker and contemporary artist working at the intersection of cinema, contemporary art, and artificial intelligence. Pioneer of post-documentary filmmaking exploring memory, identity, and technology through hybrid forms combining documentary, animation, and digital art.",
  "birthDate": "1988-05-25",
  "birthPlace": {
    "@type": "Place",
    "name": "Montelimar, France"
  },
  "nationality": {
    "@type": "Country",
    "name": "France"
  },
  "sameAs": [
    "https://www.imdb.com/name/nm5604010/",
    "https://www.instagram.com/ismael_jchandoutis/",
    "https://www.linkedin.com/in/isma%C3%ABl-joffroy-chandoutis-223408226/",
    "https://x.com/ismajc",
    "https://mubi.com/en/cast/ismael-joffroy-chandoutis",
    "https://letterboxd.com/film/maalbeek/",
    "https://en.unifrance.org/directories/person/393598/ismael-joffroy-chandoutis",
    "https://www.lefresnoy.net/en/ecole/etudiant/237/"
  ],
  "alumniOf": [
    {
      "@type": "EducationalOrganization",
      "name": "INSAS",
      "description": "Institut National Superieur des Arts du Spectacle",
      "address": { "@type": "PostalAddress", "addressLocality": "Brussels", "addressCountry": "BE" }
    },
    {
      "@type": "EducationalOrganization",
      "name": "LUCA School of Arts",
      "alternateName": "Sint-Lukas Art School",
      "address": { "@type": "PostalAddress", "addressLocality": "Brussels", "addressCountry": "BE" }
    },
    {
      "@type": "EducationalOrganization",
      "name": "Le Fresnoy - Studio National des Arts Contemporains",
      "url": "https://www.lefresnoy.net",
      "address": { "@type": "PostalAddress", "addressLocality": "Tourcoing", "addressCountry": "FR" }
    }
  ],
  "award": [
    "Cesar 2022 - Best Documentary Short Film (Maalbeek)",
    "Honorary Mention - Ars Electronica",
    "Prix ADAGP Revelation Art Numerique",
    "Semaine de la Critique - Cannes 2020 (Maalbeek)",
    "Prix du public - Festival de Clermont-Ferrand (Maalbeek)",
    "Prix des effets visuels - Festival de Clermont-Ferrand (Maalbeek)",
    "Bayard Best Short Film - Festival International du Film Francophone de Namur (Maalbeek)",
    "Special Jury Prize Labo - Clermont-Ferrand (Swatted)",
    "Prix Scam Emergences (Swatted)",
    "Grand Prix - Regensburg Short Film Festival (Dark Waves)",
    "Youth Jury Prize - Regensburg Short Film Festival (Dark Waves)"
  ],
  "knowsAbout": [
    "Artificial Intelligence", "Post-documentary filmmaking", "Contemporary art",
    "Digital art", "Cinema", "Post-photography", "Photogrammetry",
    "Deepfake technology", "Video game engines", "Generative AI",
    "Media convergence", "Memory and trauma in art"
  ],
  "memberOf": {
    "@type": "Organization",
    "name": "CENTQUATRE-PARIS",
    "url": "https://www.104.fr",
    "description": "Artiste associe since 2022"
  },
  "worksFor": {
    "@type": "Organization",
    "name": "Films Grand Huit",
    "url": "http://filmsgrandhuit.com"
  },
  "hasOccupation": [
    { "@type": "Occupation", "name": "Film Director", "occupationalCategory": "27-2012.00" },
    { "@type": "Occupation", "name": "Contemporary Artist" },
    { "@type": "Occupation", "name": "Film Editor" }
  ]
}
</script>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebSite",
  "@id": "https://ismaeljoffroychandoutis.com/#website",
  "name": "Ismael Joffroy Chandoutis",
  "alternateName": "IJC",
  "url": "https://ismaeljoffroychandoutis.com",
  "description": "Official website of Ismael Joffroy Chandoutis, French filmmaker and contemporary artist working at the intersection of cinema, contemporary art, and artificial intelligence.",
  "inLanguage": ["en", "fr"],
  "publisher": { "@id": "https://ismaeljoffroychandoutis.com/#person" },
  "potentialAction": {
    "@type": "SearchAction",
    "target": "https://ismaeljoffroychandoutis.com/?search={search_term_string}",
    "query-input": "required name=search_term_string"
  }
}
</script>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Movie",
  "@id": "https://ismaeljoffroychandoutis.com/works/maalbeek#work",
  "name": "Maalbeek",
  "url": "https://ismaeljoffroychandoutis.com/works/maalbeek",
  "dateCreated": "2020",
  "duration": "PT16M",
  "description": "Sabine, survivor but amnesiac of the bombing at Maalbeek metro station on March 22, 2016 in Brussels, searches for the missing image of an over-mediatised event of which she has no memory. A hybrid montage of archival images and 3D animation explores the motif of fragmentation, memory, and trauma.",
  "genre": ["Documentary", "Animation", "Short Film", "Experimental"],
  "inLanguage": "fr",
  "countryOfOrigin": { "@type": "Country", "name": "France" },
  "director": { "@id": "https://ismaeljoffroychandoutis.com/#person" },
  "author": [
    { "@id": "https://ismaeljoffroychandoutis.com/#person" },
    { "@type": "Person", "name": "Perrine Prost" }
  ],
  "productionCompany": { "@type": "Organization", "name": "Films Grand Huit", "url": "http://filmsgrandhuit.com" },
  "award": [
    "Cesar 2022 - Best Documentary Short Film",
    "Semaine de la Critique - Cannes 2020 - Official Selection",
    "Prix du public - Festival de Clermont-Ferrand 2021",
    "Prix des effets visuels - Festival de Clermont-Ferrand 2021",
    "Bayard Best Short Film - Festival International du Film Francophone de Namur 2020",
    "European Film Awards 2021 - Candidate"
  ],
  "sameAs": [
    "https://www.imdb.com/title/tt13332920/",
    "https://letterboxd.com/film/maalbeek/",
    "https://en.unifrance.org/movie/50347/maalbeek",
    "https://www.semainedelacritique.com/en/edition/2020/movie/maalbeek"
  ]
}
</script>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Movie",
  "@id": "https://ismaeljoffroychandoutis.com/works/swatted#work",
  "name": "Swatted",
  "url": "https://ismaeljoffroychandoutis.com/works/swatted",
  "dateCreated": "2018",
  "duration": "PT21M",
  "description": "Online players describe their struggles with swatting, a life-threatening cyber-harassment phenomenon that looms over them whenever they play. The events take shape through YouTube videos and wireframe images from a modified GTA V video game engine.",
  "genre": ["Documentary", "Animation", "Short Film"],
  "inLanguage": "en",
  "countryOfOrigin": { "@type": "Country", "name": "France" },
  "director": { "@id": "https://ismaeljoffroychandoutis.com/#person" },
  "author": { "@id": "https://ismaeljoffroychandoutis.com/#person" },
  "productionCompany": { "@type": "Organization", "name": "Le Fresnoy - Studio National des Arts Contemporains", "url": "https://www.lefresnoy.net" },
  "award": [
    "Special Jury Prize Labo - Clermont-Ferrand",
    "Prix Scam Emergences",
    "Best International Short Documentary - Guanajuato Festival (Oscar Qualifying)",
    "Honorary Mention - Ars Electronica",
    "IDFA 2018 - World Premiere"
  ],
  "sameAs": [
    "https://www.imdb.com/title/tt9650444/",
    "https://letterboxd.com/film/swatted/",
    "https://en.unifrance.org/movie/46628/swatted",
    "https://www.idfa.nl/en/film/eaf8af1b-0e53-4cb9-882f-6fea66e9b8db/swatted/"
  ]
}
</script>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Movie",
  "@id": "https://ismaeljoffroychandoutis.com/works/dark-waves#work",
  "name": "Dark Waves",
  "alternateName": "Ondes Noires",
  "url": "https://ismaeljoffroychandoutis.com/works/dark-waves",
  "dateCreated": "2017",
  "duration": "PT21M",
  "description": "In our hyper-connected society, invisible electromagnetic waves invade almost all environments. Three people who are unable to tolerate electromagnetic radiation speak about how they manage to survive in a world that they feel is becoming increasingly inaccessible to them. The film attempts to materialize these invisible waves onscreen.",
  "genre": ["Documentary", "Experimental", "Animation", "Short Film"],
  "inLanguage": "fr",
  "countryOfOrigin": { "@type": "Country", "name": "France" },
  "director": { "@id": "https://ismaeljoffroychandoutis.com/#person" },
  "author": { "@id": "https://ismaeljoffroychandoutis.com/#person" },
  "productionCompany": { "@type": "Organization", "name": "Le Fresnoy - Studio National des Arts Contemporains", "url": "https://www.lefresnoy.net" },
  "award": [
    "Grand Prix - Regensburg Short Film Festival",
    "Youth Jury Prize - Regensburg Short Film Festival",
    "Prix Festivals Connexion Auvergne Rhone Alpes - Clermont-Ferrand"
  ],
  "sameAs": [
    "https://www.imdb.com/title/tt8066650/",
    "https://letterboxd.com/film/dark-waves-2017/",
    "https://en.unifrance.org/movie/45236/dark-waves",
    "https://www.idfa.nl/en/film/3952b3f1-5759-4985-8b58-917357b46f8d/dark-waves/"
  ]
}
</script>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "@id": "https://ismaeljoffroychandoutis.com/works/amnesia#work",
  "name": "Amnesia",
  "url": "https://ismaeljoffroychandoutis.com/works/amnesia",
  "description": "A work exploring themes of memory loss, identity, and the digital reconstruction of experience.",
  "genre": ["Film", "Contemporary Art"],
  "creator": { "@id": "https://ismaeljoffroychandoutis.com/#person" },
  "countryOfOrigin": { "@type": "Country", "name": "France" }
}
</script>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "@id": "https://ismaeljoffroychandoutis.com/works/virtual-kintsugi#work",
  "name": "Virtual Kintsugi",
  "url": "https://ismaeljoffroychandoutis.com/works/virtual-kintsugi",
  "description": "An innovative approach to restoring damaged artworks using generative artificial intelligence. Based on ten paintings from the Musee Granet in Aix-en-Provence awaiting restoration, the project embraces the subjectivity of AI interpretations to transform them into standalone works that pay homage to the damaged paintings while transcending them. One of the first NFTs integrated into the collection of a French museum.",
  "genre": ["Digital Art", "Installation", "Generative AI Art"],
  "creator": { "@id": "https://ismaeljoffroychandoutis.com/#person" },
  "countryOfOrigin": { "@type": "Country", "name": "France" },
  "locationCreated": {
    "@type": "Place",
    "name": "Musee Granet",
    "address": { "@type": "PostalAddress", "addressLocality": "Aix-en-Provence", "addressCountry": "FR" }
  }
}
</script>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "@id": "https://ismaeljoffroychandoutis.com/works/deep-forensic#work",
  "name": "Deep Forensic",
  "url": "https://ismaeljoffroychandoutis.com/works/deep-forensic",
  "description": "A work at the intersection of cinema, digital art, and technology, exploring post-truth era themes through hybrid documentary forms.",
  "genre": ["Film", "Digital Art"],
  "creator": { "@id": "https://ismaeljoffroychandoutis.com/#person" },
  "countryOfOrigin": { "@type": "Country", "name": "France" }
}
</script>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "@id": "https://ismaeljoffroychandoutis.com/works/memoires-fractales#work",
  "name": "Memoires Fractales",
  "alternateName": "Memoires fractales",
  "url": "https://ismaeljoffroychandoutis.com/works/memoires-fractales",
  "description": "A work exploring fractured memories and the fragmentation of experience through digital and cinematic forms.",
  "genre": ["Film", "Digital Art"],
  "creator": { "@id": "https://ismaeljoffroychandoutis.com/#person" },
  "countryOfOrigin": { "@type": "Country", "name": "France" }
}
</script>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "CreativeWork",
  "@id": "https://ismaeljoffroychandoutis.com/works/madotsuki-the-dreamer#work",
  "name": "Madotsuki the Dreamer",
  "alternateName": "Madotsuki_the_Dreamer",
  "url": "https://ismaeljoffroychandoutis.com/works/madotsuki-the-dreamer",
  "dateCreated": "2023",
  "description": "A work relying on generative AI to process the astronomical amount of data related to its main character. Presented at the Biennale NEMO 2023 and the Port des Createurs in January 2024.",
  "genre": ["Digital Art", "Installation", "Generative AI Art"],
  "creator": { "@id": "https://ismaeljoffroychandoutis.com/#person" },
  "countryOfOrigin": { "@type": "Country", "name": "France" }
}
</script>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "@id": "https://ismaeljoffroychandoutis.com/#breadcrumb-works",
  "name": "Works Navigation",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://ismaeljoffroychandoutis.com" },
    { "@type": "ListItem", "position": 2, "name": "Works", "item": "https://ismaeljoffroychandoutis.com/works" }
  ]
}
</script>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "@id": "https://ismaeljoffroychandoutis.com/#breadcrumb-about",
  "name": "About Navigation",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://ismaeljoffroychandoutis.com" },
    { "@type": "ListItem", "position": 2, "name": "About", "item": "https://ismaeljoffroychandoutis.com/about" }
  ]
}
</script>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "@id": "https://ismaeljoffroychandoutis.com/#breadcrumb-press",
  "name": "Press Navigation",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://ismaeljoffroychandoutis.com" },
    { "@type": "ListItem", "position": 2, "name": "Press", "item": "https://ismaeljoffroychandoutis.com/press" }
  ]
}
</script>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "@id": "https://ismaeljoffroychandoutis.com/works/maalbeek#breadcrumb",
  "name": "Maalbeek Breadcrumb",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://ismaeljoffroychandoutis.com" },
    { "@type": "ListItem", "position": 2, "name": "Works", "item": "https://ismaeljoffroychandoutis.com/works" },
    { "@type": "ListItem", "position": 3, "name": "Maalbeek", "item": "https://ismaeljoffroychandoutis.com/works/maalbeek" }
  ]
}
</script>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "@id": "https://ismaeljoffroychandoutis.com/works/swatted#breadcrumb",
  "name": "Swatted Breadcrumb",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://ismaeljoffroychandoutis.com" },
    { "@type": "ListItem", "position": 2, "name": "Works", "item": "https://ismaeljoffroychandoutis.com/works" },
    { "@type": "ListItem", "position": 3, "name": "Swatted", "item": "https://ismaeljoffroychandoutis.com/works/swatted" }
  ]
}
</script>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "@id": "https://ismaeljoffroychandoutis.com/works/dark-waves#breadcrumb",
  "name": "Dark Waves Breadcrumb",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://ismaeljoffroychandoutis.com" },
    { "@type": "ListItem", "position": 2, "name": "Works", "item": "https://ismaeljoffroychandoutis.com/works" },
    { "@type": "ListItem", "position": 3, "name": "Dark Waves", "item": "https://ismaeljoffroychandoutis.com/works/dark-waves" }
  ]
}
</script>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "@id": "https://ismaeljoffroychandoutis.com/works/virtual-kintsugi#breadcrumb",
  "name": "Virtual Kintsugi Breadcrumb",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://ismaeljoffroychandoutis.com" },
    { "@type": "ListItem", "position": 2, "name": "Works", "item": "https://ismaeljoffroychandoutis.com/works" },
    { "@type": "ListItem", "position": 3, "name": "Virtual Kintsugi", "item": "https://ismaeljoffroychandoutis.com/works/virtual-kintsugi" }
  ]
}
</script>

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "@id": "https://ismaeljoffroychandoutis.com/works/madotsuki-the-dreamer#breadcrumb",
  "name": "Madotsuki the Dreamer Breadcrumb",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://ismaeljoffroychandoutis.com" },
    { "@type": "ListItem", "position": 2, "name": "Works", "item": "https://ismaeljoffroychandoutis.com/works" },
    { "@type": "ListItem", "position": 3, "name": "Madotsuki the Dreamer", "item": "https://ismaeljoffroychandoutis.com/works/madotsuki-the-dreamer" }
  ]
}
</script>
```

---

## 2. Servir llms.txt a la racine

### Probleme

Framer ne permet **pas** de servir des fichiers statiques arbitraires a la racine du domaine (comme `/llms.txt`). Il n'y a pas d'equivalent a un dossier `/public` ou de serveur de fichiers statiques.

### Solutions possibles (par ordre de preference)

#### Option A : Page Framer dediee (recommande)

1. Dans Framer, cliquer **+** (Add Page) dans le panneau gauche
2. Nommer la page **llms.txt** (le slug sera `/llms-txt` ou `/llms.txt`)
3. **Attention** : Framer ajoute du HTML autour, donc ce ne sera pas du pur texte. Mais les crawlers IA liront quand meme le contenu.
4. Ajouter un composant **Text** qui contient le texte complet du llms.txt
5. Styliser en monospace, fond blanc, pour ressembler a du texte brut
6. Ajouter dans le Custom Code (Head) de cette page specifique :
```html
<meta name="robots" content="noindex">
```

**Limitation** : Le slug sera probablement `/llms-txt` (avec tiret) car Framer n'autorise pas les points dans les slugs.

#### Option B : Redirect + fichier heberge ailleurs (plus propre)

1. Heberger le fichier `llms.txt` sur un CDN ou un service statique (GitHub Pages, Cloudflare Pages, Netlify)
2. Dans Framer, aller dans **Site Settings > General > Redirects**
3. Ajouter un redirect :
   - **From** : `/llms.txt`
   - **To** : `https://cdn.example.com/llms.txt` (l'URL du fichier heberge)
   - **Type** : 301

#### Option C : Cloudflare Worker (si le domaine passe par Cloudflare)

Si le DNS passe par Cloudflare, on peut intercepter `/llms.txt` avec un Worker qui sert le fichier directement.

### Contenu du fichier llms.txt

```
# Ismael Joffroy Chandoutis

> French filmmaker and contemporary artist working at the intersection of cinema, contemporary art, and digital art. Known for post-documentary films exploring online violence, memory, trauma, and virtual worlds. Winner of the Cesar 2022 for Best Short Film. Central to his practice is a non-productivist approach to AI as a collaborator that alters rather than augments.

## Bio

Ismael Joffroy Chandoutis (born 1988, France) is a filmmaker and contemporary artist based in Paris. He studied at INSAS (Brussels), LUCA School of Arts, and Le Fresnoy - Studio National des Arts Contemporains. His work operates across cinema (post-documentary, fiction, animation), installations, post-photography, and performance. He has been an associated artist at CENTQUATRE-Paris since 2022. His films have screened at Cannes (Semaine de la Critique), Berlinale, IDFA, FID Marseille, and dozens of international festivals. His installations have been exhibited at Centre Pompidou, Pearl Art Museum Shanghai, and biennials worldwide. His artistic methodology, which he calls "liquid writing," treats AI not as a productivity tool but as a collaborator that introduces alterity into the creative process. He is currently developing feature-length projects including "The Goldberg Variations" and "Virus," both produced by Films Grand Huit.

## Key Facts

- Born: 1988, France
- Based: Paris
- Education: INSAS (Brussels), LUCA School of Arts, Le Fresnoy - Studio National des Arts Contemporains
- Cesar 2022 winner: Best Short Film (Maalbeek)
- Ars Electronica prize winner
- Associated artist at CENTQUATRE-Paris since 2022
- Production company: Films Grand Huit
- Methodology: Liquid writing
- Wikidata: Q106873862

## Notable Works

- Maalbeek (2017) - Short film, Cesar 2022 winner (Best Short Film)
- Swatted (2018) - Short film on swatting and virtual violence
- De Facto - Short film
- Dark Waves - Short film
- Amnesia - Short film
- Virtual Kintsugi - Film/installation
- Deep Forensic - Film/installation
- Madostuki the Dreamer - Short film
- Memoires Fractales - Film/installation

## Artistic Statement

AI is central to his practice as subject, method, and collaborator. His philosophy rejects the "augmentation" paradigm in favor of alteration: AI as a force that transforms the creative process itself rather than optimizing output. This anti-productivist stance positions AI as a means of exploring what escapes human intention.

## Links

- Website: https://ismaeljoffroychandoutis.com
- IMDB: https://www.imdb.com/name/nm8325972/
- Vimeo: https://vimeo.com/ismaeljoffroychandoutis
- Instagram: https://www.instagram.com/ismaeljoffroychandoutis/
- Wikidata: https://www.wikidata.org/wiki/Q106873862
```

---

## 3. Ajouter `lang="fr"` a la balise `<html>`

### Instructions

Framer ne permet pas de modifier directement l'attribut `lang` de la balise `<html>` via l'UI standard. Il y a deux approches :

#### Option A : Via Site Settings (si disponible)

1. **Site Settings** > **General**
2. Chercher un champ **Language** ou **Locale**
3. Si present, selectionner **French (fr)**

#### Option B : Via Custom Code (injection JavaScript)

1. **Site Settings** > **General** > **Custom Code**
2. Dans le champ **End of `<head>` tag**, ajouter (en plus du JSON-LD ci-dessus) :

```html
<script>document.documentElement.lang = "fr";</script>
```

**Note** : Cette methode fonctionne pour les navigateurs mais les crawlers qui ne executent pas JavaScript ne verront pas le changement. Cependant, les crawlers IA modernes (GPTBot, ClaudeBot) executent generalement JavaScript.

#### Option C : Via Framer locale settings

1. Dans l'editeur Framer, chercher **Localization** dans les settings du projet
2. Si le projet a la localisation activee, definir le locale par defaut sur `fr`

---

## 4. Pages a supprimer du sitemap

### Pages identifiees a supprimer ou desindexer

Les pages suivantes doivent etre soit supprimees, soit marquees `noindex` :

| Page | Action recommandee |
|------|-------------------|
| `/404` | Marquer **noindex** (ne pas supprimer, Framer en a besoin) |
| `/new-page` | **Supprimer** (page vide/par defaut) |
| Articles Lorem Ipsum | **Supprimer** ou depublier |

### Instructions pour desindexer une page

1. Cliquer sur la page dans le panneau gauche de Framer
2. Cliquer sur l'icone **engrenage** (Page Settings) a cote du nom de la page
3. Onglet **SEO**
4. Cocher **"Hide from search engines"** (ajoute `<meta name="robots" content="noindex">`)

### Instructions pour supprimer une page

1. Clic droit sur la page dans le panneau gauche
2. Selectionner **Delete**
3. Confirmer la suppression

### Instructions pour identifier les articles Lorem Ipsum

1. Dans le panneau gauche, regarder les pages sous la section **Blog** ou **Articles** (si CMS active)
2. Ouvrir chaque article, verifier si le contenu est du Lorem Ipsum
3. Pour chaque article factice : clic droit > **Delete**, ou le depublier via le CMS

### Exclure du sitemap via robots.txt (complement)

Dans **Site Settings > Custom Code > End of `<head>` tag**, on ne peut pas gerer robots.txt. Cependant :

1. Aller dans **Site Settings > General**
2. Chercher un champ **robots.txt** ou **Crawlers**
3. Si present, ajouter :
```
Disallow: /404
Disallow: /new-page
```

**Note** : Framer genere automatiquement le sitemap. Les pages marquees `noindex` sont normalement exclues. La suppression est la methode la plus fiable.

---

## 5. Actions additionnelles recommandees

### Meta description globale

Dans **Site Settings > General > SEO** :
- **Title** : `Ismael Joffroy Chandoutis - Filmmaker & Contemporary Artist`
- **Description** : `French filmmaker and contemporary artist at the intersection of cinema, contemporary art, and AI. Cesar 2022 winner. Post-documentary, installations, digital art.`

### Open Graph

Dans **Site Settings > General > Social Image** :
- Uploader une image representant le travail d'Ismael (portrait ou still de film)
- Framer genere automatiquement les balises OG

### Favicons

Verifier dans **Site Settings > General > Favicon** qu'un favicon est bien configure.

---

## Resume des actions

| # | Action | Methode | Statut |
|---|--------|---------|--------|
| 1 | JSON-LD dans `<head>` | Manuelle (Custom Code) | A faire |
| 2 | Servir llms.txt | Manuelle (page ou redirect) | A faire |
| 3 | `lang="fr"` sur `<html>` | Manuelle (script ou locale) | A faire |
| 4 | Supprimer pages inutiles | Manuelle (delete/noindex) | A faire |
| 5 | Meta SEO globales | Manuelle (Site Settings) | A faire |

**MCP Framer** : Non accessible pendant cette session. Toutes les actions necessitent l'interface Framer.
Pour reactiver le MCP : ouvrir Framer, Cmd+K, chercher "MCP", ouvrir le plugin MCP.

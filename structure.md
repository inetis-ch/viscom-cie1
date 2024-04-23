
# Structure HTML et CSS d'un Portfolio

```html
<!DOCTYPE html>
<html lang="fr">

<head>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="./css/styles.css">
  <link href="https://fonts.googleapis.com/css2?family=Lato:wght@100;400;700&family=Poppins:wght@200&display=swap"
        rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@200&display=swap" rel="stylesheet">
  <title>Portfolio</title>
</head>

<body>
<header>
  <div class="container">
    <nav class="flex items-centre justify-between">
      <div class="left flex justfiy-right">
        <div class="logo">
          <img src="./images/logo.png" width="50px" alt="logo">
        </div>
        <div>
          <a href="#">Home</a>
          <a href="#about">A propos</a>
          <a href="#service">Services</a>
          <a href="blog.htm">Blog</a></li>
        </div>
      </div>
      <div class="right">
        <button class="btn btn-primary">Contact</button>
      </div>
    </nav>
  </div>
</header>
<main>
  <section id="hero" class="flex items-centre justify-between">
    <div class="left flex-1 justify-center">
      <img src="./images/portrait.png" alt="Profile">
    </div>
    <div class="right flex-1">
      <h1>Pierre-André Vullioud</h1>
      <h2>Je suis un<br> <span>Developeur</span></h2>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloremque illum nam nobis, minima
        laudantium fugit sequi nostrum quod impedit, beatae necessitatibus praesentium optio labore
        nemo!</p>
      <div>
        <a href="">
          <button class="btn btn-secondary">Télécharger mon CV</button>
        </a>
      </div>
    </div>
  </section>

  <section id="about">
    <div class="container flex items-centre">

      <div class="left flex-1">
        <h2>A propos de <span>moi</span></h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque adipisci distinctio obcaecati
          aliquid,
          quia tempora quis optio repudiandae officia earum?
          Lorem ipsum dolor sit amet consectetur, adipisicing elit.
        </p>
        <div class="flex socials">
          <a href="#"><img src="./images/facebook.png"></a>
          <a href="#"><img src="./images/instagram.png"></a>
          <a href="#"><img src="./images/reddit.png"></a>
        </div>
      </div>
      <div class="right flex-1 justify-right">
        <img src="./images/portrait2.png" alt="profile pic">
      </div>
    </div>
  </section>

  <section id="services">
    <div class="container">
      <h2 class="services-head">Mes services</h2>
      <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dicta, eligendi tempore. Eaque veniam
        impedit quis alias, sint culpa maxime animi quibusdam necessitatibus sit ex porro architecto! Unde
        animi corrupti fugit.</p>
      <div class="card-grid">
        <div class="card">
          <img src="./images/cisor.svg">
          <h2>Graphic Desgin</h2>
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nulla, debitis?</p>
        </div>
        <div class="card">
          <img src="./images/pen.svg">
          <h2>Web Development</h2>
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nulla, debitis?</p>
        </div>
        <div class="card">
          <img src="./images/valise.svg">
          <h2>Content Writing</h2>
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Nulla, debitis?</p>
        </div>
      </div>
    </div>
  </section>
</main>
<footer>
  &copy; 2024 Les pieds dans le plat
</footer>
</body>
```

## Structure de base

Dans ce document HTML, plusieurs sections et éléments sont utilisés pour structurer un site web, typiquement un portfolio. Voici une explication détaillée pour chacune des parties principales du document :

### Structure des fichiers
```md
portfolio
├── css
│   ├── styles.css
│   ├── utilities.css
│   ├── responsive.css
├── images
│   ├── logo.png
│   ├── portrait.png
│   └── etc..
└─- index.html
```

### 1. Document Type Declaration (Doctype)
```html
<!DOCTYPE html>
```
- Ceci déclare le type de document, ici un document HTML5. Cette déclaration est nécessaire pour que le navigateur interprète correctement la page comme du HTML5.

### 2. Tag `<html>`
```html
<html lang="fr">
```
- L'élément racine `<html>` contient tout le contenu de votre page web. 
- `lang="fr"` spécifie que le contenu de la page est principalement en français, aidant les moteurs de recherche et les technologies d'assistance à comprendre la langue utilisée.

### 3. Section `<head>`
```html
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="./css/styles.css">
    <link href="https://fonts.googleapis.com/css2?family=Lato:wght@100;400;700&family=Poppins:wght@200&display=swap"
        rel="stylesheet">
    <title>Portfolio</title>
</head>
```
- `<meta name="viewport">` : Configurer la zone d'affichage pour les appareils mobiles, assurant la responsivité.
- `<link rel="stylesheet">` : Lie des feuilles de style CSS externes à la page pour la mise en forme.
- `<link>` pour les polices Google : Importe des polices externes pour une utilisation dans le style de la page.
- `<title>` : Définit le titre du document, qui apparaît dans l'onglet du navigateur.

### 4. Section `<body>`
Tout le contenu visible de la page est placé ici :

#### a. `<header>`
Contient la barre de navigation et le logo, utilisant une structure de classe flexible pour l'alignement :
```html
<header>
    <div class="container">...</div>
</header>
```
- La navigation permet de relier différentes sections de la page, comme le Blog, les Services etc.

#### b. `<main>`
C'est la partie principale du contenu où différentes sections du portfolio sont détaillées :
```html
<main>
    <section id="hero">...</section>
    <section id="about">...</section>
    <section id="services">...</section>
</main>
```
- Chaque `section` possède un identifiant unique pour la navigation et la structuration, avec des contenus tels que des images, des textes, et des liens pour télécharger un CV.

### 5. `<footer>`
```html
<footer>
    &copy; 2024 Les pieds dans le plat
</footer>
```
- Contient des droits d'auteur. Utilise l'entité `&copy;` pour afficher le symbole du copyright.

## Fichier CSS principal



```css
/* Importation des fichiers */
@import 'utilities.css';
@import 'responsive.css';

:root {
  /* Déclaration des variables */
  --primary: rgb(29, 221, 189);
  --bgDark: rgb(12, 12, 12);
  --white: rgb(250, 250, 250);
  --secondary: rgb(0, 59, 50);
  --bgLight: rgb(190, 181, 181);
}

/* Reset des styles */
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Poppins', sans-serif;
  /* Definir la police par défaut */
  color: var(--bgDark);
}

.container {
  max-width: 1152px;
  /* largeur max du container */
  padding: 0 15px;
  margin: 0 auto;
  /* centrer le container */
}

section {
  padding: 6rem;
}

footer {
  background: var(--bgDark);
  color: var(--white);
  padding: 1rem 0.5rem;
  border-top: 2px solid var(--primary);
}

```

## Fichier utilitaire CSS

Un fichier utilitaire CSS, souvent appelé "fichier de classes utilitaires" ou "helpers", est utilisé pour fournir des classes réutilisables qui facilitent la mise en forme standardisée à travers les diverses parties d'un site web. 

```css
.flex {
display: flex;
/* définir un conteneur flex */
}

.items-centre {
align-items: center;
/* aligner les éléments au centre */
}

.justify-between {
justify-content: space-between;
/* aligner les éléments et répartir l'espace */
}

.justify-center {
justify-content: center;
/* aligner les éléments au centre */
}

.justify-right {
justify-content: right;
/* aligner les éléments à droite */
}

.btn {
padding: 0.6rem 2rem;
font-size: 1rem;
font-weight: 600;
border: 2px solid transparent;
/* bordure de 2px solide transparente */
outline: none;
cursor: pointer;
text-transform: uppercase;
/* transformer le texte en majuscules */
transition: all .2s ease;
/* transition de 0.2s */
}

.btn-primary {
/* bouton de base */
background-color: var(--primary);
color: var(--secondary);
margin-top: -15rem;
}

.btn-primary:hover {
/* survol des boutons */
background: transparent;
border-color: var(--primary);
color: var(--primary);
}

.flex-1 {
flex: 1;
/* définis le facteur de flexibilité */
}

.btn-secondary {
background: transparent;
color: var(--primary);
border-color: var(--primary);
}

.btn-secondary:hover {
background: var(--primary);
color: var(--secondary);
}
```

### Signification du contenu du fichier utilitaire

Chaque classe dans ce fichier utilitaire sert un objectif spécifique de mise en page ou de décoration. Voici ce que chaque classe fait:

- `.flex` : Met en place un conteneur flex. Ce mode de mise en page est utilisé pour créer des designs flexibles et réactifs en permettant aux enfants de s’adapter dynamiquement à l’espace disponible.

- `.items-centre` : Centre verticalement les éléments dans un conteneur flex.

- `.justify-between` : Dispose les éléments en justifiant l'espace entre eux dans un conteneur flex.

- `.justify-center` : Centre les éléments horizontalement dans un conteneur flex.

- `.justify-right` : Alignes les éléments à droite dans un conteneur flex.

- `.btn` : Style de base pour les boutons, incluant des propriétés de dimension, de police, de bordure, et d'interaction comme le pointeur et les transitions pour les interactions de survol.

- `.btn-primary` et `.btn-secondary` : Variantes pour les boutons qui modifient l’apparence pour les états normaux et de survol, en utilisant les variables CSS pour les couleurs qui doivent être définies autre part dans le CSS (par exemple, dans les :root ou dans un autre fichier de variables).

- `.flex-1` : Attribut à un élément un facteur de flexibilité de `1`, lui permettant d'occuper l'espace disponible dans un conteneur flex en proportion avec d'autres éléments flexibles ayant aussi cette classe.

L'utilisation de ces classes à travers le HTML augmente l'efficacité du développement et assure que les styles sont uniformément appliqués, renforçant ainsi la consistance visuelle à travers le site web.


## Header


### Code HTML de la Section Header:
```html
<header>
    <div class="container">
        <nav class="flex items-centre justify-between">
            <div class="left flex justfiy-right">
                <div class="logo">
                    <img src="./images/logo.png" width="50px" alt="logo">
                </div>
                <div>
                    <a href="#">Home</a>
                    <a href="#about">A propos</a>
                    <a href="#service">Services</a>
                    <a href="blog.htm">Blog</a></li>
                </div>
            </div>
            <div class="right">
                <button class="btn btn-primary">Contact</button>
            </div>
        </nav>
    </div>
</header>
```

## CSS a ajouté dans le fichier `styles.css`:
```css
header {
    background-color: var(--bgDark);
}

header nav .left a {
    color: var(--white);
    text-decoration: none;
    /* enlever le soulignement des liens */
    margin-right: 2rem;
    text-transform: uppercase;
    /* mettre en majuscule */
    transition: all .2s ease;
    /* transition sur tous les éléments */
}

header nav .left a:hover {
    color: var(--primary);
}

header nav {
    padding: 2rem 0;
}

header nav .logo {
    margin-right: 3rem;
}
```
### Explication des éléments:

#### 1. Tag `<header>`:
- Le tag `<header>` agit comme un conteneur pour les contenus introductifs ou les éléments de navigation. C'est un élément sémantique qui indique que le contenu à l'intérieur est en rapport avec l'introduction ou la navigation du site web.

#### 2. Conteneur Principal (`<div class="container">`):
- **`class="container"`**: Ce div sert de conteneur avec une largeur maximale et un centrage adaptatifs, assurant que le contenu de l'en-tête reste centré et esthétiquement disposé.

#### 3. Navigation (`<nav class="flex items-centre justify-between">`):
- **`class="flex items-centre justify-between"`** : Le `nav` utilise Flexbox pour un layout flexible des éléments intérieurs. Les enfants directs sont positionnés de sorte qu'il y ait un espace entre chaque élément (`justify-between`) et qu'ils soient alignés verticalement au centre (`items-centre`).

#### 4. Partie Gauche du Menu (`<div class="left flex justfiy-right">`):
- **`class="left flex justify-right"`** Contient le logo et la navigation principale.
  - **Logo** (`<div class="logo"><img src="./images/logo.png" alt="logo">`): Logotype du site, essentiel pour la marque. L'image est destinée à être reconnue facilement et à renforcer l'identité visuelle.
  - **Liens de Navigation** : Liens interactifs (`<a>`) qui dirigent vers différentes sections du site (Accueil, À Propos, Services, Blog). Ces liens sont sans soulignement (`text-decoration: none`), transformés en majuscules (`text-transform: uppercase`) et changent de couleur lorsqu'ils sont survolés.

#### 5. Partie Droite du Menu (`<div class="right">`):
- **`<button class="btn btn-primary">Contact</button>`**: Un bouton pour contact ou action principale, stylisé par les classes `btn` et `btn-primary` qui contrôlent l’apparence visuelle du bouton, rendant celui-ci immédiatement identifiable comme un appel à l'action.

## Section hero

La section "hero", souvent appelée la bannière ou "hero image", est essentielle dans de nombreux sites Web modernes, spécialement les portfolios ou les sites de présentation, car elle capte l’attention de l'utilisateur dès son arrivée sur le site. Voici une analyse détaillée de cette section :

### Code HTML
```html
<section id="hero" class="hero flex items-centre justify-between">
    <div class="left flex-1 justify-center">
        <img src="./images/portrait.png" alt="Profile">
    </div>
    <div class="right flex-1">
        <h1>Pierre-André Vullioud</h1>
        <h2>Je suis un<br> <span>Developeur</span></h2>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloremque illum nam nobis, minima
            laudantium fugit sequi nostrum quod impedit, beatae necessitatibus praesentium optio labore
            nemo!</p>
        <div>
            <a href="">
                <button class="btn btn-secondary">Télécharger mon CV</button>
            </a>
        </div>
    </div>
</section>
```
### Code CSS

```css
#hero {
  padding-top: 2rem;
  padding-bottom: 3rem;
  background-color: var(--bgDark);
}

#hero .left img {
  width: 400px;
}

#hero .right {
  color: var(--white);
  padding: 0 0 0 2rem;
}

#hero .right h2 {
  font-size: 1.5rem;
  font-weight: 100;
  /* graisse de la police */
  line-height: 1.2;
  /* interlignage */
  margin-bottom: 2rem;
}

#hero .right h2 span {
  color: var(--primary);
}

#hero .right p {
  line-height: 1.9;
  margin-bottom: 2rem;
}

#hero .right h1 {
  font-size: 2rem;
  font-weight: 400;
  margin-bottom: 0.5rem;
  margin-top: 2rem;
  color: var(--primary);
}
```

### Explication des éléments:

#### 1. Tag `<section>`:
- **`<section id="hero" class="flex items-centre justify-between">`**: 
  - **id="hero"**: L'identifiant "hero" est utilisé pour le ciblage par des liens internes.
  - **class="flex items-centre justify-between"**: Les classes appliquées ici sont  utilisées pour le positionnement et l'alignement des éléments à l'intérieur de la section avec CSS flexbox. 
    - **"flex"** active flexbox, un modèle de layout CSS conçu pour structurer les éléments de manière efficace même quand leurs tailles sont inconnues ou dynamiques.
    - **"items-centre"** et **"justify-between"** sont des propriétés flexbox qui alignent les éléments verticalement au centre et distribuent l’espace entre les enfants horizontalement.

#### 2. Division Gauche
- **`<div class="left flex-1 justify-center">`**:
  - **class="left flex-1 justify-center"**: 
    - **"left"** est utilisée pour spécifier des styles.
    - **"flex-1"** attribue une croissance flexible, permettant à cet élément de prendre tout l'espace disponible.
    - **"justify-center"** centre les éléments (ici l'image) dans le conteneur flex sur l'axe principal.
  - **`<img src="./images/portrait.png" alt="Profile">`**: Affiche une image de profil, avec un chemin relatif et une description alternative pour l'accessibilité et le SEO.

#### 3. Division Droite
- **`<div class="right flex-1">`**:
  - **class="right flex-1"**: Semblable à la div gauche, cette classe permet à cet élément de s'étendre également.
  - **`<h1>Pierre-André Vullioud</h1>`**: titre principal
  - **`<h2>Je suis un<br><span>Developeur</span></h2>`**:
    - **`<br>`**: Saut de ligne pour une meilleure présentation du texte.
    - **`<span>`**: Utilisé pour appliquer un style ou autre spécificité via CSS à une partie du titre.
  - **`<p>`**: Un paragraphe de text
  - **`<div>`** contenant **`<a>`** et **`<button>`**: Un bouton pour télécharger le CV, 




## Section About

### Code HTML
```html
<section id="about">
    <div class="container flex items-centre">
        <div class="left flex-1">
            <h2>A propos de <span>moi</span></h2>
            <h3>Hello!</h3>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque adipisci distinctio obcaecati aliquid,
                quia tempora quis optio repudiandae officia earum?
                Lorem ipsum dolor sit amet consectetur, adipisicing elit.
            </p>
            <div class="flex socials">
                <a href="#"><img src="./images/facebook.png"></a>
                <a href="#"><img src="./images/instagram.png"></a>
                <a href="#"><img src="./images/reddit.png"></a>
            </div>
        </div>
        <div class="right flex-1 justify-right">
            <img src="./images/portrait2.png" height="400px" alt="profile pic">
        </div>
    </div>
</section>
```
### Code CSS

```css
#about h2 {
    margin-bottom: 1rem;
    font-size: 2rem;
    font-weight: 600;
}

#about h2 span {
    color: var(--primary);
}

#about p {
    font-family: 'Lato', sans-serif;
    color: var(--secondary);
    line-height: 1.9rem;
    margin-bottom: 2rem;
}

/*about section*/

#about .socials a {
    display: flex;
    align-items: center;
    /* centre les éléments sur l'axe vertical */
    justify-content: center;
    /* centre les éléments sur l'axe horizontal */
    width: 2rem;
    margin-right: 0.8rem;
    border-radius: 50%;
    /* crée un rond */
}

#about .socials a:hover {
    background: var(--primary);
}

#about .socials a img {
    width: 2rem;
}

#about .right img {
    width: 100%;
}
```

### Explication des éléments:

#### 1. Tag `<section>`:
- **`<section id="about">`**:
  - **id="about"**: Identifiant unique pour cette section permettant un ciblage spécifique via CSS/JavaScript ou des liens internes.

#### 2. Conteneur principal (`<div class="container flex items-centre">`):
- **class="container flex items-centre"**:
  - **"container"** est généralement utilisé dans le design web pour indiquer un conteneur qui enveloppe son contenu dans une largeur maximale spécifique, facilitant ainsi un layout cohérent et centré.
  - **"flex"** et **"items-centre"** sont des classes de Flexbox utilisées pour aligner horizontalement tous les enfants (éléments internes) au centre de la section.

#### 3. Division Gauche (Left division):
- **`<div class="left flex-1">`**:
  - **"flex-1"** permet à ce bloc de s'adapter et d'occuper tout l'espace disponible en proportion avec les autres éléments flexibles dans le conteneur.
  - **`<h2>A propos de <span>moi</span></h2>`**: Titre principal pour la section, avec une partie ("moi") mise en valeur via un style différent grâce à l'élément `<span>`.
  - **`<p>`**: Paragraphes de texte offrant un aperçu biographique ou professionnel. Le contenu factice "Lorem ipsum" est utilisé ici en place du vrai texte.
  - **`<div class="flex socials">`**: Offre des liens vers des profils de médias sociaux, intégrant les icônes dans un conteneur avec une propriété flex pour une disposition alignée et responsive.
    - **`<a>`** avec **`<img>`**: Liens vers des réseaux sociaux avec des images servant d'icônes.

#### 4. Division Droite (Right division):
- **`<div class="right flex-1 justify-right">`**:
  - **"justify-right"** suggère une mise en page où le contenu (ici, une image) est justifié à droite du conteneur flex.
  - **`<img src="./images/portrait2.png" height="400px" alt="profile pic">`**: Image de profil, probablement différente de celle dans la section "hero", offrant un aperçu plus formel ou alternatif de l'individu.

## Services

### Code HTML
```html
<section id="services">
    <div class="container">
        <h2 class="services-head">Mes Services</h2>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. ...</p>
        <div class="card-grid">
            <div class="card">
                <img src="./images/cisor.svg">
                <h2>Graphic Design</h2>
                <p>Lorem ipsum dolor sit amet consectetur, ...</p>
            </div>
            <div class="card">
                <img src="./images/pen.svg">
                <h2>Web Development</h2>
                <p>Lorem ipsum dolor sit amet consectetur, ...</p>
            </div>
            <div class="card">
                <img src="./images/valise.svg">
                <h2>Content Writing</h2>
                <p>Lorem ipsum dolor sit amet consectetur, ...</p>
            </div>
        </div>
    </div>
</section>
```

### Code CSS
```css
/*services section*/
#services {
    background: rgb(17, 17, 17)
}

.services-head {
    color: rgb(10, 9, 9);
    text-align: center;
    margin-bottom: 1rem;
    line-height: 0.5rem;
    color: var(--primary);
}

.services-head+p {
    color: var(--white);
    font-family: 'Lato', sans-serif;
    margin-bottom: 1rem;
    text-align: center;
    margin-bottom: 6rem;
    font-weight: 400;
}

.card img {
    width: 3rem;
    background: white;
}

#services .card-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    /* 3 colonnes de largeur égale */
    column-gap: 2rem;
    /* espace entre les colonnes */
}

#services .card-grid .card {
    background: var(--white);
    padding: 3rem 2rem;
    position: relative;
    text-align: center;
    transition: all .2s ease;
}

#services .card-grid .card img {
    position: absolute;
    top: -1.5rem;
    left: 50%;
    transform: translateX(-50%);
    color: var();
}

#services .card-grid .card h2 {
    font-weight: 600;
    font-size: 1.2rem;
    margin-bottom: 0.5rem;
}

#services .card-grid .card p {
    font-family: 'Lato', sans-serif;
    color: var(--seconday);
    line-height: 1.6;
}

#services .card-grid .card:hover {
    background: var(--primary);
}

#services .card-grid .card:hover h2 {
    color: var(--white);
}

#services .card-grid .card:hover p {
    color: var(--white);
}
```

### Explication des éléments:

#### 1. Tag `<section>`:
- **`<section id="services">`**:
  - **id="services"**: Un identifiant unique pour permettre un ciblage spécifique, que ce soit par des feuilles de style CSS ou pour des liens internes.

#### 2. Conteneur principal (`<div class="container">`):
- **class="container"**: Utilisé pour centrer le contenu et le maintenir dans une largeur maximale.

#### 3. Titre de la section:
- **`<h2 class="services-head">Mes Services</h2>`**:
  - **class="services-head"**: Classe CSS qui utilisée pour appliquer des styles spécifiques au titre.

#### 4. Description des services:
- **`<p>`**: Paragraphe de texte

#### 5. Grille de cartes (`<div class="card-grid">`):
- **class="card-grid"**: Utilisé pour définir un layout en grille

### Cartes individuelles de services:
Chaque carte (élément `<div class="card">`) représente un service spécifique.

- **Images (`<img src="...">`)**: Chacune illustre le service offert. Les images sont des symboles
- **Titres de service (`<h2>`)**: Ils indiquent le type de service proposé.
- **Descriptions (`<p>`)**: paragraphe

Mise en page classique en card


# Fichier CSS styles.css complet

```css
/* Importation des fichiers */
@import 'utilities.css';
@import 'responsive.css';

:root {
    /* Déclaration des variables */
    --primary: rgb(29, 221, 189);
    --bgDark: rgb(12, 12, 12);
    --white: rgb(250, 250, 250);
    --secondary: rgb(0, 59, 50);
    --bgLight: rgb(190, 181, 181);
}

/* Reset des styles */
* {
    padding: 0;
    margin: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Poppins', sans-serif;
    /* Definir la police par défaut */
    color: var(--bgDark);
}

.container {
    max-width: 1152px;
    /* largeur max du container */
    padding: 0 15px;
    margin: 0 auto;
    /* centrer le container */
}

section {
    padding: 6rem;
}

header {
    background-color: var(--bgDark);
}

header nav .left a {
    color: var(--white);
    text-decoration: none;
    /* enlever le soulignement des liens */
    margin-right: 2rem;
    text-transform: uppercase;
    /* mettre en majuscule */
    transition: all .2s ease;
    /* transition sur tous les éléments */
}

header nav .left a:hover {
    color: var(--primary);
}

header nav {
    padding: 2rem 0;
}

header nav .logo {
    margin-right: 3rem;
}


#hero {
    padding-top: 2rem;
    padding-bottom: 3rem;
    background-color: var(--bgDark);
}

#hero .left img {
    width: 400px;
}

#hero .right {
    color: var(--white);
    padding: 0 0 0 2rem;
}

#hero .right h2 {
    font-size: 1.5rem;
    font-weight: 100;
    /* graisse de la police */
    line-height: 1.2;
    /* interlignage */
    margin-bottom: 2rem;
}

#hero .right h2 span {
    color: var(--primary);
}

#hero .right p {
    line-height: 1.9;
    margin-bottom: 2rem;
}

#hero .right h1 {
    font-size: 2rem;
    font-weight: 400;
    margin-bottom: 0.5rem;
    margin-top: 2rem;
    color: var(--primary);
}


/*about section*/

#about h2 {
    margin-bottom: 1rem;
    font-size: 2rem;
    font-weight: 600;
}

#about h2 span {
    color: var(--primary);
}

#about p {
    font-family: 'Lato', sans-serif;
    color: var(--secondary);
    line-height: 1.9rem;
    margin-bottom: 2rem;
}

/*about section*/

#about .socials a {
    display: flex;
    align-items: center;
    /* centre les éléments sur l'axe vertical */
    justify-content: center;
    /* centre les éléments sur l'axe horizontal */
    width: 2rem;
    margin-right: 0.8rem;
    border-radius: 50%;
    /* crée un rond */
}

#about .socials a:hover {
    background: var(--primary);
}

#about .socials a img {
    width: 2rem;
}

#about .right img {
    width: 100%;
}

/*services section*/
#services {
    background: rgb(17, 17, 17)
}

.services-head {
    color: rgb(10, 9, 9);
    text-align: center;
    margin-bottom: 1rem;
    line-height: 0.5rem;
    color: var(--primary);
}

.services-head+p {
    color: var(--white);
    font-family: 'Lato', sans-serif;
    margin-bottom: 1rem;
    text-align: center;
    margin-bottom: 6rem;
    font-weight: 400;
}

.card img {
    width: 3rem;
    background: white;
}

#services .card-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    /* 3 colonnes de largeur égale */
    column-gap: 2rem;
    /* espace entre les colonnes */
}

#services .card-grid .card {
    background: var(--white);
    padding: 3rem 2rem;
    position: relative;
    text-align: center;
    transition: all .2s ease;
}

#services .card-grid .card img {
    position: absolute;
    top: -1.5rem;
    left: 50%;
    transform: translateX(-50%);
    color: var();
}

#services .card-grid .card h2 {
    font-weight: 600;
    font-size: 1.2rem;
    margin-bottom: 0.5rem;
}

#services .card-grid .card p {
    font-family: 'Lato', sans-serif;
    color: var(--seconday);
    line-height: 1.6;
}

#services .card-grid .card:hover {
    background: var(--primary);
}

#services .card-grid .card:hover h2 {
    color: var(--white);
}

#services .card-grid .card:hover p {
    color: var(--white);
}

/*footer */

footer {
    background: var(--bgDark);
    color: var(--white);
    padding: 1rem 0.5rem;
    border-top: 2px solid var(--primary);
}
```
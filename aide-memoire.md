# Aide mémoire HTML

## Balises Meta
- `<meta>` : définit des métadonnées sur le document

## Balises de lien
- `<link>` : permet de relier le document HTML à une feuille de style externe ou à une police de caractère externe

## Balises de titre
- `<title>` : définit le titre du document

## Balises de structure HTML
- `<html>` : débute et termine le document HTML
- `<head>` : contient les éléments d'en-tête du document, tels que les balises meta et link
- `<body>` : contient tout le contenu visible du document HTML

## Balises de conteneur
- `<header>` : représente l'en-tête du document ou de la section
- `<main>` : représente le contenu principal du document
- `<section>` : représente une section dans un document
- `<footer>` : représente le pied de page du document

## Balises de navigation
- `<nav>` : représente une section de navigation dans le document

## Balises de contenu
- `<div>` : représente une division ou une section générique d'un document
- `<h1>`, `<h2>`, `<h6>` : représentent les titres de différents niveaux dans le document
- `<p>` : représente un paragraphe de texte

## Balises d'image
- `<img>` : permet d'inclure une image dans le document

## Balises de lien
- `<a>` : représente un lien hypertexte

## Balises de liste
- `<ul>`, `<li>` : permettent de créer des listes non ordonnées

## Balises de bouton
- `<button>` : représente un bouton interactif

# Aide mémoire CSS

## Boutons

- `background-color`: couleur de fond du bouton
- `border`: bordure du bouton
- `color`: couleur du texte du bouton
- `cursor`: curseur au survol du bouton
- `font-size`: taille de la police du bouton
- `font-weight`: épaisseur de la police du bouton
- `margin-top`: marge supérieure du bouton
- `padding`: espacement interne du bouton
- `text-transform`: transformation du texte en majuscules
- `transition`: transition au survol du bouton
  - `transition-property`: propriété sur laquelle s'applique la transition
  - `transition-duration`: durée de la transition
  - `transition-timing-function`: fonction de temporisation de la transition

## Conteneurs flex

- `display`: type d'affichage (`flex`)
- `flex`: facteur de flexibilité
- `flex-direction` : type d'alignement ligne ou colonne
- `align-items`: aligner les éléments au centre
- `justify-content`: aligner les éléments et répartir l'espace

## Couleurs

- `background-color`: couleur de fond
- `color`: couleur du texte
- `border-color`: couleur de la bordure
- `rgb()`: système de notation des couleurs en fonction des valeurs Rouge, Vert, Bleu

## Gestion du conteneur

- `box-sizing`: modèle de boîte pour le dimensionnement
- `margin`: marges extérieures
- `max-width`: largeur maximale du conteneur
- `padding`: espacement interne
- `text-decoration`: style de soulignement du texte
- `text-transform`: transformation du texte en majuscules
- `width`: largeur d'un élément

## Polices

- `font-family`: famille de police
- `font-size`: taille de la police
- `font-weight`: graisse de la police
- `line-height`: hauteur de ligne
- `sans-serif`: famille de police sans empattement

## Positionnement

- `position`: positionnement d'un élément dans le document
- `top`: distance par rapport au bord supérieur
- `left`: distance par rapport au bord gauche
- `transform`: transformation d'un élément
- `translateX()`: translation horizontale

## Transition

- `transition`: transition d'un état à un autre
- `ease`: fonction de temporisation de la transition

## Variables CSS

- `:root`: définition des variables de couleur

# Aide mémoire Flex
Le modèle de boîte flexible, ou Flexbox, en CSS est un outil puissant pour aligner et ordonner des éléments à l'intérieur d'un conteneur de façon efficace, même lorsque leurs tailles sont inconnues ou dynamiques. Voici un aide-mémoire pratique pour vous aider à utiliser Flexbox :

## Concepts de base
- **Container flex**: Le conteneur qui utilise `display: flex;` ou `display: inline-flex;` pour organiser ses enfants.
- **Flex items**: Les éléments enfants directs du conteneur flex.

## Propriétés du conteneur flex
1. **display**: 
   - `display: flex;` crée un conteneur de bloc flex.

   
2. **flex-direction**:
   - `row` (défaut): les éléments sont disposés dans l’ordre du texte.
   - `row-reverse`: les éléments sont disposés dans l’ordre inverse du texte.
   - `column`: les éléments sont disposés de haut en bas.
   - `column-reverse`: les éléments sont disposés de bas en haut.

3. **flex-wrap**:
   - `nowrap` (défaut): tous les éléments sont alignés sur une seule ligne ou colonne.
   - `wrap`: les éléments s’enroulent sur plusieurs lignes ou colonnes si nécessaire.
   - `wrap-reverse`: les éléments s'enroulent et l'ordre des lignes est inversé.

4. **justify-content**: aligne les éléments horizontalement et distribue l'espace libre.
   - `flex-start`: les éléments sont alignés au début du conteneur.
   - `flex-end`: les éléments sont alignés à la fin du conteneur.
   - `center`: les éléments sont centrés dans le conteneur.
   - `space-between`: les éléments sont uniformément distribués; le premier élément est au début, le dernier à la fin.
   - `space-around`: les éléments sont uniformément distribués avec un espace égal autour d'eux.

5. **align-items**: aligne les éléments verticalement.
   - `flex-start`: les éléments sont alignés au haut du conteneur.
   - `flex-end`: les éléments sont alignés au bas du conteneur.
   - `center`: les éléments sont centrés verticalement dans le conteneur.
   - `baseline`: les éléments sont alignés selon la ligne de base de leur texte.
   - `stretch` (défaut): les éléments s'étirent pour remplir le conteneur (verticalement).

6. **align-content**: aligne les lignes de contenu à l'intérieur du conteneur lorsque `flex-wrap` est `wrap`.
   - `flex-start`: les lignes sont empaquetées vers le haut du conteneur.
   - `flex-end`: les lignes sont empaquetées vers le bas du conteneur.
   - `center`: les lignes sont centrées dans le conteneur.
   - `space-between`: les lignes sont uniformément distribuées.
   - `space-around`: chaque ligne a un espace égal autour.
   - `stretch` (défaut): les lignes s'étirent pour remplir l'espace restant.

## Propriétés des éléments flex
1. **flex-grow**: Définit l'expansion des éléments; comment ils vont grandir par rapport aux autres autour.
2. **flex-shrink**: Définit comment l'élément doit rétrécir par rapport aux autres.
3. **flex-basis**: Définit la dimension initiale d'un élément avant l'espace restant est distribué.
4. **flex**: raccourci pour `flex-grow`, `flex-shrink` et `flex-basis`.
5. **align-self**: permet de modifier l'alignement individuel d'un élément (p. ex. override `align-items`).

## Exemple de base
```css
.container {
  display: flex;
  justify-content: center; /* Centre les éléments horizontalement */
  align-items: center; /* Centre les éléments verticalement */
}
```

# Structure de la page 
- html
  - head
    - meta
    - link
    - link
    - link
    - title
  - body
    - header
      - div
        - nav
          - div
            - div
              - img
            - div
              - a
              - a
              - a
              - a
          - div
            - button
    - main
      - section
        - div
          - div
            - img
          - div
            - h6
            - h1
              - span
            - p
            - div
              - a
                - button
      - section
        - div
          - div
            - h1
              - span
            - h2
            - p
            - div
              - a
                - img
              - a
                - img
              - a
                - img
          - div
            - img
      - section
        - div
          - h1
          - p
          - div
            - div
              - img
              - h2
              - p
            - div
              - img
              - h2
              - p
            - div
              - img
              - h2
              - p
    - footer

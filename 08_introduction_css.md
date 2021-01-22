[#](#introduction-in-css) Introduction au CSS
=========================================

[#](#syntaxe) Syntaxe
-------------------

Le HTML décrit la structure d'un site web et est comme le squelette d'un corps. Le CSS décrit l'apparence, le style de ces éléments HTML. Seul, sans HTML correspondant, le CSS ne fonctionne pas ! CSS signifie "Cascading Style Sheets" et est généralement lié à un fichier HTML en tant que fichier `.css` séparé.

Dans la [Introduction HTML](../03_introduction_html), vous avez appris que les éléments HTML sont décrits par des balises, par exemple `<body>` ou `<div>` etc. et peuvent être complétés par `class` et `id`. En CSS, vous pouvez maintenant utiliser le **sélecteur** pour définir les éléments et les attributs du HTML qui doivent être sélectionnés et conçus.

Pour ce sélecteur, vous pouvez ensuite définir une **stylerule** (règle de style) avec des parenthèses frisées. Cette règle contient plusieurs **propriétés**, auxquelles est attribuée une **valeur**.

### Exemple

    sélecteur {
      propriété : valeur ;
      propriété : valeur ;
      propriété : valeur ;
    }
    

Notation correcte

Après une propriété, il doit toujours y avoir un deux-points `:` et après la valeur un point-virgule `;`.

[#](#interplay-with-html) Interaction avec le HTML
---------------------------------------------------

Pour que le HTML et le CSS puissent se parler, vous devez lier votre fichier CSS dans le fichier HTML.

    <!doctype html>
    <html lang="en">
      < tête>
        <link rel="stylesheet" type="text/css" href="css/style.css">
      </head>
    </html>
    

Dans l'exemple ci-dessus, le fichier `style.css` est situé dans le sous-répertoire `css`. Si le fichier CSS était situé dans le répertoire racine, par exemple, vous écririez `href="style.css"` dans l'attribut `href`.

Grâce à la balise "link" de la section "head" de notre fichier HTML, vous pouvez maintenant commencer la mise en forme et la mise en page avec le CSS.

[#](#sélecteurs) Sélecteurs
-------------------------

! [Sélecteurs CSS](/assets/img/css-selectors.1f006427.png) Image : internetingishard.com

### [#](#tag-selector) Tag Selector

Vous voulez colorier et mettre en gras une section de texte `<p>` dans un document HTML.

    <p>
      Voici un exemple de phrase qui a été stylisée avec le CSS.
    </p>
    

En CSS, on écrit :

    p {
      couleur : tomate ;
      poids de la police : gras ;
    }
    

**résultat**

* * *

Il s'agit d'un exemple de phrase stylisée avec le CSS.

* * *

### [#](#sélecteur de classe) Sélecteur de classe

Le sélecteur de balises peut aussi parfois être très limitatif. Peut-être ne voulez-vous pas que toutes les sections de texte soient définies dans un seul style. C'est là qu'une **classe** (class) devient utile.

    <p class="highlighted-text">
      Il s'agit d'un exemple de phrase stylisée avec le CSS.
    </p>
    

Au lieu de styliser la balise `p` très générique, vous pouvez affecter exclusivement les éléments HTML qui ont une classe spécifique avec mon style :

    .highlighted-text {
      couleur : tomate ;
      poids de la police : gras ;
    }
    

Orthographe correcte

En CSS, une classe a toujours un point ".`" devant le sélecteur, en HTML, on ne l'écrit pas. HTML : "ma classe", CSS : "ma classe".

### [#](#id-selector) ID selector

Les ID ne doivent être utilisés en HTML que s'ils sont nécessaires pour les formulaires ou les "ancres". Par exemple, un clic permet d'accéder à une zone spécifique d'une page web. La plupart du temps, cependant, les cours sont suffisants.

    <p id="very-specific-area">
      Il s'agit d'un exemple de phrase stylisée avec le CSS.
    </p>
    

    #toutes les zones spécifiques {
      couleur : tomate ;
      poids de la police : gras ;
    }
    

Orthographe correcte.

En CSS, un ID a toujours un dièse "#" devant le sélecteur. En HTML, vous n'écrivez pas ce hachage. HTML : `my-id`, CSS : `#my-id`.

[#](#selecteurs-combine) Combiner les sélecteurs
-------------------------------------------------

### [#](#tags-mit-classes) Étiquettes avec classes

Le fichier HTML suivant doit être mis en forme.

    <p class="highlighted">
      Je suis une section de texte qui apparaît en surbrillance.
    </p>
    
    <a class="highlighted" href="https://duckduckgo.com">
      Je suis un lien qui mène à un moteur de recherche.
    </a>
    

Maintenant, seuls les liens "a>" avec la classe "mis en évidence" devraient être affichés différemment.

    /* Le sélecteur CSS suivant serait utilisé pour sélectionner <p> et <a> */.
    
    .highlighted {
      couleur : bleu royal ;
      style de police : italique ;
    }
    
    /* Avec le sélecteur CSS suivant, seul <a> avec la classe "surligné" serait sélectionné */
    
    a.highlighted {
      couleur : tomate ;
    }
    

**résultat**

* * *

Je suis une section de texte qui apparaît en surbrillance.

[Je suis un lien qui mène à un moteur de recherche](https://duckduckgo.com)

* * *

### [#](#multiple-classes) Multiple Classes

Vous pouvez styliser les éléments HTML s'ils ont une certaine combinaison de Classes.

    <p class="box">
      Cette case apparaît normalement.
    </p>
    
    <p class="box highlighted">
      Cette case apparaît en surbrillance.
    </p>
    

    .box {
      couleur de fond : blanc fumé ;
      rembourrage : 1rem ;
      largeur de la bordure : 10px ;
      style frontière : solide ;
      couleur de la bordure : bleu royal ;
      couleur : noir ;
      poids de la police : normal ;
    }
    
    .box.highlighted {
      couleur de la bordure : tomate ;
      couleur : tomate ;
      poids de la police : gras ;
    }
    

**résultat**

* * *

Cette case semble normale.

Cette case apparaît en surbrillance.

* * *

Orthographe correcte

En HTML, vous pouvez simplement séparer plusieurs classes avec un espace.

Exemple : `<p class="box highlighted"></p>`

En CSS, cependant, cet espacement doit être omis, sinon cela ne veut pas dire la même chose. Si vous écrivez "box.highlighted" en CSS, vous sélectionnez **un** élément HTML avec les classes "box" et "highlighted". Ce principe est appelé "chaînage". Cependant, si vous écrivez " .box .highlighted " en CSS, cela signifie que vous recherchez un enfant de la classe " highlighted " dans l'élément HTML avec la classe " box ". Ce principe est appelé "nesting".

[#](#principes importants) Principes importants
---------------------------------------------

Le CSS suit trois concepts de base. [Spécificité](https://developer.mozilla.org/en-US/docs/Web/CSS/Specificity) , [Héritage](https://developer.mozilla.org/de/docs/Web/CSS/Vererbung) et la [Cascade](https://developer.mozilla.org/en-US/docs/Web/CSS/Cascade)

### [#](#spécificité) Spécificité

La spécificité est un ensemble de règles que les navigateurs utilisent pour déterminer quelles sont les valeurs de propriété les plus importantes et qui sont appliquées, ou qui sont annulées.

En règle générale, vous pouvez vous souvenir : Plus vous sélectionnez un élément HTML dans le CSS de manière spécifique et précise, plus il est probable que ces styles seront visibles. Par exemple, dans notre exemple, ".souligné" sera remplacé par "a.souligné" parce qu'il est plus spécifique.

(### [#](#héritage) Héritage

L'héritage signifie essentiellement que des valeurs peuvent être héritées d'un élément parent. Tout au long de ce cours, vous travaillerez avec ce principe.

### [#](#cascade) Cascade

En termes simples, la cascade dans le CSS signifie que l'ordre des règles du CSS est important. Si deux règles aussi spécifiques sont définies, c'est celle qui vient en dernier dans le CSS qui sera utilisée. C'est d'ailleurs vrai pour de nombreux fichiers CSS. L'ordre est donc important !

[#](#modèle de boîte) Modèle de boîte
-------------------------

Lorsque vous utilisez le CSS et le HTML, de nombreuses "boîtes" sont créées sur votre écran. Dans les CSS, une telle boîte peut avoir une largeur, une hauteur, un contour, une distance intérieure et extérieure.

! [Modèle de boîte CSS](/assets/img/css-box-model.73a525e2.png) Image : internetingishard.com

Imaginez une boîte de 500 pixels de large et 500 pixels de haut. Si vous ajoutez maintenant une "marge" (distance extérieure) de 10 pixels, les dimensions de la boîte passent à 510 pixels. Cela peut entraîner des effets secondaires désagréables dans la mise en page. Cependant, vous pouvez contrôler cela avec la propriété "box-sizing".

Pour faciliter la mise en page, il est utile de sélectionner un modèle de boîte uniforme et de l'appliquer à tous les éléments. Avec le sélecteur "*", vous pouvez influer sur cette situation. L'astérisque "*" indique au CSS que "cela affecte tout".

    * {
      taille de la boîte : border-box ;
    }
    

Bien que la propriété "box-sizing" connaisse les valeurs "content-box", "padding-box", "border-box" et "margin-box", la plupart du temps vous n'avez besoin que de "content-box" et "border-box". Beaucoup de gens peuvent s'en sortir avec une simple "boîte à lettres".

### [#](#differences-between-content-box-and-border-box) Différences entre content-box et border-box

Regardez le code suivant.

    .box {
      largeur : 300px ;
      rembourrage : 1rem ;
      marge inférieure : 1rem ;
      largeur de la bordure : 10px ;
      style frontière : solide ;
      couleur de la bordure : bleu royal ;
    }
    
    .content-box {
      taille de la boîte : content-box ;
    }
    
    .border-box {
      taille de la boîte : border-box ;
    }
    

    <div class="box content-box">
      Je suis une boîte A avec un contenu
    </div>
    
    <div class="box border-box">
      Je suis une boîte B avec un style border-box
    </div>
    

**résultat**

* * *

Je suis la boîte A qui a le style de la boîte de contenu.

Je suis une boîte B qui a le style d'une border-box.

* * *

La boîte A et la boîte B diffèrent en largeur, bien qu'une largeur fixe de 300 pixels soit fixée pour les deux avec la classe " .box ".

#### [#](#pourquoi les boîtes sont-elles de largeur différente) Pourquoi les boîtes sont-elles de largeur différente ?

Content-box" ajoute les valeurs des propriétés "padding" et "border-width" à la largeur de 300 pixels du contenu. Le fait que `padding : 10px;` et `border-width : 10px;` donne une largeur de 340 pixels - les valeurs des propriétés doivent être comptées deux fois, car elles sont appliquées sur les deux côtés.

La largeur de la "border-box" est de 300 pixels, ce qui est défini par le CSS. La largeur du contenu (dans ce cas le texte) n'est donc pas de 300 pixels **plus** `padding` et `border-width` comme dans l'exemple précédent, mais de 300 pixels **moins** les deux propriétés. La boîte fait donc 300 pixels de large au total, mais le contenu ne fait que 260 pixels.

! [Box sizing](/assets/img/box-sizing-content-box.09f48a7d.png) Image : internetingishard.com

(les biens les plus importants) Les biens les plus importants
-----------------------------------------------------------

### [#](#mise en page) Mise en page

| Propriété | Signification |
| --- | --- |
| `display` | layout behavior of elements. Plus : [Mise en page CSS](/guide/09_css_layout/) |
| position` | positionnement des éléments. Plus : [Positionnement et chemins](/guide/11_chemins) |
| `margin` | distance d'un élément de bloc vers l'extérieur |
| `padding` | distance d'un élément de bloc vers l'intérieur |
| `border` | contour d'un élément de bloc |

### [#](#texte et couleurs) Texte et couleurs

| propriété | signification |
| --- | --- |
| `font-family` | font |
| `font-size` | font-size |
| "couleur" | couleur de la police
| | couleur d'arrière-plan / image d'arrière-plan

Avec ces propriétés, vous pouvez déjà concevoir beaucoup de choses avec le CSS. Les possibilités sont presque illimitées, il est donc préférable de consulter la [Référence CSS](https://cssreference.io/) ou la [Feuille de calcul CSS](https://devhints.io/css) pour voir ce qui est possible. Au cours de ce cours, vous apprendrez à connaître d'autres propriétés.

Liens

* [Référence CSS avec exemples](https://cssreference.io/)
* [Feuille de calcul CSS](https://devhints.io/css)
* [Exemple interactif des différences entre content-box et border-box](https://codepen.io/kilianso/full/GRoGNBy)

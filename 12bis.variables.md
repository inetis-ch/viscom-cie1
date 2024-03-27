# 12 bis. Variables CSS

Les variables CSS sont des entités définies pour contenir des valeurs pouvant être utilisées dans tout le document. Elles sont créées en initiant des propriétés personnalisées telles que `--main-color: noir`; et sont accessibles en utilisant la syntaxe `var()` tel que color: `var(--main-color)`;. Ces propriétés permettent de réduire la répétition de la valeur et simplifient la maintenance du code.

```css
    :root {
        --main-color: black;
        --main-bg-color: white;
    }

    body {
        color: var(--main-color);
        background-color: var(--main-bg-color);
    }
```

Design system
Dans les frameworks CSS tels que Bootstrap, les variables facilitent le partage d'un design de base à travers les éléments. Prenez la classe .bg-danger, qui change la couleur d'arrière-plan d'un élément en rouge et sa propre couleur en blanc. Dans ce premier projet, vous allez construire quelque chose de similaire.

```css
    :root {
        --primary: #007bff;
        --secondary: #6c757d;
        --success: #28a745;
        --error: #dc3545;
        --link: #007bff;
    }

    .btn {
        padding: 0.5rem 1rem;
        border-radius: 0.25rem;
        font-size: 1rem;
        cursor: pointer;
    }

    .btn-primary {
        color: white;
        background-color: var(--primary);
    }

    .btn-secondary {
        color: white;
        background-color: var(--secondary);
    }

    .btn-success {
        color: white;
        background-color: var(--success);
    }

    .btn-error {
        color: white;
        background-color: var(--error);
    }

    .btn-link {
        color: var(--link);
        background-color: transparent;
    }
```
La classe `btn` contient les styles de base pour tous les boutons. Les variations de couleurs sont définies au niveau `:root` du document. 

Par exemple, si demain vous décidez que la valeur de la propriété personnalisée `--error` est trop terne pour une couleur rouge, vous pouvez facilement la changer en #f00000. Une fois que vous l'avez fait tous les éléments utilisant cette propriété personnalisée sont mis à jour

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>CSS Variables - Button Variations</title>
  </head>
  <body>
    <section>
      <div class="container">
        <h1 class="title">CSS Color Variations</h1>
        <div class="btn-group">
          <button class="btn btn-primary">Primary</button>
          <button class="btn btn-secondary">Secondary</button>
          <button class="btn btn-link">Link</button>
          <button class="btn btn-success">Success</button>
          <button class="btn btn-error">Error</button>
        </div>
      </div>
    </section>
  </body>
</html>
```


:hand: Tâches Remplacer les couleurs de votre site web par des variables CSS.


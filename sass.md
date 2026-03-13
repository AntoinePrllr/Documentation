# Guide complet : SASS (Syntactically Awesome Style Sheets)

## 1. Qu'est‑ce que Sass ?

**Sass** est un **préprocesseur CSS** qui ajoute des fonctionnalités
avancées au CSS classique :

-   variables
-   imbrication de règles
-   mixins
-   fonctions
-   héritage
-   logique (conditions, boucles)

Le code Sass est ensuite **compilé en CSS classique**, lisible par les
navigateurs.

------------------------------------------------------------------------

# 2. Les deux syntaxes Sass

## SCSS (la plus utilisée)

``` scss
$primary-color: #3498db;

body {
  background: $primary-color;
}
```

-   ressemble beaucoup au CSS
-   utilise **accolades et points-virgules**
-   extension : `.scss`

## Sass (ancienne syntaxe)

``` sass
$primary-color: #3498db

body
  background: $primary-color
```

-   indentation au lieu des `{}`
-   extension : `.sass`

👉 **Aujourd'hui on utilise presque toujours SCSS.**

------------------------------------------------------------------------

# 3. Installation de Sass

### Avec Node.js

``` bash
npm install -g sass
```

### Compiler un fichier

``` bash
sass style.scss style.css
```

### Compiler en continu

``` bash
sass --watch style.scss:style.css
```

------------------------------------------------------------------------

# 4. Variables

Les variables permettent de stocker des valeurs réutilisables.

``` scss
$primary-color: #ff6600;
$font-size: 16px;

body {
  color: $primary-color;
  font-size: $font-size;
}
```

Utilisations fréquentes :

-   couleurs
-   tailles
-   polices
-   espacements

------------------------------------------------------------------------

# 5. Nesting (imbrication)

Permet d'imbriquer les sélecteurs comme en HTML.

``` scss
nav {
  ul {
    list-style: none;
  }

  li {
    display: inline-block;
  }

  a {
    text-decoration: none;
  }
}
```

Compilation CSS :

``` css
nav ul { }
nav li { }
nav a { }
```

------------------------------------------------------------------------

# 6. Parent Selector (&)

Permet de référencer le sélecteur parent.

``` scss
button {
  background: blue;

  &:hover {
    background: red;
  }
}
```

Résultat :

``` css
button:hover {
  background: red;
}
```

------------------------------------------------------------------------

# 7. Partials (fichiers partiels)

Les fichiers Sass peuvent être séparés.

Exemple :

    sass/
      _variables.scss
      _mixins.scss
      _buttons.scss
      style.scss

Les fichiers avec `_` sont appelés **partials**.

------------------------------------------------------------------------

# 8. Import / Use

Ancien système :

``` scss
@import "variables";
```

Nouveau système recommandé :

``` scss
@use "variables";
```

------------------------------------------------------------------------

# 9. Mixins

Les **mixins** permettent de réutiliser des blocs de CSS.

``` scss
@mixin flex-center {
  display: flex;
  justify-content: center;
  align-items: center;
}

.container {
  @include flex-center;
}
```

Avec paramètres :

``` scss
@mixin size($width, $height) {
  width: $width;
  height: $height;
}

.box {
  @include size(200px, 100px);
}
```

------------------------------------------------------------------------

# 10. Héritage avec @extend

Permet de partager des styles.

``` scss
.button {
  padding: 10px;
  border-radius: 5px;
}

.primary-button {
  @extend .button;
  background: blue;
}
```

------------------------------------------------------------------------

# 11. Opérations

Sass permet de faire des calculs.

``` scss
.container {
  width: 100% / 3;
}
```

Exemple :

``` scss
$base: 10px;

.box {
  padding: $base * 2;
}
```

------------------------------------------------------------------------

# 12. Conditions

``` scss
$theme: dark;

body {
  @if $theme == dark {
    background: black;
    color: white;
  } @else {
    background: white;
    color: black;
  }
}
```

------------------------------------------------------------------------

# 13. Boucles

### @for

``` scss
@for $i from 1 through 3 {
  .col-#{$i} {
    width: 100% / 3 * $i;
  }
}
```

------------------------------------------------------------------------

# 14. Lists

``` scss
$sizes: 10px, 20px, 30px;

@each $size in $sizes {
  .m-#{$size} {
    margin: $size;
  }
}
```

------------------------------------------------------------------------

# 15. Maps

``` scss
$colors: (
  primary: #3498db,
  secondary: #2ecc71
);

.button {
  color: map-get($colors, primary);
}
```

------------------------------------------------------------------------

# 16. Fonctions

``` scss
@function double($size) {
  @return $size * 2;
}

.box {
  width: double(20px);
}
```

------------------------------------------------------------------------

# 17. Organisation recommandée

Architecture Sass populaire :

    sass/
    │
    ├── abstracts/
    │   ├── _variables.scss
    │   ├── _mixins.scss
    │
    ├── base/
    │   ├── _reset.scss
    │   ├── _typography.scss
    │
    ├── components/
    │   ├── _buttons.scss
    │   ├── _cards.scss
    │
    ├── layout/
    │   ├── _header.scss
    │   ├── _footer.scss
    │
    └── main.scss

------------------------------------------------------------------------

# 18. Bonnes pratiques

✔ utiliser des variables pour les couleurs\
✔ éviter trop de nesting\
✔ utiliser des partials\
✔ préférer `@use` à `@import`\
✔ structurer les fichiers

------------------------------------------------------------------------

# 19. Sass vs CSS

  Fonction    CSS   Sass
  ----------- ----- ------
  Variables   ❌    ✔
  Nesting     ❌    ✔
  Mixins      ❌    ✔
  Fonctions   ❌    ✔
  Boucles     ❌    ✔

------------------------------------------------------------------------

# 20. Conclusion

Sass permet :

-   d'écrire du CSS **plus propre**
-   de **réutiliser du code**
-   de **structurer les gros projets**
-   d'augmenter la **maintenabilité du style**

Il est utilisé dans la plupart des frameworks modernes.

------------------------------------------------------------------------

**Fin de la documentation Sass**

# L'histoire de Node.js et npm

## Avant Node.js

Pendant longtemps, JavaScript était utilisé uniquement dans les navigateurs web.

Il permettait principalement :

* D'ajouter de l'interactivité aux pages web
* De manipuler le contenu HTML
* De réagir aux actions des utilisateurs

À cette époque, JavaScript ne pouvait pas être exécuté directement sur un ordinateur en dehors d'un navigateur.

---

## La création de Node.js

En 2009, un développeur nommé Ryan Dahl crée Node.js.

Son objectif est de permettre l'exécution de JavaScript en dehors du navigateur.

Grâce à Node.js, JavaScript peut désormais être utilisé pour :

* Créer des serveurs web
* Automatiser des tâches
* Développer des applications complètes
* Exécuter des outils de développement

Cette innovation contribue fortement à la popularité du langage JavaScript.

---

## L'arrivée de npm

Peu après la création de Node.js apparaît npm.

npm signifie :

```text
Node Package Manager
```

Son rôle est de faciliter l'installation et le partage de bibliothèques JavaScript.

Au lieu de télécharger manuellement des fichiers sur Internet, les développeurs peuvent installer une bibliothèque avec une simple commande.

Exemple :

```bash
npm install sass
```

---

## Pourquoi npm a révolutionné le développement

Avant npm, installer une bibliothèque pouvait nécessiter :

* Le téléchargement manuel de fichiers
* Des configurations complexes
* Des mises à jour difficiles

Avec npm, tout est automatisé :

* Installation des bibliothèques
* Gestion des versions
* Mise à jour des dépendances
* Partage des projets entre développeurs

Aujourd'hui, npm est le plus grand registre de paquets au monde avec plusieurs millions de bibliothèques disponibles.

---

## Node.js et les outils modernes

Au fil des années, de nombreux outils populaires ont été construits autour de Node.js et npm :

* Sass
* React
* Vue.js
* Angular
* Vite
* Webpack
* ESLint
* TypeScript

Même lorsqu'un projet est principalement en HTML et CSS, Node.js est souvent utilisé pour installer et exécuter ces outils.

---

## Node.js dans mon projet

Dans ce projet, Node.js n'est pas utilisé pour créer un serveur ou une application backend.

Il est utilisé pour :

* Installer Sass avec npm
* Gérer les dépendances du projet
* Exécuter le script de compilation SCSS vers CSS

Exemple :

```bash
npm install sass
```

Puis :

```bash
npm run sass
```

qui compile automatiquement les fichiers SCSS en CSS.

---

## Quelques dates importantes

| Année       | Événement                                                            |
| ----------- | -------------------------------------------------------------------- |
| 1995        | Création du langage JavaScript                                       |
| 2009        | Création de Node.js par Ryan Dahl                                    |
| 2010        | Développement rapide de npm                                          |
| 2015        | Forte adoption de Node.js dans le développement web moderne          |
| Aujourd'hui | Node.js et npm sont utilisés dans la majorité des projets JavaScript |

---

# À retenir

* JavaScript était initialement limité aux navigateurs web.
* Node.js a été créé en 2009 par Ryan Dahl pour exécuter JavaScript en dehors du navigateur.
* npm signifie Node Package Manager.
* npm permet d'installer et de gérer des bibliothèques facilement.
* Node.js et npm sont aujourd'hui des outils essentiels du développement web moderne.
* Dans ce projet, ils sont utilisés pour installer Sass et automatiser la compilation des fichiers SCSS en CSS.

# Installation de Node.js

## Télécharger Node.js

Télécharger Node.js depuis le site officiel :

https://nodejs.org

Pour un projet classique, il est recommandé d'installer la version **LTS (Long Term Support)**.

Cette version est plus stable et mieux adaptée au développement.

---

## Installation

Lancer l'installateur téléchargé puis suivre les étapes de l'assistant.

Les options par défaut conviennent dans la majorité des cas.

L'installation ajoute automatiquement :

* Node.js
* npm (Node Package Manager)

---

## Vérifier l'installation de Node.js

Ouvrir un terminal puis exécuter :

```bash
node -v
```

Exemple :

```bash
v22.16.0
```

Si une version s'affiche, Node.js est correctement installé.

---

## Vérifier l'installation de npm

Exécuter :

```bash
npm -v
```

Exemple :

```bash
10.9.2
```

Si une version s'affiche, npm est correctement installé.

---

## Qu'est-ce que npm ?

npm signifie :

```text
Node Package Manager
```

Il s'agit du gestionnaire de paquets fourni avec Node.js.

npm permet notamment de :

* Installer des bibliothèques
* Gérer les dépendances
* Exécuter des scripts définis dans le fichier package.json

---

## Initialiser un projet Node.js

Depuis le dossier du projet :

```bash
npm init
```

Ou directement avec les valeurs par défaut :

```bash
npm init -y
```

Cette commande crée un fichier :

```text
package.json
```

qui contient les informations et dépendances du projet.

---

## Installer une dépendance

Exemple avec Sass :

```bash
npm install sass
```

npm télécharge automatiquement la bibliothèque et l'ajoute au projet.

---

## Installer une dépendance de développement

```bash
npm install sass --save-dev
```

La dépendance est enregistrée dans :

```json
"devDependencies"
```

Elle sera utilisée uniquement pendant le développement.

---

## Les fichiers créés par npm

Après l'installation d'une dépendance, npm crée généralement :

```text
node_modules/
package.json
package-lock.json
```

### node_modules

Contient toutes les bibliothèques installées.

### package.json

Contient la configuration du projet.

### package-lock.json

Enregistre précisément les versions installées afin que tous les développeurs utilisent les mêmes dépendances.

---

## Installer les dépendances d'un projet existant

Lorsqu'un projet contient déjà un fichier package.json :

```bash
npm install
```

npm télécharge automatiquement toutes les dépendances nécessaires.

---

## Exécuter un script npm

Exemple :

```json
"scripts": {
  "sass": "sass sass/main.scss css/style.css --watch"
}
```

Le script peut être lancé avec :

```bash
npm run sass
```

npm exécute alors automatiquement la commande définie dans le package.json.

---

# À retenir

* Node.js installe automatiquement npm.
* npm permet d'installer des bibliothèques et d'exécuter des scripts.
* `npm init -y` crée un fichier package.json.
* `npm install` installe les dépendances d'un projet.
* `npm install nom-du-package --save-dev` installe une dépendance de développement.
* `npm run nom-du-script` exécute un script défini dans le package.json.
* Dans un projet Sass, Node.js et npm sont utilisés pour installer Sass et automatiser la compilation des fichiers SCSS en CSS.

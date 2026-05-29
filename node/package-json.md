# Comprendre le fichier package.json

## Qu'est-ce qu'un package.json ?

Le fichier `package.json` est le fichier de configuration principal d'un projet Node.js.

Il est créé automatiquement lors de l'exécution de la commande :

```bash
npm init -y
```

Il permet de centraliser toutes les informations importantes du projet dans un seul fichier.

---

## Pourquoi utiliser un package.json ?

Le package.json permet notamment de :

* Identifier le projet
* Définir sa version
* Gérer les dépendances
* Créer des scripts personnalisés
* Faciliter le partage du projet

Grâce à lui, plusieurs développeurs peuvent travailler sur le même projet avec les mêmes versions des outils.

---

## Structure générale

Exemple :

```json
{
  "name": "projet-4",
  "version": "1.0.0",
  "description": "Projet 4 - OhMyFood",
  "scripts": {
    "sass": "sass sass/main.scss css/style.css --watch"
  },
  "devDependencies": {
    "sass": "^1.98.0"
  }
}
```

Chaque section possède un rôle précis.

---

## name

```json
"name": "projet-4"
```

Nom du projet.

Il sert à identifier le package.

---

## version

```json
"version": "1.0.0"
```

Version du projet.

Le format utilisé est généralement :

```text
MAJOR.MINOR.PATCH
```

Exemple :

```text
1.0.0
```

* MAJOR : changement important
* MINOR : ajout de fonctionnalité
* PATCH : correction de bug

---

## description

```json
"description": "Projet 4 - OhMyFood"
```

Description du projet.

Cette information est principalement informative.

---

## scripts

```json
"scripts": {
  "sass": "sass sass/main.scss css/style.css --watch"
}
```

Les scripts permettent de créer des commandes personnalisées.

Par exemple :

```bash
npm run sass
```

npm lit alors le package.json et exécute automatiquement la commande associée.

Cela évite de devoir retaper une longue commande à chaque utilisation.

---

## dependencies

```json
"dependencies": {
}
```

Cette section contient les bibliothèques nécessaires au fonctionnement du projet.

Exemple :

```bash
npm install nom-du-package
```

La dépendance sera automatiquement ajoutée dans cette section.

---

## devDependencies

```json
"devDependencies": {
  "sass": "^1.98.0"
}
```

Cette section contient les outils utilisés uniquement pendant le développement.

Dans ce projet :

```json
"sass": "^1.98.0"
```

sert à compiler les fichiers SCSS en CSS.

Une fois le site généré, Sass n'est plus nécessaire pour son fonctionnement.

C'est pourquoi il est placé dans `devDependencies`.

---

## package-lock.json

Lors de l'installation d'une dépendance, npm crée également :

```text
package-lock.json
```

Ce fichier enregistre les versions exactes des bibliothèques installées.

Il garantit que tous les développeurs du projet utilisent les mêmes versions.

---

## Réinstaller les dépendances

Lorsqu'un projet contient déjà un package.json, il n'est pas nécessaire d'installer chaque bibliothèque manuellement.

La commande :

```bash
npm install
```

lit le package.json et télécharge automatiquement toutes les dépendances nécessaires.

---

## Exemple concret avec Sass

Installation :

```bash
npm install sass --save-dev
```

Ajout automatique dans le package.json :

```json
{
  "devDependencies": {
    "sass": "^1.98.0"
  }
}
```

Création d'un script :

```json
{
  "scripts": {
    "sass": "sass sass/main.scss css/style.css --watch"
  }
}
```

Exécution :

```bash
npm run sass
```

npm lance alors automatiquement Sass.

---

# À retenir

* Le fichier `package.json` est le fichier de configuration principal d'un projet Node.js.
* Il est généralement créé avec `npm init -y`.
* Il contient les informations du projet.
* Il permet de gérer les dépendances.
* Il permet de créer des scripts personnalisés.
* Il facilite le partage d'un projet entre plusieurs développeurs.
* Dans un projet Sass, il permet de stocker la dépendance Sass et d'exécuter la commande `npm run sass`.

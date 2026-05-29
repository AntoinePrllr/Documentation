# Le fichier .gitignore

## Qu'est-ce qu'un fichier .gitignore ?

Le fichier `.gitignore` permet d'indiquer à Git quels fichiers ou dossiers doivent être ignorés.

Les éléments présents dans ce fichier ne seront pas ajoutés au dépôt Git lors des commits.

Il est généralement placé à la racine du projet.

---

## Pourquoi utiliser un .gitignore ?

Certains fichiers ne doivent pas être partagés dans le dépôt :

* Fichiers temporaires
* Dépendances téléchargées automatiquement
* Fichiers générés lors du build
* Paramètres personnels de l'IDE
* Informations sensibles (clés API, mots de passe, variables d'environnement)

L'utilisation d'un `.gitignore` permet de garder un dépôt propre et sécurisé.

---

## Mettre en place un fichier .gitignore

À la racine du projet, créer un fichier nommé :

```text
.gitignore
```

Exemple d'arborescence :

```text
mon-projet/
│
├── .gitignore
├── index.html
├── style.css
└── script.js
```

Une fois le fichier créé, il suffit d'y ajouter les règles d'exclusion souhaitées.

---

## Exemple de fichier .gitignore

```gitignore
# Dépendances Node.js
node_modules/

# Variables d'environnement
.env

# Fichiers de build
dist/
build/

# Configuration VS Code
.vscode/

# Logs
*.log
```

---

## Ignorer un dossier

Pour ignorer un dossier entier :

```gitignore
node_modules/
```

Git ignorera alors tous les fichiers contenus dans ce dossier.

---

## Ignorer un fichier spécifique

```gitignore
config.json
```

Git ignorera uniquement ce fichier.

---

## Ignorer une extension

```gitignore
*.log
```

Tous les fichiers ayant l'extension `.log` seront ignorés.

---

## Vérifier que le .gitignore fonctionne

Après avoir ajouté des règles dans le fichier `.gitignore`, exécuter :

```bash
git status
```

Les fichiers ignorés ne doivent plus apparaître dans la liste des fichiers à ajouter au dépôt.

---

## Attention aux fichiers déjà suivis

Le fichier `.gitignore` n'agit que sur les fichiers qui ne sont pas encore suivis par Git.

Si un fichier a déjà été ajouté au dépôt, il continuera à être suivi même après son ajout dans le `.gitignore`.

---

## Retirer un fichier du suivi Git

Pour arrêter de suivre un fichier déjà présent dans le dépôt :

```bash
git rm --cached fichier.txt
```

Pour un dossier :

```bash
git rm -r --cached dossier
```

Puis enregistrer la modification :

```bash
git add .
git commit -m "Mise à jour du .gitignore"
```

---

## Exemple concret

Supposons qu'un projet contienne le dossier suivant :

```text
mon-projet/
│
├── node_modules/
├── .env
├── src/
└── package.json
```

Le fichier `.gitignore` pourra contenir :

```gitignore
node_modules/
.env
```

Ainsi :

* Le dossier `node_modules` ne sera pas envoyé sur GitHub.
* Le fichier `.env` restera privé sur l'ordinateur du développeur.

---

## Vérifier les fichiers ignorés

Afficher les fichiers ignorés :

```bash
git status --ignored
```

---

# À retenir

* Le fichier `.gitignore` se crée à la racine du projet.
* Il permet d'exclure des fichiers ou dossiers du dépôt Git.
* Il évite d'envoyer des fichiers inutiles ou sensibles.
* Les fichiers déjà suivis doivent être retirés avec `git rm --cached`.
* Il est recommandé de créer le `.gitignore` dès le début du projet.
* Toujours vérifier son fonctionnement avec `git status`.

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

## Vérifier les fichiers ignorés

Afficher les fichiers ignorés :

```bash
git status --ignored
```

---

# À retenir

* Le fichier `.gitignore` permet d'exclure des fichiers ou dossiers du dépôt Git.
* Il est généralement placé à la racine du projet.
* Il permet d'éviter d'envoyer des fichiers inutiles ou sensibles.
* Les fichiers déjà suivis doivent être retirés avec `git rm --cached`.
* Un bon `.gitignore` doit être créé dès le début du projet.

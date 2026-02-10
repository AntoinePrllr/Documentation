# 📘 HTML — HyperText Markup Language

## 1. Définition

**HTML (HyperText Markup Language)** est un **langage de balisage** utilisé pour **structurer le contenu** des pages web.

- HTML définit la structure et la sémantique du contenu
- HTML ne gère ni le style (CSS), ni la logique (JavaScript)

---

## 2. Date de création & histoire

- **1991** : création par **Tim Berners-Lee**
- Objectif initial : partager des documents scientifiques sur le web

### Grandes étapes
- **HTML 1.0** : structure basique
- **HTML 4.01 (1999)** : standard historique
- **XHTML** : version plus stricte inspirée du XML
- **HTML5 (2014)** : sémantique moderne, audio, vidéo
- **HTML Living Standard** : évolution continue aujourd’hui

---

## 3. Rôle de HTML dans le web

HTML fait partie du triptyque fondamental du web :

| Technologie | Rôle                      |
| ----------- | ------------------------- |
| HTML        | Structure et contenu      |
| CSS         | Apparence et mise en page |
| JavaScript  | Interactivité et logique  |

---

## 4. Structure minimale d’un document HTML

```html
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Titre de la page</title>
</head>
<body>
  <h1>Hello World</h1>
</body>
</html>
```

---

## 5. Balises HTML

### Balises ouvrantes / fermantes
```html
<p>Un paragraphe</p>
```

### Balises auto-fermantes
```html
<img src="image.jpg" alt="Description">
<br>
<input>
```

---

## 6. Attributs HTML

Les attributs apportent des informations supplémentaires aux balises.

```html
<a href="https://example.com" target="_blank">Lien</a>
```

Attributs courants :
- `id`
- `class`
- `src`
- `href`
- `alt`
- `title`
- `data-*`

---

## 7. Sémantique HTML

Balises sémantiques principales :
- `<header>`
- `<nav>`
- `<main>`
- `<section>`
- `<article>`
- `<aside>`
- `<footer>`

Avantages :
- Accessibilité
- SEO
- Lisibilité
- Maintenabilité

---

## 8. Titres et hiérarchie

```html
<h1>Titre principal (1 seul par page)</h1>
<h2>Section</h2>
<h3>Sous-section</h3>
```

---

## 9. Contenu textuel

- `<p>` : paragraphe
- `<strong>` : importance forte
- `<em>` : emphase
- `<span>` : inline neutre
- `<blockquote>` : citation
- `<code>` : code inline
- `<pre>` : texte préformaté

---

## 10. Liens

```html
<a href="page.html">Lien interne</a>
<a href="https://site.com">Lien externe</a>
<a href="#section">Ancre</a>
```

---

## 11. Images et médias

```html
<img src="image.jpg" alt="Description accessible">
```

---

## 12. Listes

```html
<ul>
  <li>Item</li>
</ul>
```

```html
<ol>
  <li>Item</li>
</ol>
```

---

## 13. Tableaux

```html
<table>
  <thead>
    <tr><th>Nom</th></tr>
  </thead>
  <tbody>
    <tr><td>Valeur</td></tr>
  </tbody>
</table>
```

---

## 14. Formulaires

```html
<form>
  <label for="email">Email</label>
  <input type="email" id="email">
  <button type="submit">Envoyer</button>
</form>
```

---

## 15. Accessibilité

Bonnes pratiques :
- Attribut `alt`
- Balises sémantiques
- Labels liés aux inputs
- Hiérarchie des titres
- `aria-*` si nécessaire

---

## 16. Bonnes pratiques HTML

- Code lisible
- Indentation propre
- Un seul `<h1>`
- Séparation HTML / CSS / JS
- Séparation HTML / CSS / JS

Code lisible avant tout

17. Ce que HTML n’est pas

❌ Un langage de programmation
❌ Un langage de mise en page
❌ Un langage logique

HTML = structure & sens

18. Question typique d’entretien

“À quoi sert HTML ?”
👉 À structurer sémantiquement le contenu d’une page web.

“Différence div / section ?”
👉 div = neutre
👉 section = contenu thématique

# CSS — Cascading Style Sheets

## 1. Définition

**CSS (Cascading Style Sheets)** est un langage de feuille de style utilisé pour décrire **la présentation visuelle** d’un document écrit en **HTML** ou **XML**.

HTML décrit la structure du contenu, tandis que CSS gère l’apparence :
- couleurs
- polices
- tailles
- espacements
- mise en page
- animations
- responsive design

---

## 2. Origine et création de CSS

### 2.1 Contexte historique

Au début du Web, au début des années 1990, HTML servait à la fois à structurer le contenu et à le mettre en forme (balises `<font>`, `<center>`, etc.).

Cela posait plusieurs problèmes :
- code difficile à lire
- duplication massive des styles
- maintenance complexe
- absence de séparation des rôles

---

### 2.2 Création de CSS

CSS a été proposé en **1994** par **Håkon Wium Lie**, alors chercheur au **CERN**.

L’objectif principal était clair :
> Séparer le **contenu** (HTML) de la **présentation** (CSS).

---

### 2.3 Normalisation

CSS est standardisé par le **W3C (World Wide Web Consortium)**, l’organisme chargé de définir les standards du Web.

---

## 3. Dates clés importantes

- **1994** : proposition initiale de CSS
- **1996** : CSS1 devient un standard officiel
- **1998** : CSS2
- **2011** : CSS 2.1
- **Depuis 2012** : CSS évolue sous forme de modules (souvent appelés CSS3)

⚠️ CSS3 n’est pas une version unique mais un ensemble de modules indépendants.

---

## 4. Principe fondamental : la cascade

Le mot *Cascading* fait référence à la manière dont les styles sont appliqués selon des règles de priorité.

### Ordre de priorité simplifié :
1. `!important`
2. Styles inline (`style=""`)
3. Spécificité des sélecteurs
4. Ordre d’apparition dans le fichier CSS

### Spécificité (simplifiée) :
- Inline : 1000
- ID : 100
- Classe : 10
- Élément : 1

---

## 5. Syntaxe de base

```css
sélecteur {
  propriété: valeur;
}
```

Exemple :
```css
p {
  color: blue;
  font-size: 16px;
}
```

---

## 6. Sélecteurs CSS

### Sélecteurs simples
- `p` : élément
- `.classe`
- `#id`
- `*` : universel

### Sélecteurs combinés
```css
div p
div > p
h1 + p
h1 ~ p
```

### Sélecteurs avancés
- `[type="text"]`
- `:hover`
- `:focus`
- `:nth-child()`
- `::before`
- `::after`

---

## 7. Le modèle de boîte (Box Model)

Chaque élément CSS est une boîte composée de :
1. content
2. padding
3. border
4. margin

```css
box-sizing: content-box;
box-sizing: border-box;
```

---

## 8. Mise en page moderne

### Flexbox
Gestion des layouts sur un axe unique (ligne ou colonne).

```css
display: flex;
justify-content: center;
align-items: center;
```

### Grid
Gestion des layouts en deux dimensions.

```css
display: grid;
grid-template-columns: repeat(3, 1fr);
gap: 20px;
```

---

## 9. Responsive Design

Le responsive design permet l’adaptation à tous les écrans.

```css
@media (max-width: 768px) {
  body {
    font-size: 14px;
  }
}
```

Le principe **Mobile First** est aujourd’hui recommandé.

---

## 10. Animations et transitions

### Transition
```css
transition: all 0.3s ease;
```

### Animation
```css
@keyframes fade {
  from { opacity: 0; }
  to { opacity: 1; }
}
```

---

## 11. Évolutions modernes de CSS

- Variables CSS (`--main-color`)
- calc()
- clamp()
- container queries
- Préprocesseurs : Sass, Less, PostCSS

---

## 12. Bonnes pratiques

- Séparer HTML et CSS
- Utiliser les classes plutôt que les IDs pour le style
- Éviter `!important`
- Nommer clairement les classes
- Écrire un CSS lisible et maintenable

---

## 13. Phrase clé pour un oral

> « CSS est un langage déclaratif normalisé par le W3C, basé sur la cascade, la spécificité et l’héritage, permettant de séparer la présentation du contenu afin d’améliorer la maintenabilité et l’accessibilité des interfaces web. »

---

## 14. Conclusion

CSS est un langage de style essentiel au Web moderne.  
Il permet la mise en forme, le responsive design, les animations et l’amélioration de l’expérience utilisateur.

CSS n’est **pas** un langage de programmation, mais un **langage déclaratif**.

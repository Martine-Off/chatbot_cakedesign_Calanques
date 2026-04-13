# 📋 Guide Copyright — Marche à suivre pour les projets EISF

> **Version** : 1.0 — Avril 2026
> **Auteur** : Martine Desmaroux — m.desmaroux@eisf.fr
> **Usage** : Guide réutilisable pour ajouter les mentions de copyright sur tout projet logiciel EISF

---

## Objectif

Ce document décrit la **procédure exhaustive** pour protéger la propriété intellectuelle d'un projet logiciel EISF. Il est conçu pour être réutilisable sur n'importe quel projet (site web, chatbot, application, outil interne, etc.).

---

## 📌 Checklist rapide

Cocher chaque élément une fois réalisé :

- [x] **Fichier `LICENSE`** à la racine du projet
- [x] **Header copyright** dans chaque fichier de code source (`.js`, `.css`, `.html`, `.py`, etc.)
- [x] **Balise `<meta name="author">`** dans chaque page HTML
- [x] **Commentaire copyright** dans le CSS (inline ou fichier séparé)
- [x] **Documentation des droits sur les visuels** (images, logos, icônes)
- [x] **Inventaire des dépendances tierces** et vérification de leurs licences
- [x] **Mention dans la documentation** du projet (`README.md` ou doc technique)

---

## Étape 1 — Créer le fichier `LICENSE`

### Quoi
Un fichier texte nommé `LICENSE` (sans extension) à la **racine du dépôt Git**.

### Pourquoi
C'est le standard universel reconnu par GitHub, GitLab, et tous les outils de gestion de code. Sans ce fichier, le code est légalement considéré comme "tous droits réservés" par défaut en France, mais l'expliciter évite toute ambiguïté.

### Modèle pour projets EISF (propriétaire)

```
Copyright (c) 2026 EISF — École Internationale du Savoir Faire Français
Tous droits réservés / All Rights Reserved

Ce logiciel et les fichiers associés (le "Logiciel") sont la propriété
exclusive de l'École Internationale du Savoir Faire Français (EISF).

Toute copie, modification, distribution, publication, ou utilisation du
Logiciel, en tout ou en partie, est strictement interdite sans
l'autorisation écrite préalable de l'EISF.

Le Logiciel est fourni "en l'état", sans garantie d'aucune sorte,
expresse ou implicite.

---

This software and associated files (the "Software") are the exclusive
property of École Internationale du Savoir Faire Français (EISF).

Any copying, modification, distribution, publication, or use of the
Software, in whole or in part, is strictly prohibited without prior
written authorization from EISF.

The Software is provided "as is", without warranty of any kind,
express or implied.

---

Auteur / Author : Martine Desmaroux — m.desmaroux@eisf.fr
Organisation / Organization : EISF — École Internationale du Savoir Faire Français
Repo : (privé / private)
Date de création / Creation date : Avril 2026
```

---

## Étape 2 — Ajouter le header copyright dans le code source

### Quoi
Un bloc de commentaire en tête de **chaque fichier de code** du projet.

### Pourquoi
Si un fichier est copié individuellement (sans le `LICENSE`), la mention de copyright reste attachée au code.

### Modèles par langage

#### JavaScript (`.js`)
```javascript
/**
 * L'Ecume Sucrée - Chatbot Cake Design — Interface de prise de commande
 *
 * © 2026 EISF — École Internationale du Savoir Faire Français
 * Tous droits réservés / All Rights Reserved.
 *
 * Ce fichier fait partie du projet "L'Ecume Sucrée - Chatbot Cake Design".
 * Toute reproduction ou utilisation non autorisée est interdite.
 * Voir le fichier LICENSE à la racine du projet.
 *
 * @author  Martine Desmaroux <m.desmaroux@eisf.fr>
 * @version 1.0
 * @date    Avril 2026
 * @license Propriétaire — EISF
 */
```

#### HTML (`.html`)
```html
<!--
  L'Ecume Sucrée - Chatbot Cake Design — Interface de prise de commande

  © 2026 EISF — École Internationale du Savoir Faire Français
  Tous droits réservés / All Rights Reserved.

  Auteur : Martine Desmaroux — m.desmaroux@eisf.fr
  Voir le fichier LICENSE à la racine du projet.
-->
```

#### CSS (`.css` ou `<style>`)
```css
/*
 * L'Ecume Sucrée - Chatbot Cake Design — Styles
 *
 * © 2026 EISF — École Internationale du Savoir Faire Français
 * Tous droits réservés.
 *
 * @author  Martine Desmaroux <m.desmaroux@eisf.fr>
 * @license Propriétaire — EISF
 */
```

---

## Étape 3 — Balises meta HTML

### Quoi
Ajouter dans le `<head>` de chaque page HTML les balises suivantes :

```html
<meta name="author" content="EISF — École Internationale du Savoir Faire Français" />
<meta name="copyright" content="© 2026 EISF — Tous droits réservés" />
```

### Pourquoi
- Les moteurs de recherche et crawlers lisent ces balises
- C'est une bonne pratique SEO et juridique
- Cela documente la propriété directement dans le fichier déployé

---

## Étape 4 — Inventaire des dépendances tierces

### Quoi
Vérifier la licence de **chaque ressource externe** utilisée dans le projet.

### Inventaire — Projet Chatbot L'Ecume Sucrée

| Ressource | Type | Licence | Usage commercial | Crédit requis | Statut |
|-----------|------|---------|-----------------|---------------|--------|
| Google Fonts (Poppins, Playfair Display, Bodoni Moda, Lora) | Police | SIL OFL 1.1 | ✅ Oui | Non | ✅ OK |
| Make.com | Service SaaS | — | ✅ Oui (abonnement) | Non | ✅ OK |

### Licences courantes et leur signification

| Licence | Usage commercial | Modification | Crédit requis | Copyleft |
|---------|-----------------|-------------|---------------|----------|
| **MIT** | ✅ | ✅ | ✅ Oui | Non |
| **Apache 2.0** | ✅ | ✅ | ✅ Oui | Non |
| **GPL v3** | ✅ | ✅ | ✅ Oui | ⚠️ **Oui** — code dérivé doit être GPL |
| **SIL OFL 1.1** | ✅ | ✅ (polices) | Non | Non |
| **CC BY 4.0** | ✅ | ✅ | ✅ Oui | Non |
| **CC BY-NC** | ❌ Non commercial | ✅ | ✅ Oui | Non |
| **Propriétaire** | ❌ Sauf accord | ❌ | — | — |

---

## Étape 5 — Documenter les droits sur les visuels

### Quoi
Pour chaque image, logo, icône ou visuel dans le projet, documenter :

### Inventaire visuels — Projet Chatbot L'Ecume Sucrée

| Fichier | Description | Créateur | Licence | Date |
|---------|-------------|----------|---------|------|
| `L'Ecume Sucrée.png` | Logo officiel de la pâtisserie | EISF (interne) | Propriétaire EISF | 2026 |
| `M. Baris.png` | Avatar Monsieur Baris | EISF (interne) | Propriétaire EISF | 2026 |

### Pourquoi
- En cas de litige, on peut prouver la propriété
- Si un prestataire externe a créé un visuel, il faut s'assurer que les droits ont été cédés à EISF
- Les images de stock (Shutterstock, Adobe Stock) ont souvent des restrictions

### Points de vigilance

> [!WARNING]
> **Images trouvées sur Internet** : même si elles sont "libres de droits" en apparence, vérifier la licence exacte. Un usage "gratuit pour usage personnel" ≠ usage commercial autorisé.

> [!IMPORTANT]
> **Logos et visuels créés par un prestataire** : s'assurer qu'un contrat de cession de droits existe. Sans cession écrite, l'auteur conserve ses droits même s'il a été payé.

---

## Étape 6 — Mention dans la documentation

### Quoi
Ajouter une section "Propriété intellectuelle" ou "Copyright" dans :
- Le `README.md` du repo
- La documentation technique du projet

### Modèle utilisé dans le README

```markdown
## Propriété intellectuelle

Ce projet est la propriété exclusive de l'[EISF — École Internationale du Savoir Faire Français](https://eisf.fr).

- **Auteur** : Martine Desmaroux — m.desmaroux@eisf.fr
- **Licence** : Propriétaire — Tous droits réservés
- **Voir** : [LICENSE](./LICENSE)

Toute reproduction, modification ou distribution non autorisée est interdite.
```

---

## Étape 7 — Vérification finale

### Checklist de validation

| # | Vérification | Comment | ✅ |
|---|-------------|---------|---|
| 1 | Le fichier `LICENSE` existe à la racine | `ls LICENSE` dans le terminal | ✅ |
| 2 | Chaque fichier `.js` a un header copyright | Rechercher `©` dans tous les `.js` | ✅ |
| 3 | Chaque fichier `.html` a un commentaire copyright | Ouvrir chaque HTML | ✅ |
| 4 | Les balises `<meta author>` et `<meta copyright>` sont présentes | Inspecter le `<head>` | ✅ |
| 5 | L'inventaire des dépendances est à jour | Relire le tableau | ✅ |
| 6 | Les visuels sont documentés | Vérifier le tableau des visuels | ✅ |
| 7 | La documentation mentionne le copyright | Ouvrir le README/doc | ✅ |

---

*© 2026 EISF — École Internationale du Savoir Faire Français — Document interne*


# 🌟 Villa Nova — Projet by ALYA ANNABI

> Application web culturelle pour centraliser les événements d'une collectivité territoriale, destinée aux 18–40 ans.

---

## 📌 Contexte

VillaNova est une ville fictive confrontée à un problème réel : malgré une programmation culturelle riche (concerts, expositions, théâtre, festivals), la participation des jeunes adultes reste faible.

**Cause identifiée :** l'information est dispersée sur de multiples supports, rendant la découverte des événements complexe et peu intuitive.

**Solution :** une application web centralisée permettant de consulter tous les événements, naviguer dans un agenda interactif et réserver en quelques clics.

---

## 🗂️ Structure du projet

```
villa-nova/
├── index.html          → Page d'accueil (hero, cartes, slider vidéos)
├── evenement.html      → Tous les événements avec filtres
├── agenda.html         → Calendrier interactif + API OpenAgenda
├── about.html          → Présentation du projet + engagement écologique
│
├── sass/
│   ├── style.scss      → Fichier principal (imports)
│   ├── style.css       → CSS compilé
│   ├── _variable.scss  → Variables (couleurs, typo, espacements)
│   ├── _header.scss
│   ├── _hero.scss
│   ├── _event.scss
│   ├── _agenda.scss
│   ├── _footer.scss
│   ├── _burger.scss
│   ├── _mobile-menu.scss
│   ├── _responsive.scss
│   ├── _filtre.scss
│   ├── _load.scss
│   ├── _about.scss
│   ├── _body.scss
│   └── _video.scss
│
├── js/
│   ├── main.js         → Slider vidéos
│   ├── card.js         → Bouton "Voir plus"
│   ├── nav-burger.js   → Menu hamburger mobile
│   └── agenda.js       → Calendrier + appel API OpenAgenda
│
└── assets/             → Images et médias
```

---

## 🛠️ Technologies utilisées

| Technologie | Utilisation |
|---|---|
| HTML5 | Structure sémantique des 4 pages |
| SCSS | Styles organisés en fichiers partiels avec variables |
| JavaScript (ES6) | Interactivité, DOM, fetch API |
| OpenAgenda API | Récupération des événements en temps réel |
| Tabler Icons | Icônes via webfont CDN |
| Google Fonts | Police Permanent Marker |

---

## ✨ Fonctionnalités

- **Navigation responsive** avec menu hamburger animé (croix à l'ouverture)
- **Page événements** avec filtres par catégorie (Exposition, Concert, Théâtre, Festival)
- **Bouton "Voir plus"** qui affiche les cartes cachées progressivement
- **Calendrier interactif** avec navigation mois par mois
- **Intégration API OpenAgenda** — affichage des vrais événements en temps réel
- **Fallback** si l'API est indisponible (message d'erreur propre, calendrier toujours affiché)
- **Slider vidéos YouTube** avec flèches (une vidéo à la fois, lazy loading)
- **Page À propos** avec problématique, solution, objectifs et engagement écologique
- **Design responsive** desktop + mobile sur les 4 pages

---

## 🌿 Engagement écologique

Le projet intègre une démarche éco-responsable :
- Vidéos en lazy loading (chargement uniquement si visible)
- Pas d'autoplay vidéo (réduction de la bande passante)
- Hébergement vidéo sur YouTube (infrastructure optimisée)
- Images compressées

---

## 🚀 Installation et lancement

1. Clone ou télécharge le projet
2. Ouvre `index.html` dans ton navigateur

> Aucune installation requise — le projet tourne en HTML/CSS/JS pur.

Si tu veux modifier le SCSS :
```bash
# Installer Sass si pas déjà fait
npm install -g sass

# Compiler en mode watch
sass --watch sass/style.scss sass/style.css
```

---

## 🔑 API OpenAgenda

L'agenda utilise l'API publique OpenAgenda.

- **Slug de l'agenda :** `villa-nova-alya`
- **Clé API :** configurée dans `js/agenda.js`
- **Endpoint utilisé :** `https://api.openagenda.com/v2/agendas/{uid}/events`

---

## 🐛 Problèmes rencontrés et solutions

| Problème | Solution |
|---|---|
| Hamburger ne s'ouvrait pas sur evenement.html | Ajout du bloc `#mobileMenu` manquant dans le header |
| Nav desktop invisible sur mobile → desktop | Réorganisation de l'ordre des règles CSS (media query après la déclaration) |
| Agenda non responsive | Media query `.agenda-section` déplacé après sa déclaration |
| `card.js` plantait silencieusement | Ajout des `const button` et `const hiddenCards` manquantes |
| URLs YouTube cassées dans iframe | Remplacement de `youtu.be/...` par `youtube.com/embed/...` |

---

## 📅 Réalisé en 5 jours

| Jour | Travail |
|---|---|
| Jour 1 | Structure HTML des 4 pages + architecture SCSS |
| Jour 2 | Design complet + responsive mobile |
| Jour 3 | JavaScript (burger, cards, slider) |
| Jour 4 | Intégration API OpenAgenda + calendrier |
| Jour 5 | Vidéos, debug final, page about, finitions |

---

## 👩‍💻 Auteur

ALYA ANNABI

Projet réalisé dans le cadre du **Bloc 2** à **La Plateforme** — Formation développement web.

# 🌟 Projet URANIE - Gestion et Cartographie de Processus

Application web moderne de gestion et cartographie de processus métier avec système de recherche avancé et navigation intuitive.

## 📋 Description

**URANIE** est une application web complète permettant de :
- Visualiser et gérer des processus métier
- Cartographier les flux et ressources IT
- Rechercher efficacement dans la base de connaissances
- Naviguer intuitivement entre les différentes sections

## 💻 Technologies

### Frontend
- **HTML5** - Structure sémantique
- **Vue.js 3** - Framework JavaScript réactif (via CDN)
- **Tailwind CSS** - Framework CSS utilitaire (via CDN)
- **JavaScript ES6+** - Logique applicative moderne

### Backend (Prévu)
- **SQL Server** - Base de données relationnelle
- **SharePoint** - Gestion documentaire et collaboration

## 🏗️ Structure du Projet

```
KusmiKartProto/
├── README.md                           # Documentation principale
├── docs/
│   └── CDC-URANIE-Prompt.md           # Cahier des charges complet
├── assets/
│   ├── images/
│   │   ├── logo-luna.png              # Logo principal
│   │   └── tsarevna.jpg               # Image de référence
│   └── css/
│       └── style-global.css           # Styles globaux
└── pages/
    ├── uranie-accueil-vue.html        # Page d'accueil
    ├── uranie-recherche-vue.html      # Page de recherche
    └── uranie-fiche-process-vue.html  # Template fiche processus
```

## 🚀 Installation et Démarrage

### Prérequis
- Un navigateur web moderne (Chrome, Firefox, Safari, Edge)
- Un serveur web local (optionnel pour le développement)

### Lancement en local

**Option 1 : Serveur web simple**
```bash
# Avec Python 3
python -m http.server 8000

# Avec Node.js (http-server)
npx http-server
```

**Option 2 : Ouvrir directement**
Ouvrez le fichier `pages/uranie-accueil-vue.html` dans votre navigateur.

⚠️ **Note** : Certaines fonctionnalités peuvent nécessiter un serveur web pour fonctionner correctement (CORS, etc.).

## 📄 Pages Disponibles

### 🏠 Page d'Accueil (`uranie-accueil-vue.html`)
- 5 cartes rectangulaires interactives
- Recherche intégrée dans la carte centrale
- Mode développeur (Ctrl+D) pour ajuster les positions
- Navigation vers les différentes sections

### 🔍 Page de Recherche (`uranie-recherche-vue.html`)
- Champ de recherche avec auto-focus
- 5 filtres exclusifs : Carto, Tag, Process, Flow, Ressources
- Validation sur Enter
- Animation d'étoiles en arrière-plan

### 📋 Page Fiche Process (`uranie-fiche-process-vue.html`)
- Layout 2/3 - 1/3
- Affichage détaillé d'un processus
- Tags colorés cliquables
- Sections : Résumé, Architecture, Liens, Cartographie, Flux, Ressources

## 🎨 Design System

### Palette de Couleurs
- **Violet** : `#4F46E5` (Indigo)
- **Purple** : `#7C3AED`
- **Rose** : `#EC4899`
- **Dégradés** : Combinaisons violet/indigo/rose

### Typographies
- **Montserrat** (400, 600, 700) - Textes courants
- **Metamorphous** - Titres stylisés

### Thématique
- Style cosmique/spatial avec effets étoilés animés
- Transitions fluides et animations modernes
- Effets hover interactifs

## ⚡ Fonctionnalités Avancées

### Mode Développeur
- Activation : `Ctrl+D`
- Permet le repositionnement des cartes
- Export automatique des coordonnées
- Copie dans le presse-papiers

### Navigation
- Sidebar rétractable
- Menu Admin avec sous-menus déroulants
- Navigation fluide entre les pages
- Boutons de retour contextuels

### Recherche
- Auto-focus au chargement
- Filtrage par catégorie
- Persistance dans l'URL
- Redirection intelligente vers les fiches

## 🔌 Intégrations Prévues

- **SQL Server** : CRUD complet pour toutes les entités
- **SharePoint** : Stockage et versioning des documents
- **API REST** : Communication avec les systèmes externes

## 📱 Responsive Design

### Breakpoints
- **Mobile** : < 640px
- **Tablet** : 640px - 1024px
- **Desktop** : > 1024px

### Accessibilité
- Sémantique HTML5
- Labels ARIA sur les actions
- Navigation clavier (Tab, Enter, Escape)
- Contrastes WCAG AA
- Focus visible

## 🛠️ Développement

### Conventions de Nommage
- **Fichiers** : kebab-case (`uranie-page-vue.html`)
- **Composants Vue** : PascalCase
- **CSS classes** : Tailwind utilities + BEM si nécessaire
- **Variables** : camelCase

### Git Workflow
- Feature branches : `feature/nom-fonctionnalite`
- Commits : Conventional Commits (`feat:`, `fix:`, `docs:`)
- Pull Requests avec review

## 📊 Métriques de Succès

- **Performance** : < 2s temps de chargement
- **Accessibilité** : Score Lighthouse > 90
- **UX** : < 3 clics pour toute action
- **Adoption** : Taux d'utilisation > 80%

## 🎯 Roadmap

### Court terme ✅
- [x] Interface utilisateur complète
- [x] Navigation fonctionnelle
- [x] Recherche avec filtres
- [ ] Connexion API SQL Server
- [ ] Authentification utilisateur

### Moyen terme 📅
- [ ] Pages Admin fonctionnelles
- [ ] CRUD complet pour chaque entité
- [ ] Système de commentaires
- [ ] Export PDF des fiches

### Long terme 🚀
- [ ] Module de reporting avancé
- [ ] Dashboard analytics
- [ ] API REST documentée
- [ ] Tests unitaires (Vitest)
- [ ] Migration vers build Vite.js

## 📞 Documentation

Pour plus de détails sur le projet, consultez le [Cahier des Charges](docs/CDC-URANIE-Prompt.md).

## 📝 Licence

Projet interne - Tous droits réservés

---

**Version** : 1.0
**Dernière mise à jour** : Octobre 2025
**Statut** : ✅ Développement initial terminé

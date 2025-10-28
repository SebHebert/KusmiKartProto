# 📋 CAHIER DES CHARGES - Projet URANIE
## Prompt de synthèse pour IA

---

## 🎯 CONTEXTE DU PROJET

**URANIE** est une application web de gestion et cartographie de processus métier avec un système de recherche avancé et de navigation intuitive.

---

## 💻 ENVIRONNEMENT TECHNIQUE

### **Stack Frontend**
- **HTML5** - Structure sémantique
- **Vue.js 3** - Framework JavaScript réactif avec CDN
- **Tailwind CSS** - Framework CSS utilitaire via CDN
- **JavaScript ES6+** - Logique applicative

### **Stack Backend**
- **SQL Server** - Base de données relationnelle
- **SharePoint** - Gestion documentaire et collaboration

### **Design System**
- **Palette de couleurs** : Dégradés violet/indigo/rose (#4F46E5, #7C3AED, #EC4899)
- **Typographies** : 
  - Montserrat (400, 600, 700) - Textes courants
  - Metamorphous - Titres stylisés
- **Thématique** : Cosmique/spatial avec effets étoilés animés
- **Animations** : Transitions fluides, fade-in, pulse, hover effects

### **Assets graphiques**
- `logoluna.png` - Logo principal avec dégradés rose-violet-orange
- `tsarevna.jpg` - Image de référence (thé Kusmi Tea)

---

## 🏗️ ARCHITECTURE & FONCTIONNALITÉS DÉVELOPPÉES

### **1. PAGE D'ACCUEIL** (`uranie-accueil-vue.html`)

#### Layout principal
- **5 cartes rectangulaires positionnables**
  - 4 cartes en périphérie (Carto, Tag, Flow, Ressources)
  - 1 carte centrale "Kusmi Tea" avec recherche intégrée
- **Système de grille interactive**
  - Sélection multiple des cartes (effet grisé)
  - Copie du code de position pour développement

#### Fonctionnalités
- Mode développeur avec ajustement positions (Ctrl+D)
- Recherche rapide dans la carte centrale
- Navigation vers les sections via cartes cliquables
- Sidebar de navigation rétractable

---

### **2. PAGE DE RECHERCHE** (`uranie-recherche-vue.html`)

#### Interface de recherche
- **Champ de recherche principal** avec auto-focus
- **5 filtres cliquables exclusifs** :
  - 🗺️ Carto (Cartographies) - Vert
  - 🏷️ Tag (Tags) - Bleu
  - 📋 Process (Processus) - Violet
  - 🔄 Flow (Flux) - Orange
  - 📚 Ressources (Ressources) - Rose

#### Comportements
- Sélection exclusive (un seul filtre actif)
- Validation sur Enter
- Redirection vers fiche correspondante avec paramètres de recherche
- Animation des étoiles en arrière-plan
- Bouton retour à l'accueil

---

### **3. PAGE FICHE PROCESS** (`uranie-fiche-process-vue.html`)

#### Layout 2/3 - 1/3
**Zone principale (2/3)** :
- Titre du process avec badge statut
- Tags colorés cliquables
- Résumé descriptif
- Architecture technique
- Liens utiles (boutons externes)
- Section Cartographie
- Section Flux
- Section Ressources

**Sidebar droite (1/3)** :
- Informations process
- Métadonnées (dates, versions)
- Actions rapides

#### Code couleur des statuts
- 🟢 **VERT** - Validé / En production
- 🔴 **ROUGE** - Obsolète / Erreur
- 🔵 **BLEU** - En cours / Développement
- 🟠 **ORANGE** - En attente / Révision

#### Sections détaillées
- **Tags** : Système de catégorisation visuel
- **Résumé** : Description fonctionnelle
- **Architecture** : Schémas et diagrammes
- **Liens** : Accès externes (docs, repos Git, Jira)
- **Cartographie** : Vue d'ensemble processus
- **Flux** : Diagrammes de flux de données
- **Ressources** : Documents, guides, contacts

---

### **4. NAVIGATION GLOBALE**

#### Sidebar latérale gauche (toutes les pages)
- **Bouton toggle** - Rétractable/Expandable
- **Menu principal** :
  - 🏠 Accueil
  - 🔍 Recherche
  - 📋 Processus
  - 🗺️ Cartographies
  - 🔄 Flux
  - 📚 Ressources

#### Menu Admin avec sous-menus
- **👤 Admin** (déroulant au clic)
  - 👥 Utilisateurs - Gestion des utilisateurs
  - 📋 Processus - Gestion des processus
  - 🗺️ Cartographies - Gestion des cartographies
  - ⚙️ Paramètres - Configuration système
  - 📄 Logs - Journaux système

#### Animations sidebar
- Transition fluide 0.3s ease
- États hover interactifs
- Icônes SVG vectorielles
- Max-height animation pour sous-menus

---

## 🎨 COMPOSANTS & PATTERNS UI

### Boutons
```css
- Primary : bg-gradient violet-to-indigo
- Secondary : bg-white/10 backdrop-blur
- Hover : scale(1.05) + shadow
- States : active, disabled, loading
```

### Cartes
```css
- Background : white/90 backdrop-blur
- Shadow : xl avec hover lift
- Border-radius : lg (0.5rem)
- Animations : fadeIn, scale on hover
```

### Filtres
```css
- Style : Pills avec border coloré
- Active : background couleur + opacity 40%
- Transition : 0.3s all ease
- Icons : SVG inline
```

### Badges de statut
```css
- Round : full border-radius
- Size : text-xs px-2 py-1
- Colors : bg-{color}-100 text-{color}-800
- Font : font-semibold uppercase
```

---

## 🔌 INTÉGRATIONS PRÉVUES

### SQL Server
- CRUD processus, cartographies, flux, ressources
- Gestion utilisateurs et droits
- Historique et versioning
- Recherche full-text

### SharePoint
- Stockage documents
- Gestion versions
- Workflow approbation
- Partage sécurisé

---

## 📱 RESPONSIVE & ACCESSIBILITÉ

### Breakpoints
- Mobile : < 640px
- Tablet : 640px - 1024px
- Desktop : > 1024px

### Accessibilité
- Sémantique HTML5
- ARIA labels sur actions
- Navigation clavier (Tab, Enter, Escape)
- Contrastes WCAG AA
- Focus visible

---

## ⚡ PERFORMANCES & OPTIMISATIONS

- **CDN** pour Vue.js et Tailwind (pas de build requis)
- **Lazy loading** des images
- **Animations CSS** (GPU accelerated)
- **Debounce** sur recherche
- **Transitions** optimisées 60fps

---

## 🚀 FONCTIONNALITÉS AVANCÉES

### Mode Développeur (Ctrl+D)
- Activation du drag & drop des cartes
- Visualisation des positions en temps réel
- Export des coordonnées pour le code
- Copie automatique dans le presse-papiers

### Recherche intelligente
- Auto-focus au chargement
- Validation sur Enter
- Persistance du terme dans l'URL
- Filtrage contextuel par section

### Animation d'arrière-plan
- Génération dynamique d'étoiles (30 éléments)
- Animation pulse asynchrone
- Tailles et positions aléatoires
- Performance optimisée (will-change)

---

## 📦 STRUCTURE DES FICHIERS

```
uranie/
├── uranie-accueil-vue.html          # Page d'accueil
├── uranie-recherche-vue.html        # Page recherche
├── uranie-fiche-process-vue.html    # Template fiche
├── assets/
│   ├── logoluna.png                 # Logo principal
│   └── tsarevna.jpg                 # Image référence
└── README.md                        # Documentation
```

---

## 🎯 PROCHAINES ÉTAPES SUGGÉRÉES

### Court terme
1. Connexion API SQL Server (fetch/axios)
2. Authentification utilisateur
3. Pages Admin fonctionnelles
4. CRUD complet pour chaque entité

### Moyen terme
1. Système de commentaires
2. Export PDF des fiches
3. Historique des modifications
4. Notifications temps réel

### Long terme
1. Module de reporting avancé
2. Dashboard analytics
3. API REST documentée
4. Tests unitaires (Vitest)
5. Migration vers build Vite.js

---

## 📝 CONVENTIONS DE DÉVELOPPEMENT

### Nommage
- **Fichiers** : kebab-case (`uranie-page-vue.html`)
- **Composants Vue** : PascalCase (dans data/methods)
- **CSS classes** : Tailwind utilities + custom BEM si besoin
- **Variables** : camelCase JavaScript

### Structure Vue.js
```javascript
Vue.createApp({
    data() { return {...} },
    computed() { ... },
    methods: { ... },
    mounted() { ... }
}).mount('#app');
```

### Git workflow
- Feature branches : `feature/nom-fonctionnalite`
- Commits : Conventional Commits (feat:, fix:, docs:)
- Pull Requests avec review obligatoire

---

## 🔐 SÉCURITÉ

- Validation côté client ET serveur
- Échappement XSS sur contenus dynamiques
- HTTPS obligatoire en production
- Headers de sécurité (CSP, HSTS)
- Gestion des sessions SQL Server sécurisée

---

## 📊 MÉTRIQUES DE SUCCÈS

- **Performance** : < 2s temps de chargement
- **Accessibilité** : Score Lighthouse > 90
- **UX** : < 3 clics pour toute action
- **Adoption** : Taux d'utilisation > 80% des utilisateurs cibles

---

## 📞 CONTACTS & RESSOURCES

- **Documentation Vue.js** : https://vuejs.org
- **Tailwind CSS** : https://tailwindcss.com
- **SQL Server Docs** : https://docs.microsoft.com/sql
- **SharePoint API** : https://docs.microsoft.com/sharepoint

---

*Dernière mise à jour : Octobre 2025*
*Version : 1.0*
*Statut : ✅ Développement initial terminé*

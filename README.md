# GéoMINDEVEL - Centres d'État Civil du Cameroun

Application web géospatiale interactive pour visualiser les 2531 Centres d'État Civil (CEC) du Cameroun.

![Version](https://img.shields.io/badge/version-1.0-green.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

## Démarrage Rapide

### Option 1: Ouverture Directe (Simple)

1. Ouvrez le fichier `index.html` dans votre navigateur web
2. Attendez le chargement des données (2-3 secondes)
3. Explorez la carte !

### Option 2: Serveur Local (Recommandé)

**Avec Python:**
```bash
cd geominddevel
python -m http.server 8000
```

**Avec Node.js:**
```bash
cd geominddevel
npx serve
```

Puis accédez à: `http://localhost:8000/index.html`

## Fonctionnalités

### 🗺️ Carte Interactive
- **2531 Centres d'État Civil** visualisés sur la carte
- **Fonds de carte**: OpenStreetMap ou Google Satellite
- **4 couches de données**: Régions, Départements, Arrondissements, CEC

### 🔍 Filtrage Avancé
- Recherche textuelle par nom de CEC
- Filtres géographiques en cascade (Région → Département → Commune)
- Filtres par type de CEC (Principal, Secondaire, C.U.)
- Statistiques dynamiques en temps réel

### 📍 Géolocalisation GPS
- Obtenir votre position actuelle
- Trouver les CEC les plus proches (3, 5 ou 10)
- Calcul et affichage des distances en kilomètres
- Lignes visuelles vers les CEC proches

### 📊 Statistiques
- Nombre total de CEC visibles
- Répartition par type
- Informations contextuelles selon les filtres

### 💡 Popups Détaillés
Cliquez sur un CEC pour afficher:
- Nom, type, commune, département, région
- Numéro de matriculation
- Code CEC et référence COG
- Observations et date

## Structure du Projet

```
geominddevel/
│
├── index.html                 # Application web complète
├── README.md                  # Ce fichier
├── cahier_des_charges.md      # Spécifications détaillées
└── resume_travaux.md          # Documentation technique
```

## Technologies Utilisées

- **HTML5** / **CSS3** / **JavaScript ES6+**
- **Leaflet.js 1.9.4** - Cartographie interactive
- **Supabase** - Base de données PostgreSQL/PostGIS
- **CDN** - Toutes les dépendances

## Base de Données

### Connexion Supabase
- URL: `https://hrlufnjhwhgddxkpyzst.supabase.co`
- 4 vues PostgreSQL créées pour optimiser l'accès aux données géospatiales

### Données
- **2531 CEC** (Centres d'État Civil)
- **10 Régions** avec polygones
- **58 Départements** avec polygones
- **360 Arrondissements** avec polygones

## Configuration Requise

### Navigateurs Supportés
- Chrome ≥ 90
- Firefox ≥ 88
- Safari ≥ 14
- Edge ≥ 90
- Navigateurs mobiles iOS/Android récents

### Réseau
- Connexion internet requise (chargement des données et tiles)
- ~3.2 MB de données téléchargées au démarrage

## Déploiement

### GitHub Pages
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/username/geominddevel.git
git push -u origin main
```
Activez GitHub Pages dans Settings → Pages

### Vercel
```bash
vercel deploy
```

### Netlify
Glissez-déposez le dossier sur [netlify.com/drop](https://app.netlify.com/drop)

## Documentation

- **[cahier_des_charges.md](cahier_des_charges.md)** - Spécifications complètes (13 sections)
- **[resume_travaux.md](resume_travaux.md)** - Documentation technique et résumé des travaux

## Utilisation

### Navigation
- **Zoom**: Molette de souris ou boutons +/-
- **Déplacement**: Clic et glisser
- **Popup**: Clic sur un élément (CEC, région, etc.)

### Filtres
1. Utilisez la barre latérale gauche
2. Sélectionnez une région (optionnel)
3. Sélectionnez un département (optionnel)
4. Sélectionnez une commune (optionnel)
5. Cochez/décochez les types de CEC
6. Recherchez par nom avec le champ de recherche

### Géolocalisation
1. Cliquez sur "Ma position GPS"
2. Autorisez l'accès à votre position
3. Sélectionnez le nombre de CEC proches à afficher
4. Cliquez sur "Trouver les CEC les plus proches"

### Couches
- Utilisez les cases à cocher en bas de la sidebar pour activer/désactiver:
  - Régions
  - Départements
  - Arrondissements
  - CEC

## Performance

- **Chargement initial**: 2-3 secondes
- **Filtrage**: Instantané (< 100ms)
- **Affichage**: Fluide avec les 2531 points

## Personnalisation

### Modifier les Couleurs
Éditez la section `<style>` dans `index.html`:
```css
#header {
    background: linear-gradient(135deg, #1a5632 0%, #2d8659 100%);
}
```

### Ajouter des Fonctionnalités
Le code JavaScript est dans la balise `<script>` de `index.html`.
Le code est modulaire et bien commenté.

## Dépannage

### La carte ne s'affiche pas
- Vérifiez votre connexion internet
- Ouvrez la console du navigateur (F12) pour voir les erreurs
- Essayez d'utiliser un serveur local au lieu d'ouvrir le fichier directement

### Pas de données
- Vérifiez que Supabase est accessible
- Vérifiez la console pour les erreurs de chargement

### Géolocalisation ne fonctionne pas
- Utilisez HTTPS (ou localhost)
- Autorisez l'accès à la position dans le navigateur
- Vérifiez que votre appareil a un GPS/réseau disponible

## Améliorations Futures

- [ ] Export CSV des données filtrées
- [ ] Mode impression
- [ ] PWA pour mode hors ligne
- [ ] Clustering pour zoom éloigné
- [ ] Calcul d'itinéraire
- [ ] Graphiques statistiques
- [ ] Mode sombre

## Licence

MIT License - Libre d'utilisation et de modification

## Auteur

**MINDEVEL**  
Date: Août 2026  
Version: 1.0

## Support

Pour toute question ou problème:
1. Consultez `cahier_des_charges.md` pour les spécifications
2. Consultez `resume_travaux.md` pour la documentation technique
3. Ouvrez la console du navigateur (F12) pour débugger

---

**Développé avec** ❤️ **par Claude Code**

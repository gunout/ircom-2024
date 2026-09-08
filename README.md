# 📊 IRCOM 2024 - Revenus fiscaux des foyers par département

Application interactive de visualisation des données IRCOM (Impôt sur le Revenu des personnes physiques) 2024, issue de la DGFiP (Direction Générale des Finances Publiques).

## 🗺️ Aperçu

L'application permet de visualiser et comparer les revenus fiscaux des foyers français par département à travers :
- Une **carte choroplèthe** interactive
- Un **système de comparaison** multi-départements
- Des **graphiques** (barres et radar) pour analyser les écarts
- Des **exports** d'images et de données

## ✨ Fonctionnalités

### Carte interactive
- Visualisation des indicateurs par département avec code couleur
- Popups détaillés avec toutes les données IRCOM
- Ajout rapide d'un département à la comparaison depuis la carte

### Comparaison de départements
- Sélection multiple via une liste déroulante
- Affichage en temps réel des valeurs comparées
- Graphique à barres comparatif
- Radar comparatif pour une vue d'ensemble

### Indicateurs disponibles
- 📊 RFR moyen par foyer fiscal
- 📈 Part des foyers imposés
- 💰 RFR moyen des foyers imposés
- 💳 Impôt net moyen par foyer
- 🏛️ Impôt net total
- 👨‍👩‍👧‍👦 Nombre de foyers fiscaux
- 🏠 Nombre de communes

### Exports
- PNG / JPG / SVG des graphiques de comparaison
- PNG / JPG / SVG du radar comparatif

## 📦 Structure du projet
  
    ircom-2024/
    ├── index.html # Application principale
    ├── departements-5m.geojson # Contours des départements (~43 Mo)
    ├── ircom_communes_complet_revenus_2024.json # Données IRCOM (~26 Mo)
    └── README.md # Documentation


## 🚀 Installation et lancement

### Prérequis
- Python 3 (pour le serveur HTTP)
- Un navigateur web moderne (Chrome, Firefox, Edge)

### Étapes

1. **Télécharger les fichiers**
   ```bash
   git clone https://github.com/gunout/ircom-2024.git
   cd ircom-2024
   python -m http.server 8000
   http://localhost:8000
   ```

   📊 Données
Source

    DGFiP - DESF (Direction des Études et Statistiques Fiscales)

    IRCOM 2025 (données sur les revenus localisés 2024)

    Fichier communes complet

Métriques
Indicateur	Description	Unité
RFR moyen	Revenu Fiscal de Référence moyen par foyer	€
Taux d'imposés	Part des foyers imposés	%
Impôt moyen	Impôt net moyen par foyer	€
Impôt total	Impôt net total	Md€
Nb foyers	Nombre total de foyers fiscaux	-
Nb communes	Nombre de communes	-
Notes

    Les montants RFR sont en milliers d'euros dans le fichier source

    L'application convertit automatiquement en euros pour l'affichage

    Les valeurs "n.c." (non communiquées) sont ignorées

🎨 Interface
En-tête

    KPIs nationaux : RFR moyen, taux d'imposés, impôt moyen, nombre de départements

Panneau de contrôle (à droite)

    📊 Sélecteur d'indicateur

    🗺️ Sélection multiple des départements à comparer

    🔍 Boutons "Comparer" et "Effacer"

    📋 Légende de la carte

    ℹ️ Nombre de départements chargés

Graphiques

    Barres : Comparaison des indicateurs sélectionnés

    Radar : Vue d'ensemble multi-critères

🛠️ Technologies utilisées

    Leaflet - Cartographie interactive

    Chart.js - Graphiques

    OpenStreetMap - Fonds de carte

    Vanilla JavaScript - Pas de framework

📱 Compatibilité

    ✅ Ordinateurs (écran large)

    ✅ Tablettes (responsive)

    ⚠️ Smartphones (partiellement compatible)


# EXAMPLE 

<img width="1816" height="892" alt="Screenshot 2026-09-08 at 05-01-42 IRCOM 2024 – Revenus fiscaux par département" src="https://github.com/user-attachments/assets/6f783d70-b540-488e-8f6a-ebdbd97f7430" />


## MIT License

Copyright (c) 2026 gunout

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

# 📊 IRCOM 2024 - Revenus fiscaux + Votes par département

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Made with JavaScript](https://img.shields.io/badge/Made%20with-JavaScript-blue.svg)](https://www.javascript.com/)

Application interactive de visualisation des données IRCOM (Impôt sur le Revenu des personnes physiques) 2024 superposées avec les résultats électoraux par département.

🔗 **Lien vers l'application :** [https://gunout.github.io/ircom-2024](https://gunout.github.io/ircom-2024)

---

## 🗺️ Aperçu

L'application permet d'analyser la corrélation entre les revenus fiscaux des foyers français et les votes politiques à travers :

- Une **carte choroplèthe** interactive des indicateurs IRCOM
- Une **superposition des votes** (1er tour présidentielle 2022) par département
- Un **système de comparaison** multi-départements avec graphiques
- Des **graphiques de corrélation** (Impôts vs Votes)

<img width="1816" height="auto" alt="Screenshot de l'application" src="https://github.com/user-attachments/assets/6f783d70-b540-488e-8f6a-ebdbd97f7430" />

---

## ✨ Fonctionnalités

### 🗺️ Carte interactive
- Visualisation des indicateurs IRCOM par département avec code couleur
- Superposition des votes des 11 candidats du 1er tour 2022
- Popups détaillés avec données IRCOM + résultats électoraux
- Ajout rapide d'un département à la comparaison depuis la carte

### 🔍 Comparaison de départements
- Sélection multiple via une liste déroulante
- Affichage en temps réel des valeurs comparées
- **Graphique à barres** comparatif
- **Radar comparatif** pour une vue d'ensemble multi-critères

### 📊 Indicateurs IRCOM disponibles
| Indicateur | Description | Unité |
|------------|-------------|-------|
| RFR moyen | Revenu Fiscal de Référence moyen par foyer | € |
| Taux d'imposés | Part des foyers imposés | % |
| RFR imposés | RFR moyen des foyers imposés | € |
| Impôt moyen | Impôt net moyen par foyer | € |
| Impôt total | Impôt net total | Md€ |
| Nb foyers | Nombre total de foyers fiscaux | - |
| Nb communes | Nombre de communes | - |

### 🗳️ Superposition des votes
- 11 candidats du 1er tour de l'élection présidentielle 2022
- Cercles proportionnels au pourcentage de voix
- Sélection du candidat à afficher
- Toggle ON/OFF pour afficher/masquer la couche

### 📈 Graphiques de corrélation "Impôts vs Votes"
- **Impôt moyen vs Votes** : Corrélation entre l'impôt moyen et le score du candidat
- **RFR moyen vs Votes** : Corrélation entre le RFR moyen et le score du candidat
- **Taux d'imposés vs Votes** : Corrélation entre le taux d'imposés et le score du candidat
- Exports PNG/JPG de chaque graphique

### 📤 Exports
- PNG / JPG / SVG des graphiques de comparaison
- PNG / JPG / SVG du radar comparatif
- PNG / JPG des graphiques de corrélation

---

## 📦 Structure du projet
    ircom-2024/
    ├── index.html # Application principale
    ├── departements-5m.geojson # Contours des départements (~43 Mo)
    ├── ircom_communes_complet_revenus_2024.json # Données IRCOM (~26 Mo)
    ├── README.md # Documentation
    └── LICENSE # Licence MIT


---

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
Source IRCOM

    DGFiP - DESF (Direction des Études et Statistiques Fiscales)

    IRCOM 2025 (données sur les revenus localisés 2024)

    Fichier communes complet

Source Votes

    Ministère de l'Intérieur - Élection présidentielle 2022 (1er tour)

    Données simulées pour la démonstration (remplaçables par les vraies données)

Notes

    Les montants RFR sont en milliers d'euros dans le fichier source

    L'application convertit automatiquement en euros pour l'affichage

    Les valeurs "n.c." (non communiquées) sont ignorées

    Les votes sont simulés pour la démonstration

🎨 Interface
En-tête

    KPIs nationaux : RFR moyen, taux d'imposés, impôt moyen, nombre de départements

Panneau de contrôle (à droite)

    📊 Sélecteur d'indicateur IRCOM

    🗳️ Sélection du candidat et toggle des votes

    🗺️ Sélection multiple des départements à comparer

    🔍 Boutons "Comparer", "Effacer" et "Corrélation"

    📋 Légende de la carte

    ℹ️ Nombre de départements chargés

## Graphiques

    Barres : Comparaison des indicateurs sélectionnés

    Radar : Vue d'ensemble multi-critères

    Corrélation : 3 graphiques Impôts vs Votes (nuages de points)

## 🛠️ Technologies utilisées
Technologie	Utilisation
Leaflet	Cartographie interactive
Chart.js	Graphiques et visualisations
OpenStreetMap	Fonds de carte
Vanilla JavaScript	Pas de framework

## 📱 Compatibilité

    ✅ Ordinateurs (écran large) - Navigation optimale

    ✅ Tablettes (responsive) - Interface adaptée

    ⚠️ Smartphones - Partiellement compatible (à améliorer)


## 📝 Licence  

MIT License

Copyright (c) 2026 gunout

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction...

---

<div align="center">

### 🇫🇷 Gunout · 2026

![Made in France](https://img.shields.io/badge/Made_in-France-002395?style=flat-square&labelColor=FFFFFF&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA5MDAgNjAwIj48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjYwMCIgZmlsbD0iIzAwMjM5NSIvPjxyZWN0IHdpZHRoPSI5MDAiIGhlaWdodD0iNDAwIiB5PSIxMDAiIGZpbGw9IiNmZmYiLz48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjIwMCIgeT0iNDAwIiBmaWxsPSIjZWQyOTM5Ii8+PC9zdmc+)
![GitHub](https://img.shields.io/badge/GitHub-gunout-181717?style=flat-square&logo=github&logoColor=white)
![Year](https://img.shields.io/badge/2026-ED2939?style=flat-square&labelColor=FFFFFF)

<sub>© 2026 <strong>gunout</strong> — Tous droits réservés.</sub>

</div>    

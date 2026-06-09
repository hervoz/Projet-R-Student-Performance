# Analyse des Performances des Étudiants

## Description du Projet

Ce projet réalise une analyse statistique complète des performances académiques d'étudiants. L'objectif est d'explorer les facteurs qui influencent les résultats scolaires à travers des visualisations, des tests statistiques et des modèles de régression.

L'analyse porte sur 1000 observations d'étudiants avec des informations sur leur genre, leur origine ethnique, le niveau d'éducation de leurs parents, le type de repas, leur participation à un cours de préparation, et leurs scores en mathématiques, lecture et écriture.

## Contenu du Projet

### Fichiers Principaux

- **Projet finale.R** : Script R contenant l'ensemble du code d'analyse
- **rapport finale.Rmd** : Document R Markdown avec explications détaillées et visualisations
- **rapport-finale.html** : Version HTML du rapport pour consultation dans un navigateur
- **StudentsPerformance.csv** : Données brutes contenant 1000 observations d'étudiants

## Préalables (Prérequis)

Avant de lancer le projet, assurez-vous que vous avez :

1. **R** installé sur votre ordinateur (version 3.6 ou plus récente)
   - Téléchargement : https://www.r-project.org/

2. **RStudio** (recommandé mais optionnel)
   - Téléchargement : https://www.rstudio.com/

3. **Les packages R suivants** à installer avec les commandes :

```
install.packages("readr")
install.packages("dplyr")
install.packages("ggplot2")
install.packages("broom")
install.packages("purrr")
install.packages("tidyr")
install.packages("tibble")
```

## Comment Utiliser

### Exécuter l'analyse complète

1. Ouvrez RStudio
2. Ouvrez le fichier `Projet finale.R`
3. Assurez-vous que le fichier `StudentsPerformance.csv` est dans le même dossier
4. Exécutez le script complet avec Ctrl+Shift+Enter (ou Cmd+Shift+Enter sur Mac)

### Consulter le rapport

Ouvrez simplement le fichier `rapport-finale.html` dans votre navigateur web pour voir l'analyse complète avec les graphiques et explications.

## Étapes de l'Analyse

### 1. Nettoyage des Données

L'analyse commence par importer les données et vérifier :
- La structure du tableau
- Les valeurs manquantes
- Les doublons
- La conversion des variables en facteurs pour les analyses catégorielles
- Le renommage des colonnes pour plus de clarté

### 2. Visualisations

Plusieurs graphiques sont créés pour explorer les données :

- **Histogramme** : Distribution des scores moyens
- **Boxplots** : Comparaison des scores par genre et niveau d'éducation parentale
- **Matrice de scatter plots** : Relations entre scores en mathématiques, lecture et écriture

### 3. Statistiques Descriptives

Calcul des moyennes, écarts-types et valeurs extrêmes pour chaque matière et le score global.

### 4. Tests d'Hypothèses

Trois tests statistiques pour vérifier les influences :

- **Test t** : Différence entre les genres
- **Test t** : Effet de la préparation au test
- **ANOVA** : Influence du niveau d'éducation parentale

### 5. Analyse des Corrélations

Matrice de corrélation entre les trois scores pour identifier les liens entre les matières.

### 6. Modélisation Linéaire

Trois modèles de régression progressive :

- **Modèle 1** : Prédire les scores en mathématiques avec la lecture et l'écriture (R² = 0.67)
- **Modèle 2** : Ajouter le genre et la préparation au test (R² = 0.85)
- **Modèle 3** : Ajouter le niveau d'éducation parentale (R² = 0.85)

### 7. Analyse des Résidus

Vérification de la qualité des modèles par l'analyse des résidus avec des Q-Q plots.

## Principaux Résultats

### Observations Clés

1. Les filles obtiennent des scores moyens plus élevés que les garçons (différence significative)

2. La préparation au test améliore considérablement les performances (augmentation moyenne de 7.7 points)

3. Le niveau d'éducation des parents influence les résultats :
   - Master's degree : 73.6 points
   - High school : 63.1 points

4. Les trois scores (mathématiques, lecture, écriture) sont fortement corrélés

5. Les modèles incluant le genre et la préparation au test expliquent 85% de la variance des performances

## Données Utilisées

Le fichier `StudentsPerformance.csv` contient :

- **1000 observations** (étudiants)
- **8 variables** :
  - gender : Sexe (male/female)
  - race/ethnicity : Origine ethnique (groups A-E)
  - parental level of education : Niveau d'éducation des parents
  - lunch : Type de repas (standard/free/reduced)
  - test preparation course : Préparation au test (none/completed)
  - math score : Score en mathématiques (0-100)
  - reading score : Score en lecture (0-100)
  - writing score : Score en écriture (0-100)

## Questions Répondues par l'Analyse

1. Comment les performances académiques sont-elles distribuées ?
2. Les garçons et les filles ont-ils les mêmes résultats ?
3. La préparation au test fait-elle une différence ?
4. L'éducation des parents influence-t-elle les résultats ?
5. Existe-t-il des corrélations entre les matières ?
6. Quel modèle prédit le mieux les performances en mathématiques ?

## Notes Techniques

- **Langage** : R
- **Format rapport** : R Markdown (Rmd) générant HTML
- **Environnement recommandé** : RStudio
- **Version R minimale** : 3.6
- **Packages principaux** : dplyr (manipulation), ggplot2 (visualisation), broom (modélisation)

## Interprétation des Graphiques

### Boxplots

Les boîtes représentent l'intervalle interquartile (50% des données). La ligne au centre est la médiane. Les points en dehors sont des valeurs extrêmes.

### Histogrammes

Montrent la fréquence des scores. Une forme en cloche indique une distribution normale.

### Q-Q Plots

Vérifient si les résidus suivent une distribution normale. Les points proches de la ligne diagonale indiquent une bonne qualité du modèle.

## Contact et Auteur

Projet réalisé comme analyse statistique des performances étudiantes.

## Licence

Ce projet est fourni à titre éducatif.

---

**Dernière mise à jour** : 2026-01-14

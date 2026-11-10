# Tarification automobile et prédiction des sinistres

Deux travaux d'actuariat non-vie sur des portefeuilles d'assurance automobile, réalisés à l'ESSAI.

## 1. Tarification et sinistres graves (`01_tarification_sinistres_graves.ipynb`)

- Contrôles de qualité sur environ **21 600 contrats** et leurs sinistres (cohérence entre bases, polices inexistantes, valeurs aberrantes).
- Séparation des sinistres **attritionnels** et **graves** : choix du seuil par la méthode **Peaks Over Threshold** (loi de Pareto généralisée, test de Kolmogorov-Smirnov, bootstrap).
- Prime pure = fréquence × coût moyen : **763 € par année-police** au global, puis déclinée par segment.

Projet réalisé en groupe dans le cadre du cours d'actuariat non-vie.

## 2. Prédiction des sinistres (`02_prediction_sinistres.ipynb`)

- Prédiction de la survenance d'un sinistre sur **58 592 polices**.
- Rééquilibrage des classes par **SMOTE** et sélection des variables par **RFECV**.
- Comparaison de plusieurs modèles (régression logistique, analyse discriminante, SVM, arbre, KNN, forêts aléatoires), avec intervalles de confiance de l'AUC.
- Les modèles simples atteignent une **AUC d'environ 0,61 à 0,63** : la survenance d'un sinistre reste difficile à prédire avec les seules variables disponibles.

## Données

Les données ne sont pas publiées dans ce dépôt.

Technologies : Python, pandas, scikit-learn, imbalanced-learn, SciPy.

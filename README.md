# 🫀 Modélisation prédictive de la mortalité – Insuffisance cardiaque

## 📌 Contexte

L'insuffisance cardiaque est une pathologie grave dont la mortalité reste élevée.
Ce projet vise à prédire le décès de patients atteints d'insuffisance cardiaque
à partir de variables cliniques, en comparant plusieurs modèles de classification supervisée.

**Dataset :** Heart Failure Clinical Records (UCI Machine Learning Repository)
- 299 patients
- 12 variables cliniques (âge, fraction d'éjection, créatinine sérique, etc.)
- Variable cible : `death_event` (0 = survie, 1 = décès)

---

## 🎯 Objectifs

- Réaliser une analyse exploratoire complète des données cliniques
- Comparer les performances de plusieurs modèles de classification
- Évaluer l'impact de la normalisation et de la sélection de variables

---

## 🛠️ Technologies utilisées

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-orange)
![pandas](https://img.shields.io/badge/pandas-data-lightgrey)
![seaborn](https://img.shields.io/badge/seaborn-viz-teal)

- **Langage :** Python
- **Librairies :** pandas, numpy, matplotlib, seaborn, scikit-learn

---

## 🔬 Méthodologie

### Partie 1 – Exploration et modélisation initiale
- Analyse exploratoire (pairplot, boxplots, histogrammes, matrice de corrélation)
- Entraînement de 5 modèles sans normalisation :
  - Logistic Regression, KNN, Decision Tree, Random Forest, SVM
- Retrait de la variable `time` (biais de causalité inversée)

### Partie 2 – Normalisation (StandardScaler)
- Application d'une normalisation sur les variables explicatives
- Comparaison des performances avant/après normalisation

### Partie 3 – Sélection de variables
- Suppression des variables peu discriminantes identifiées lors de l'EDA
- Nouvelle phase de modélisation sur le jeu de données réduit

---

## 📊 Résultats

| Modèle | Sans normalisation | Avec normalisation |
|---|---|---|
| Logistic Regression | ⚠️ Faible recall | ✅ Meilleur équilibre |
| Random Forest | ✅ Meilleure accuracy | ✅ Stable |
| SVM | ⚠️ Recall nul | ✅ Amélioré |
| KNN | ⚠️ Faible | ⚠️ Précision ok, recall faible |
| Decision Tree | 🔶 Correct | 🔶 Correct |

**Conclusion :** La Random Forest est le modèle le plus performant sans normalisation. Après normalisation, la Régression Logistique devient le modèle le plus équilibré.

---

## 👩‍💻 Auteure

**Noor Seba** – Étudiante en Master Épidémiologie, Données de Santé & Biostatistique
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Noor%20Seba-blue?logo=linkedin)](https://www.linkedin.com/in/noor-seba-260685369)

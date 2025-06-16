# 📊 Analyse Économétrique Qualitative – Assurance Automobile

### 🔍 Prédiction de la survenance d’un accident et modélisation du nombre d’accidents

---

## 📁 Contexte du projet

Ce projet s’inscrit dans le cadre de l’économétrie qualitative appliquée au secteur de l’assurance automobile.  
L’objectif principal est de **modéliser la probabilité de survenance d’un accident** à partir des caractéristiques des assurés,  
et de **modéliser le nombre d’accidents** pour les profils à risque élevé.

L’intérêt est stratégique pour les compagnies d’assurance : mieux comprendre les facteurs de risque permet d’**ajuster les primes**,  
d’**optimiser la prévention** et de **réduire les coûts liés aux sinistres**.

---

## 🧾 Données utilisées

- **Fichier source** : `ASSURANCE_MAKASI.csv`  
- **Origine** : Compagnie d’assurance IARD (Incendie, Accidents et Risques Divers)  
- **Nombre d’observations** : 382 154 clients  
- **Variables disponibles** : âge, sexe, marque du véhicule, type de carburant, conditions de conduite, etc.

---

## ❓ Problématique

- Quels sont les facteurs qui influencent significativement la survenance d’un accident ?
- Peut-on modéliser efficacement la **fréquence des accidents** pour affiner la tarification ?
- Comment améliorer un **modèle initial présentant 45% de taux d’erreur** ?

---

## 🎯 Objectifs

1. **Prédire la probabilité de survenance d’un accident** (binaire : Oui/Non) à l’aide d’une régression **logistique**.
2. **Modéliser le nombre d’accidents** par client grâce à une régression de **Poisson** ou **binomiale négative**, selon la dispersion des données.

---

## 🛠️ Méthodologie

### 🔹 Étape 0 – Prétraitement des données
- Suppression des doublons
- Gestion des valeurs manquantes
- Traitement des valeurs aberrantes
- Feature engineering (création de variables synthétiques, regroupement de modalités rares)

### 🔹 Étape 1 – Analyse univariée
- Description des variables quantitatives et qualitatives
- Vérification de la normalité
- Visualisations graphiques

### 🔹 Étape 2 – Analyse bivariée
- Croisement des variables qualitatives (tableaux de contingence)
- Analyse des relations entre variables quantitatives et catégorielles

### 🔹 Étape 3 – Analyses multidimensionnelles
- ACP / ACM
- Clustering

### 🔹 Étape 4 – Modélisation économétrique
- **Régression logistique** pour modéliser la variable binaire `ACCIDENT`
  - Validation avec test de Hosmer-Lemeshow
  - Courbes ROC / AUC
  - Sélection de variables via StepAIC et VIF
- **Régression de Poisson / Binomiale négative**
  - Modélisation du **nombre d’accidents**
  - Ajustement en cas de surdispersion

---

## 🧠 Résultats attendus

- Réduction du **taux d’erreur initial** de 45%
- Identification des **variables influentes** (ex. : âge du conducteur, ancienneté du véhicule)
- Un modèle de comptage robuste pour prévoir les profils à risque
- Recommandations stratégiques pour les compagnies d’assurance

---

## 🧰 Outils & Langages

- 📊 **R** (tidyverse, glm, MASS, caret, etc.)
- 🐍 **Python** (pandas, statsmodels, scikit-learn, seaborn)
- 🖥️ IDE : RStudio, Jupyter Notebook

---

## 📁 Fichiers disponibles

| Fichier                  | Description                                               |
|--------------------------|-----------------------------------------------------------|
| `ASSURANCE_MAKASI.csv`   | Jeu de données utilisé                                    |
| `script_analysis.R`      | Script R pour l’analyse statistique et la modélisation    |
| `model_logit_poisson.py` | Script Python pour les modèles logit et Poisson           |
| `rapport_final.pdf`      | Rapport détaillé du projet (avec interprétations)         |
| `README.md`              | Documentation du projet                                   |

---

## 🏁 Conclusion

Ce projet démontre l’intérêt de l’économétrie qualitative dans la prédiction de sinistres automobiles.  
Grâce à une approche rigoureuse combinant nettoyage, EDA, modélisation et validation, nous obtenons  
des modèles robustes capables de guider les décisions stratégiques des assureurs.

---

## 👨‍🎓 Réalisé par

**Kaba Mahamoud Toib**  
Master Statistique, Économétrie et Data Science  
INSEEDS – Institut Supérieur d’Études et de Recherche en Statistique

---

## 📬 Contact

Pour toute question ou suggestion, merci de me contacter via GitHub ou à l’adresse suivante :  
+2250576140830


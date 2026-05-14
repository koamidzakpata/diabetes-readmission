# 🏥 Prédiction de la Réadmission Hospitalière des Patients Diabétiques

![Python](https://img.shields.io/badge/Python-3.12-blue)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.x-orange)
![XGBoost](https://img.shields.io/badge/XGBoost-2.x-green)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## 📋 Description
Projet d'analyse prédictive sur le dataset **Diabetes 130-US Hospitals (1999–2008)**,
visant à prédire la réadmission hospitalière dans les 30 jours suivant la sortie
d'un patient diabétique.

> **Objectif** : Identifier les facteurs de risque clés et construire un modèle ML
> capable de détecter les patients à risque de réadmission précoce.

---

## 📊 Dataset
- **Source** : [Kaggle — Diabetes 130-US Hospitals](https://www.kaggle.com/datasets/brandao/diabetes)
- **Taille** : 101 766 entrées × 50 variables
- **Période** : 1999–2008, 130 hôpitaux américains

---

## 🔬 Méthodologie

données brutes → EDA → Preprocessing → Modélisation → Interprétabilité

### 1. 📈 Analyse Exploratoire (EDA)
- Analyse des valeurs manquantes
- Distribution de la variable cible
- Analyse par tranche d'âge, insuline, médicaments

### 2. 🧹 Preprocessing
- Suppression des colonnes > 40% manquantes
- Encodage des variables catégorielles (Label Encoding)
- Rééquilibrage des classes avec **SMOTE** (1:8 → 1:1)

### 3. 🤖 Modélisation
| Modèle | AUC-ROC |
|--------|---------|
| Logistic Regression | 0.7987 |
| Random Forest | **0.9541** 🏆 |
| XGBoost | 0.9388 |

### 4. 🔍 Interprétabilité
- SHAP Values pour expliquer les prédictions du Random Forest

---

## 💡 Insights Clés
- 🔴 Les patients **[20-30 ans]** ont le taux de réadmission le plus élevé (14.24%)
- 💊 La **réduction de la dose d'insuline** est le signal d'alerte le plus fort
- 📊 Plus un patient a de **médicaments**, plus son risque de réadmission est élevé
- 🏆 Le **Random Forest** atteint 91% d'accuracy et 0.95 d'AUC-ROC

---

## 📁 Structure du Projet

diabetes-readmission/
├── data/
│   ├── raw/                    ← dataset original
│   └── processed/              ← données nettoyées
├── notebooks/
│   ├── 01_EDA.ipynb
│   ├── 02_preprocessing.ipynb
│   ├── 03_modeling.ipynb
├── reports/
│   └── figures/                ← visualisations
├── requirements.txt
└── README.md

---

## 🚀 Installation

```bash
# Cloner le repo
git clone https://github.com/VOTRE_USERNAME/diabetes-readmission.git
cd diabetes-readmission

# Créer et activer l'environnement virtuel
python -m venv venv
venv\Scripts\activate  # Windows
source venv/bin/activate  # Mac/Linux

# Installer les dépendances
pip install -r requirements.txt
```

---

## 🛠️ Stack Technique
- **Python 3.12**
- **Pandas / NumPy** — Manipulation des données
- **Matplotlib / Seaborn** — Visualisation
- **Scikit-learn** — Modèles ML
- **XGBoost** — Gradient Boosting
- **Imbalanced-learn** — SMOTE
- **SHAP** — Interprétabilité

---

## 👤 Auteur
**DZAKPATA Koami Junior**
- LinkedIn : [linkedin.com/in/dzakpata-junior](https://linkedin.com/in/dzakpata-junior)
- GitHub : [github.com/koamidzakpata](https://github.com/koamidzakpata)
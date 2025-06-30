# 12-microsoft-fabric-lung-cancer-survival-prediction

This project focuses on predicting the survival of lung cancer patients using AutoML with [FlaML](https://github.com/microsoft/FLAML) and supporting the analysis through a Power BI dashboard.

---

## 📊 Objective

The main goals of this project are:

- To explore and preprocess a real-world medical dataset of lung cancer patients (890,000 records).
- To train and evaluate machine learning models using AutoML with **FlaML**.
- To predict patient survival (`survived` column) based on clinical and demographic features.
- To build an insightful **Power BI** report to support medical or public health decision-making.

---

## 🧠 Dataset Description

- **Source**: Provided for academic purposes
- **Rows**: 890,000 patients
- **Columns**: 17 features including demographic, clinical, and treatment information

### 📌 Key Features:
- `age`, `gender`, `bmi`, `smoking_status`, `cancer_stage`, `treatment_type`, etc.
- Target: `survived` (Yes/No)

---

## 🔁 Project Workflow

### 1. **Exploratory Data Analysis (EDA)**
- Missing value detection
- Class imbalance check
- Encoding categorical variables
- Correlation matrix and distribution analysis

### 2. **Preprocessing**
- Label encoding / One-hot encoding
- Normalization of continuous variables
- Feature selection and engineering
- Handling date variables: `diagnosis_date`, `end_treatment_date`

### 3. **Model Training with FlaML**
- AutoML run on classification task (`survived`)
- Hyperparameter tuning handled by FlaML
- Model evaluation: Accuracy, ROC AUC, Confusion Matrix

### 4. **Power BI Report**
- Importing predictions and raw data
- Visual KPIs: Survival rate by stage, treatment effectiveness, demographics
- Slicers for filtering: gender, country, smoking status

---

## 🚀 Technologies Used

- **Python 3.11**
- **FlaML** for lightweight AutoML modeling
- **Pandas, Scikit-learn, Matplotlib, Seaborn** for EDA and prep
- **Power BI** for interactive dashboard
- **Jupyter Notebooks** for development

---

## 📁 Repository Structure

lung-cancer-survival-prediction-flaml-powerbi/
├── data/
│   ├── lung_cancer_dataset.csv           # Fichier source (anonymisé ou échantillon)
│   └── data_dictionary.md                # Dictionnaire des colonnes du dataset
│
├── notebooks/
│   ├── 01_eda_preprocessing.ipynb        # Analyse exploratoire + preprocessing
│   ├── 02_model_training_flaml.ipynb     # AutoML avec FlaML + évaluation du modèle
│   └── 03_export_predictions.ipynb       # Export des résultats pour Power BI
│
├── outputs/
│   ├── predictions.csv                   # Résultats de prédiction avec probabilité
│   ├── evaluation_metrics.md             # Résumé des performances du modèle
│   └── model.pkl                         # Modèle entraîné (fichier sérialisé)
│
├── powerbi/
│   ├── lung_cancer_dashboard.pbix        # Rapport Power BI interactif
│   └── dashboard_screenshots/            # Captures d’écran du rapport
│       ├── survival_rate_by_stage.png
│       └── treatment_analysis.png
│
├── src/
│   ├── preprocessing.py                  # Fonctions de nettoyage, encodage, normalisation
│   ├── train_model.py                    # Script de training standalone avec FlaML
│   └── utils.py                          # Fonctions utilitaires (dates, visualisation, etc.)
│
├── requirements.txt                      # Librairies Python nécessaires
├── README.md                             # Présentation complète du projet
└── .gitignore                            # Fichiers/dossiers à exclure du versioning


## 📌 Results Preview

Power BI Dashboard: [Screenshot or GIF preview here]

# Disaster-Sentinel-Machine-Learning

This repository contains the machine learning part of the Disaster Sentinel Project, focused on flood prediction and analysis using hydrological, meteorological, and satellite data.

## Table of Contents
- [Overview](#overview)
- [Repository Structure](#repository-structure)
- [Datasets](#datasets)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Models](#models)
- [Data Sources](#data-sources)
- [Contributing](#contributing)
- [License](#license)

## Overview

The Disaster Sentinel ML project aims to predict flood events using machine learning techniques. This repository implements various machine learning models including:
- Random Forest
- XGBoost
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Logistic Regression
- Decision Trees

The project uses two primary datasets:
1. **CAMELS-IND**: A comprehensive dataset of Indian catchments with hydrological, meteorological, and catchment characteristics
2. **IndoFloods**: A dataset specifically focused on flood events in Indonesia

## Repository Structure

```
├── README.md                          # This file
├── LICENSE                           # Apache License 2.0
├── references.txt                    # Dataset references and citations
├── final_dataset.csv                 # Processed dataset ready for ML
├── eda_and_preprocessing.ipynb       # Data exploration and preprocessing
├── Explore_Indofloods.ipynb         # IndoFloods dataset exploration
├── random_forest.ipynb              # Random Forest model implementation
├── xgboost_model.ipynb              # XGBoost model implementation
├── svm.ipynb                        # SVM model implementation
├── knn.ipynb                        # K-NN model implementation
├── train_logistic.ipynb             # Logistic Regression model
├── train_decision_tree.ipynb        # Decision Tree model implementation
├── Camels Dataset/                  # CAMELS-IND dataset
│   ├── CAMELS_IND_All_Catchments/   # Complete dataset
│   └── CAMELS_IND_Catchments_Streamflow_Sufficient/  # Filtered dataset
└── Indofloods Dataset/              # IndoFloods dataset
    ├── floodevents_indofloods.csv
    ├── catchment_characteristics_indofloods.csv
    ├── precipitation_variables_indofloods.csv
    ├── metadata_indofloods.csv
    └── variables_description_indofloods.pdf
```

## Datasets

### CAMELS-IND Dataset
The CAMELS-IND dataset provides comprehensive information about Indian catchments including:
- **Hydrological signatures**: 64-73 attributes including streamflow characteristics
- **Climate indices**: 36-39 attributes including precipitation, temperature, and evapotranspiration
- **Topographic characteristics**: 14-16 attributes including elevation, slope, and area
- **Land cover characteristics**: 13 attributes including vegetation and land use
- **Soil characteristics**: 27-28 attributes including soil composition and properties
- **Geological characteristics**: 7 attributes including rock types and geological features
- **Anthropogenic influences**: 13-25 attributes including human activities and infrastructure

### IndoFloods Dataset
The IndoFloods dataset focuses specifically on flood events and includes:
- **Flood events**: Detailed information about flood occurrences, duration, and severity
- **Catchment characteristics**: Physical and hydrological properties of catchments
- **Precipitation variables**: Meteorological data related to flood events
- **Metadata**: Additional information about gauging stations and data quality

## Requirements

### Python Version
- Python 3.8 or higher

### Core Libraries
```
numpy>=1.21.0
pandas>=1.3.0
matplotlib>=3.5.0
seaborn>=0.11.0
scikit-learn>=1.0.0
xgboost>=1.5.0
imbalanced-learn>=0.8.0
```

### Optional Libraries for Advanced Features
```
jupyter>=1.0.0
ipykernel>=6.0.0
```

## Installation

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/Disaster-Sentinel-Machine-Learning.git
cd Disaster-Sentinel-Machine-Learning
```

### 2. Create a Virtual Environment (Recommended)
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

If `requirements.txt` is not available, install the dependencies manually:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn xgboost imbalanced-learn jupyter ipykernel
```

### 4. Download Datasets

#### CAMELS-IND Dataset
1. Visit the official CAMELS-IND dataset page: https://essd.copernicus.org/articles/17/461/2025/
2. Download the dataset files
3. Extract the files to the `Camels Dataset/` directory

#### IndoFloods Dataset
1. Visit the IndoFloods dataset page: https://journals.ametsoc.org/view/journals/bams/106/2/BAMS-D-24-0008.1.xml
2. Download the dataset files
3. Extract the files to the `Indofloods Dataset/` directory

### 5. Setup Jupyter Notebook (Optional)
```bash
jupyter notebook
```

## Usage

### Step 1: Data Exploration and Preprocessing
Start with the data exploration notebook to understand the datasets:
```bash
jupyter notebook eda_and_preprocessing.ipynb
```

This notebook covers:
- Data loading and inspection
- Missing value analysis and handling
- Feature engineering
- Data visualization
- Dataset preparation for ML models

### Step 2: IndoFloods Dataset Exploration
Explore the IndoFloods dataset:
```bash
jupyter notebook Explore_Indofloods.ipynb
```

### Step 3: Model Training and Evaluation
Choose and run the appropriate model notebook:

#### Random Forest
```bash
jupyter notebook random_forest.ipynb
```

#### XGBoost
```bash
jupyter notebook xgboost_model.ipynb
```

#### Support Vector Machine
```bash
jupyter notebook svm.ipynb
```

#### K-Nearest Neighbors
```bash
jupyter notebook knn.ipynb
```

#### Logistic Regression
```bash
jupyter notebook train_logistic.ipynb
```

#### Decision Tree
```bash
jupyter notebook train_decision_tree.ipynb
```

### Step 4: Model Comparison and Selection
Each model notebook includes:
- Data preprocessing and feature engineering
- Model training with hyperparameter tuning
- Model evaluation using multiple metrics
- Visualization of results
- Feature importance analysis (where applicable)

## Models

### 1. Random Forest
- **File**: `random_forest.ipynb`
- **Features**: Handles imbalanced datasets, feature importance analysis
- **Techniques**: SMOTE for class balancing, cross-validation

### 2. XGBoost
- **File**: `xgboost_model.ipynb`
- **Features**: Gradient boosting, high performance
- **Techniques**: Feature engineering, hyperparameter optimization

### 3. Support Vector Machine
- **File**: `svm.ipynb`
- **Features**: Kernel-based classification, data scaling
- **Techniques**: StandardScaler preprocessing, SMOTE balancing

### 4. K-Nearest Neighbors
- **File**: `knn.ipynb`
- **Features**: Distance-based classification
- **Techniques**: Feature scaling, optimal k selection

### 5. Logistic Regression
- **File**: `train_logistic.ipynb`
- **Features**: Linear classifier, probability estimates
- **Techniques**: Regularization, class balancing

### 6. Decision Tree
- **File**: `train_decision_tree.ipynb`
- **Features**: Interpretable model, feature importance
- **Techniques**: Pruning, visualization

## Data Sources

### CAMELS-IND Dataset
- **Citation**: Refer to the official publication at https://essd.copernicus.org/articles/17/461/2025/
- **License**: Check the dataset documentation for usage terms
- **Version**: 2.2 (March 2025)

### IndoFloods Dataset
- **Citation**: Refer to the official publication at https://journals.ametsoc.org/view/journals/bams/106/2/BAMS-D-24-0008.1.xml
- **License**: Check the dataset documentation for usage terms

## Key Features

### Data Preprocessing
- Missing value imputation using linear interpolation
- Feature engineering including lag features and rolling statistics
- Data normalization and scaling
- Handling of imbalanced datasets using SMOTE

### Model Evaluation
- Classification metrics (Precision, Recall, F1-score)
- Confusion matrix analysis
- Precision-Recall curves
- Feature importance analysis
- Cross-validation

### Visualization
- Data distribution plots
- Correlation heatmaps
- Time series plots
- Model performance visualizations
- Feature importance plots

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -am 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Create a Pull Request

## License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- CAMELS-IND dataset contributors
- IndoFloods dataset contributors
- The scientific community for providing open-access datasets for flood research

## Contact

For questions or collaboration, please open an issue in this repository.

---

**Note**: This project is part of the larger Disaster Sentinel Project focused on disaster prediction and early warning systems.

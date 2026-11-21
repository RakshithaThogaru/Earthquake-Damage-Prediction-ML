# Earthquake Damage Prediction Using Machine Learning

## Project Overview

This project aims to predict the level of earthquake-induced damage to buildings using machine learning techniques. By analyzing structural, geographical, and building-related characteristics, the project explores how data-driven models can support earthquake damage assessment and disaster risk management.

The project involves data preprocessing, exploratory data analysis, feature engineering, model development, performance evaluation, and feature importance analysis.

## Problem Statement

Earthquakes can cause significant damage to buildings and infrastructure, resulting in loss of life, economic losses, and displacement of communities. Assessing building damage efficiently is essential for disaster response and recovery planning.

The objective of this project is to develop machine learning models that classify buildings into different damage categories based on their characteristics.

## Dataset

The project uses the Nepal Earthquake Building Damage Dataset.

- **Total records:** 260,601 buildings
- **Independent features:** 38
- **Target variable:** `damage_grade`
- **Damage categories:**
  - Grade 1: Low damage
  - Grade 2: Medium damage
  - Grade 3: Almost complete destruction

### Target Distribution

| Damage Grade | Number of Buildings | Percentage |
|---|---:|---:|
| Grade 1 | 25,124 | 9.64% |
| Grade 2 | 148,259 | 56.89% |
| Grade 3 | 87,218 | 33.47% |
| **Total** | **260,601** | **100%** |

The dataset contains structural features, geographical identifiers, building age, height, number of floors, foundation type, roof type, ground floor type, and other construction-related characteristics.

## Project Workflow

1. Data loading and merging
2. Data validation and quality checks
3. Exploratory Data Analysis (EDA)
4. Target variable analysis
5. Numerical and categorical feature analysis
6. Correlation analysis
7. Feature selection
8. Data preprocessing
9. Train-test splitting
10. Model development
11. Model evaluation and comparison
12. Feature importance analysis
13. Earthquake damage mitigation recommendations

## Exploratory Data Analysis

Exploratory Data Analysis was performed to understand the dataset, identify patterns, and analyze the relationship between building characteristics and earthquake damage.

Key analyses included:

- Damage grade distribution
- Building age distribution
- Number of floors
- Building height
- Building area
- Foundation type
- Roof type
- Ground floor type
- Structural characteristics
- Geographical distribution
- Correlation analysis
- Damage patterns across different building characteristics

## Data Preprocessing

The following preprocessing techniques were implemented:

- Merging training features and target labels using `building_id`
- Removing irrelevant identifiers and derived EDA-only features from model inputs
- Stratified train-test split (80% training and 20% testing)
- Standardization of numerical features using `StandardScaler`
- One-hot encoding of categorical features using `OneHotEncoder`
- Retaining binary features without additional encoding
- Handling unseen categorical values using `handle_unknown='ignore'`

The preprocessing pipeline transformed the original features into a machine-learning-ready representation.

## Machine Learning Models

Three models were developed and compared.

### 1. Baseline Classifier

A Dummy Classifier using the most frequent class was implemented to establish baseline performance.

### 2. Decision Tree Classifier

A Decision Tree model was developed to identify nonlinear patterns and relationships between building characteristics and damage levels.

### 3. Random Forest Classifier

A Random Forest model was implemented using multiple decision trees to improve predictive performance and generalization.

Class weighting was used to address class imbalance, and stratified sampling was applied during model development.

## Model Evaluation

The models were evaluated using the following metrics:

- Accuracy
- Precision
- Recall
- F1-score
- Macro F1-score
- Weighted F1-score
- Confusion Matrix

### Model Performance Comparison

| Model | Accuracy | Macro F1-score | Weighted F1-score |
|---|---:|---:|---:|
| Baseline Classifier | 0.57 | 0.24 | 0.41 |
| Decision Tree | 0.35 | 0.32 | 0.32 |
| Random Forest | 0.47 | 0.46 | 0.45 |

The Random Forest model achieved the highest Macro F1-score and Weighted F1-score among the developed machine learning models.

## Feature Importance

Feature importance analysis was performed using the Random Forest model to identify influential factors associated with building damage prediction.

Important features included:

- Ground floor type
- Foundation type
- Roof type
- Geographical location identifiers
- Building structural characteristics

The analysis highlights the importance of building construction characteristics and geographical factors in predicting earthquake damage.

## Key Findings

- The dataset exhibits significant class imbalance, with Grade 2 damage representing the majority of observations.
- Structural characteristics play an important role in damage classification.
- Geographical features contribute to identifying damage patterns.
- The Random Forest model achieved the best overall F1-score performance among the evaluated models.
- The classification task remains challenging due to class imbalance and the complexity of earthquake damage patterns.

## Challenges and Limitations

- Imbalanced target classes
- High-dimensional feature representation after categorical encoding
- Complex geographical and structural relationships
- Limited model performance
- Computational constraints during model training
- Further validation required before real-world deployment

## Conclusion

This project demonstrates the application of machine learning techniques to earthquake-induced building damage prediction.

Among the evaluated models, Random Forest achieved the best overall performance based on Macro F1-score and Weighted F1-score. Exploratory data analysis and feature importance analysis provided insights into the relationship between building characteristics, geographical factors, and earthquake damage.

The developed framework can serve as a foundation for further research into earthquake damage assessment and disaster risk analysis. However, additional model optimization, validation, and performance improvement are necessary before practical deployment.

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Repository Contents

- `Earthquake_Damage_Prediction.ipynb` – Complete project notebook containing data analysis, preprocessing, model development, evaluation, visualizations, and conclusions.

## Author

**Rakshitha Thogaru**

GitHub: [RakshithaThogaru](https://github.com/RakshithaThogaru)


# ML-project
# Breast Cancer

This repository contains a **Jupyter Notebook** that applies **Machine Learning** techniques for the analysis and classification of breast cancer data.  
The goal is to develop a predictive model that can support early diagnosis.

---

## Project Context
This project was developed as part of an exam in the **Bioinformatics** program at the **University of Bologna**.  
It is intended **for educational and research purposes only**.

---

## Dataset
This project uses the Breast Cancer Wisconsin (Diagnostic) dataset, 
available in `sklearn.datasets.load_breast_cancer`.

- 569 samples, 30 numeric features
- Target: 0 = malignant, 1 = benign
- Source: [UCI Machine Learning Repository]('https://archive.ics.uci.edu/ml/machine-learning-databases/breast-cancer-wisconsin/wdbc.data')
### Dataset Features

The dataset is built from **10 basic characteristics** of breast cell nuclei, each measured in three ways (mean, standard error, worst).  
This results in a total of **30 features**.  

### Base Characteristics

- **Radius** → mean distance from the nucleus center to the perimeter  
- **Texture** → variation in gray-scale pixel intensity (standard deviation of image values)  
- **Perimeter** → length of the nucleus boundary  
- **Area** → size (area) of the nucleus  
- **Smoothness** → local variation of radius lengths (measures how smooth or irregular the edges are)  
- **Compactness** → combination of perimeter and area (perimeter² / area – 1.0), relates to how compact the shape is  
- **Concavity** → severity of concave (inward-curving) parts of the nucleus contour  
- **Concave points** → number of distinct concave (inward) portions of the contour  
- **Symmetry** → degree of symmetry of the nucleus shape  
- **Fractal dimension** → measure of the complexity of the contour (approximation of fractal dimension, like "coastline complexity")  

### Measurement Types

- **Mean (suffix 1):** average value across nuclei  
- **Standard Error (suffix 2):** variability of the measurement  
- **Worst (suffix 3):** maximum or most extreme value observed  

---

## Project Workflow

1. **Data Preprocessing**  
   - Removed the non-informative `ID` column  
   - Encoded target variable (`M = 1`, `B = 0`)  
   - Standardized features with `StandardScaler`  
   - Balanced classes using **SMOTE**  

2. **Exploratory Data Analysis (EDA)**  
   - Class distribution visualization  
   - Correlation heatmap  
   - Statistical summary of features  

3. **Modeling**  
   Implemented and compared:  
   - Logistic Regression  
   - Random Forest  
   - K-Nearest Neighbors  

4. **Evaluation**  
   - Confusion Matrix  
   - ROC Curve & AUC  
   - 5-fold Cross-Validation  
   - Feature Importance (Random Forest)
   - Computed **Permutation Importance** for KNN and Logistic Regression to compare interpretability across different algorithms

5. **Hyperparameter Tuning**  
   - Applied `GridSearchCV` for Logistic Regression  

---

## Results & Insights

- **Random Forest** achieved the highest AUC, showing robustness and strong predictive ability.  
- **Logistic Regression** performed surprisingly well, reinforcing its role as a strong, interpretable baseline.  
- Balancing the dataset with **SMOTE** improved recall for the malignant class, reducing false negatives.  

**Interpretation of Feature Importance**  
The most influential features in Random Forest were related to **radius, perimeter, area, and concavity**, which align with medical understanding:  
larger and irregular nuclei are often malignant.  

---

## Future Work

- Explore advanced algorithms: XGBoost, SVM, Deep Learning  
- Use dimensionality reduction (PCA, t-SNE) for visualization  
- Apply **SHAP** or **LIME** for interpretability  
- Extend analysis to clinical datasets  

---

## License
Distributed under the MIT License.

---

## Disclaimer
This project is developed for educational purposes only within the Bioinformatics course at the University of Bologna.
It must not be used as a medical diagnostic tool.



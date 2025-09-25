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

##  How to Use
1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/breast-cancer-ml.git
   cd breast-cancer-ml
2. Install the required libraries (ensure you have Jupyter Notebook and the libraries listed at the beginning of the .ipynb file installed).
3. Run Jupyter Notebook
4. Open and execute the file

---

## License
Distributed under the MIT License.

---

## Disclaimer
This project is developed for educational purposes only within the Bioinformatics course at the University of Bologna.
It must not be used as a medical diagnostic tool.



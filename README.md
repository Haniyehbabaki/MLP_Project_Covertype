# 🌲 MLP Project - Forest Cover Type Classification

This project applies a **Multi-Layer Perceptron (MLP)** model to classify forest cover types using the **Covertype dataset** from the UCI Machine Learning Repository.  
It was developed as part of the **Computational Intelligence** course and explores model performance under different architectures and class balancing techniques.

---

## 📊 Dataset Information

- **Dataset name:** Covertype  
- **Source:** [UCI Machine Learning Repository - Covertype](https://archive.ics.uci.edu/ml/datasets/covertype)  
- **Number of features:** 54  
- **Target variable:** `Cover_Type` (7 classes representing forest cover types)  
- **Total samples:** 581,012  

The dataset describes the forest cover type for each observation using cartographic variables such as elevation, slope, soil type, and wilderness area.
---

## 🧰 Libraries Used

The following Python libraries were used in this project:
`pandas`,`numpy`,`matplotlib`,`seaborn`,`scikit-learn`,`tensorflow` / `keras`, `ucimlrepo`,`tabulate`
---

## 🔍 Project Workflow

### 1️⃣ Data Loading & Exploration
- Load the Covertype dataset using the `ucimlrepo` library.  
- Display dataset structure, feature types, and class distribution.  
- Visualize the class imbalance using **seaborn bar plots**.

### 2️⃣ Data Preprocessing
- Handle missing values (if any).  
- Normalize features using `StandardScaler`.  
- Split the data into **train (70%)**, **validation (15%)**, and **test (15%)** sets with stratified sampling.  
- Compute **class weights** to handle imbalance.

### 3️⃣ Model Building
- Build multiple **MLP architectures** with different:
  - hidden layer configurations (`[64,32]`, `[128,64,32]`, `[256,128,64]`)
  - activation functions (`relu`, `tanh`, `sigmoid`)
  - optimizers (`adam`, `sgd`, `rmsprop`)
  - learning rates and batch sizes
- Use **EarlyStopping** to prevent overfitting.

### 4️⃣ Model Training & Evaluation
- Train **3 random MLP models** with and without class balancing.
- Evaluate models based on:
  - Precision
  - Recall
  - F1-score
  - Accuracy  
- Display and compare **confusion matrices** and summary tables for each model.

### 5️⃣ Feature Importance (Permutation Importance)
- Evaluate feature importance by **measuring accuracy drop** when features are permuted.  
- Visualize results using bar plots to identify which features impact performance most.
---

## 📈 Results Summary

- Models are trained and evaluated **10 times** each to obtain stable mean and standard deviation of metrics.  
- Both **balanced and unbalanced** versions of each model are compared.  
- The **best model** is automatically selected based on the highest mean accuracy.
---

## Author
Haniyeh Babaki
B.Sc. Student in Computer Engineering
Damghan university
   ```bash
   git clone https://github.com/Haniyehbabaki/MLP_Project_Covertype.git

# 🍷 Wine Quality Prediction using Decision Tree Classifier

## 📘 Project Overview

This Python project analyzes the physicochemical properties of Portuguese "Vinho Verde" to **predict wine quality** using a **Decision Tree Classifier**. The goal is to automate and interpret wine evaluation based on objective chemical data, replacing traditional sensory analysis.

---

## 📊 Dataset Source

* **Dataset**: Wine Quality – Red Wine
* **Source**: [Kaggle](https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009?resource=download)
* **Features Used**:

  * Alcohol, Volatile Acidity, Sulphates, Density, Citric Acid, etc.
  * **Target**: Wine quality score (from 0 to 10, but simplified to good or bad quality)

---

## 🧠 Key Features

### 1. **Data Analysis**

* Correlation analysis to identify the most relevant attributes
* Data cleaning and inspection
* Creation of a binary target variable (good vs bad quality)

### 2. **Model Construction**

* Use of **Decision Tree Classifier** from `scikit-learn`
* Criterion: **Entropy** (Information Gain)
* Model training and prediction using training/test split

### 3. **Evaluation**

* Model accuracy and confusion matrix
* Feature importance ranking
* Tree visualization using `plot_tree` for explainability

---

## 📦 Requirements

* Python 3.x
* Required libraries:

  ```bash
  pip install pandas seaborn matplotlib scikit-learn
  ```

---

## ▶️ How to Use

1. Clone this repository:

   ```bash
   git clone https://github.com/ViniciusCastellani/wine-quality-classification
   cd wine-quality-classification
   ```

2. Run the notebook:

   ```bash
   jupyter notebook exercicio_arvore_decisao_vinho.ipynb
   ```

3. Explore the code step-by-step:

   * Data preprocessing
   * Model training
   * Accuracy evaluation
   * Tree visualization and interpretation

---

## 🧪 Code Structure

1. **Data Loading**

   * Load the CSV file directly from UCI or local directory
   * Inspect and prepare dataset

2. **Exploratory Analysis**

   * Use of `seaborn` heatmap for correlation
   * Distribution plots for alcohol, density, and acidity

3. **Model Building**

   * Binary classification target:

     * 1 (Good quality: score ≥ 7)
     * 0 (Bad quality: score < 7)
   * Train/test split
   * Fit Decision Tree with entropy criterion

4. **Evaluation & Visualization**

   * Confusion matrix
   * Accuracy score
   * Plotting the decision tree with `max_depth` for readability
   * Feature importance ranking

---

## 📈 Results

* Model achieved approximately **87% accuracy**
* Most important features for good wine classification:

  * **Alcohol**, **Citric Acid**, and **Sulphates**
* Features indicating poor quality:

  * **High Volatile Acidity**, **Density**, **Total Sulfur Dioxide**
* The decision tree allows **transparent and explainable predictions**

---

## 💬 Interpretation

* **Good Quality Wines**:

  * High alcohol content
  * Moderate to high citric acid
  * Balanced levels of sulphates and fixed acidity

* **Poor Quality Wines**:

  * High volatile acidity (sourness)
  * Higher density (possibly due to residual sugar)
  * High sulfur dioxide (which may affect flavor)
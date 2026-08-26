# 💻 Laptop Price Prediction

A Machine Learning regression project that predicts laptop prices based on hardware specifications, brand, display features, storage, processor, graphics, and other relevant characteristics.

> 🚧 **Project Status:** Frontend Development and Model Integration — Upcoming

---

## 📌 Project Overview

Laptop prices vary significantly depending on specifications such as **RAM, CPU, GPU, storage, display quality, laptop type, and brand**.

The objective of this project is to build a regression model capable of predicting the price of a laptop from its specifications.

The project follows an end-to-end Machine Learning workflow:

```text
Raw Dataset
     ↓
Data Cleaning
     ↓
Exploratory Data Analysis
     ↓
Feature Engineering
     ↓
Data Preprocessing
     ↓
Model Training
     ↓
Model Comparison
     ↓
Best Model Selection
     ↓
Hyperparameter Tuning
     ↓
Deployment
```

---

## 📊 Dataset

The dataset contains **1,303 laptop records** with information about:

* Company
* Laptop Type
* Screen Resolution
* CPU
* RAM
* Memory
* GPU
* Operating System
* Screen Size
* Weight
* Price

The original dataset contained a mixture of numerical and text-based features, so preprocessing and feature engineering were required before model training.

---

# 🔍 Exploratory Data Analysis

EDA was performed to understand the structure and characteristics of the dataset before building the models.

### EDA Performed

* Examined dataset shape and feature types
* Checked for missing values
* Identified unnecessary columns
* Analyzed categorical feature distributions
* Studied numerical feature distributions
* Examined the distribution of laptop prices
* Investigated relationships between features and price
* Analyzed correlations between numerical variables
* Identified potential outliers

### Key Findings

* The dataset contains **1,303 laptop records**.
* No significant missing-value problem was found.
* `Unnamed: 0` was identified as an unnecessary index column.
* **8GB RAM** is the most common RAM configuration.
* Notebook laptops represent the largest category.
* Dell, Lenovo, and HP are among the most frequently represented brands.
* The `Price` variable is **right-skewed**, with some high-priced laptops.
* RAM showed a strong positive relationship with laptop price.
* Screen size alone showed a relatively weak relationship with price.

EDA helped identify which characteristics were likely to be useful for predicting laptop prices and guided the feature engineering process.

---

# ⚙️ Feature Engineering

The original dataset contained several features in raw text/string form. These were transformed into structured features that could be effectively used by Machine Learning algorithms.

### Transformations Performed

* Extracted numerical values from **RAM**
* Converted **Weight** into a numerical value
* Simplified **Operating System** categories
* Converted **TouchScreen** into a binary feature
* Converted **IPS** into a binary feature
* Engineered **PPI (Pixels Per Inch)** using screen resolution and screen size
* Extracted **CPU Brand**
* Separated combined storage into **HDD** and **SSD** capacities
* Extracted **GPU Brand**
* Removed unnecessary information from complex specification strings

### Why Feature Engineering?

Feature engineering helped transform complicated laptop specifications into meaningful numerical and categorical variables.

For example:

```text
8GB RAM → 8
1TB HDD → 1000 GB HDD
256GB SSD → 256 GB SSD
Touchscreen → 1 / 0
IPS Display → 1 / 0
```

The resulting dataset became significantly more suitable for Machine Learning models.

---

# 🤖 Model Development & Selection

After preprocessing the dataset, **10 different regression algorithms** were trained and evaluated to determine which model performed best for this problem.

### Models Tested

* Linear Regression
* Lasso Regression
* Ridge Regression
* KNN Regressor
* Decision Tree Regressor
* Random Forest Regressor
* AdaBoost Regressor
* Gradient Boosting Regressor
* Extra Trees Regressor
* XGBoost Regressor
* SVR

> The models were compared using **Mean Absolute Error (MAE)** and **R² Score**.

---

## 📈 Model Comparison

The models showed noticeable differences in performance.

Based on the evaluation results:

* **Random Forest Regressor** achieved the best overall performance.
* Extra Trees and XGBoost also performed strongly.
* KNN and boosting-based models produced competitive results.
* Linear, Ridge, and Lasso Regression performed reasonably well but were less effective at capturing the complex relationships in the dataset.
* **SVR performed significantly worse** than the other tested models.

### 🏆 Best Model: Random Forest Regressor

The **Random Forest Regressor** was selected as the current best-performing model because it provided the strongest combination of:

* High **R² Score**
* Low **Mean Absolute Error**
* Ability to capture **non-linear relationships**
* Robustness to different feature interactions

The results suggest that laptop pricing depends on complex interactions between specifications such as RAM, CPU, GPU, storage, display characteristics, and laptop category—relationships that tree-based ensemble models can capture effectively.

---

# 🧠 Why Random Forest?

Random Forest is particularly suitable for this dataset because laptop prices are unlikely to follow a simple linear relationship.

For example:

```text
RAM + CPU + GPU + SSD + Display
              ↓
        Price Relationship
```

The effect of one feature can depend on the values of other features.

Random Forest can capture these **non-linear relationships and feature interactions** by combining predictions from multiple decision trees.

---

# 🚧 Future Work

### Model Evaluation

Further evaluation will include:

* MAE
* MSE
* RMSE
* R² Score
* Cross-validation performance
* Actual vs Predicted price analysis
* Residual/error analysis

---

# 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **XGBoost**
* **Jupyter Notebook**
* **Git & GitHub**

---

# 📁 Project Structure

The project structure may continue to evolve as new stages are added.

```text
Laptop-Price-Prediction/
│
├── dataset/
│   └── laptop_data.csv
│
├── notebooks/
│   ├── Laptop-Price-Predictor.ipynb
│   
│    
│
├── models/
│   └── ...
│
├── app/
│   └── ...
│
|
├── README.md
└── .gitignore
```

---

# 📈 Project Progress

* [x] Dataset Collection
* [x] Data Cleaning
* [x] Exploratory Data Analysis
* [x] Feature Engineering
* [x] Data Preprocessing
* [x] Regression Model Training
* [x] Model Comparison
* [x] Best Model Selection
* [x] Hyperparameter Tuning
* [x] Final Model

---

# 🎯 Final Objective

The ultimate goal of this project is to develop a reliable **Laptop Price Prediction system** capable of estimating laptop prices from their specifications while demonstrating a complete real-world Machine Learning workflow:

**Data → EDA → Feature Engineering → Modeling → Evaluation → Optimization**

---

## 👨‍💻 Author

**Hassan Ibrahim**

This project is part of my Machine Learning journey, focusing on applying theoretical concepts to practical, end-to-end Machine Learning projects.

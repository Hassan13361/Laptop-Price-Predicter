# 💻 Laptop Price Prediction

A Machine Learning project focused on predicting laptop prices based on their hardware specifications, brand, display characteristics, storage, processor, graphics, and other relevant features.

> 🚧 **Project Status:** In Progress
> The project is currently in the **EDA and Feature Engineering** phase. Model training, evaluation, and deployment will be added in future stages.

---

## 📌 Project Overview

Laptop prices vary significantly depending on specifications such as RAM, processor, GPU, storage, display quality, and laptop category.

The goal of this project is to build a **regression-based Machine Learning model** that can learn from historical laptop specifications and predict the expected price of a laptop.

The project is being developed step-by-step, starting from raw data exploration and gradually moving toward preprocessing, model development, evaluation, and deployment.

---

## 📊 Dataset

The dataset contains **1,303 laptop records** with information related to:

* Company / Brand
* Laptop Type
* Screen Resolution
* CPU
* RAM
* Memory / Storage
* GPU
* Operating System
* Screen Size
* Weight
* Price

The dataset initially contained a mixture of numerical and text-based features, requiring preprocessing and feature engineering before Machine Learning could be applied.

---

## 🔍 Exploratory Data Analysis

During EDA, the dataset was analyzed to understand its structure, distributions, relationships, and potential issues.

### Key EDA Steps

* Examined dataset shape and feature types
* Checked for missing values
* Identified unnecessary columns
* Analyzed categorical feature distributions
* Studied numerical feature distributions
* Investigated the distribution of laptop prices
* Analyzed relationships between features and price
* Identified potential outliers
* Examined correlations between numerical variables

### Key Findings

* The dataset contains **no missing values**.
* `Unnamed: 0` was identified as an unnecessary index column.
* **8GB RAM** is the most common RAM configuration.
* Notebook laptops represent the largest laptop category.
* Dell, Lenovo, and HP are among the most frequently occurring brands.
* Laptop prices are **right-skewed**, with relatively expensive laptops forming the upper end of the distribution.
* RAM has a strong positive relationship with laptop price.
* Screen size alone has a relatively weak relationship with price.

---

## ⚙️ Feature Engineering

The original dataset contained several features in text/string format. These were transformed into more meaningful features suitable for Machine Learning.

### Transformations Performed

* Extracted numerical values from **RAM**
* Converted **Weight** into a numerical value
* Simplified **Operating System** categories
* Created binary `TouchScreen` feature
* Created binary `IPS` feature
* Engineered **PPI (Pixels Per Inch)** from screen resolution and screen size
* Extracted **CPU Brand**
* Separated storage into **HDD** and **SSD** capacities
* Extracted **GPU Brand**
* Removed unnecessary information from complex text-based specifications

These transformations reduced feature complexity while preserving information that can contribute to laptop price prediction.

---

## 🧠 Machine Learning Pipeline

The complete Machine Learning pipeline will be developed progressively:

```text
Raw Dataset
     ↓
Data Cleaning
     ↓
Exploratory Data Analysis
     ↓
Feature Engineering
     ↓
Feature Encoding
     ↓
Train-Test Split
     ↓
Model Training
     ↓
Model Evaluation
     ↓
Hyperparameter Tuning
     ↓
Final Model
     ↓
Deployment
```

---

## 🚧 Future Work

The project is intentionally being developed in stages. Future improvements will include:

### 1. Data Preprocessing

* Encode categorical variables
* Scale numerical features where required
* Prepare the final feature matrix

### 2. Model Development

Different regression algorithms will be experimented with, such as:

* Linear Regression
* Ridge / Lasso Regression
* Decision Tree Regressor
* Random Forest Regressor
* Gradient Boosting
* XGBoost / other boosting techniques

### 3. Model Evaluation

Models will be compared using appropriate regression metrics, including:

* MAE
* MSE
* RMSE
* R² Score

### 4. Hyperparameter Tuning

The best-performing models will be optimized using techniques such as:

* Grid Search
* Random Search
* Cross-Validation

### 5. Model Selection

The final model will be selected based on its performance on unseen data while considering both accuracy and generalization.

### 6. Deployment

The trained model will eventually be integrated into a user-friendly application where users can enter laptop specifications and receive an estimated price.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **Jupyter Notebook**
* **Git & GitHub**

Additional libraries and tools may be added as the project progresses.

---

## 📁 Project Structure

The structure may evolve as new stages are completed:

```text
Laptop-Price-Prediction/
│
├── dataset/
│   └── laptop_data.csv
│
├── notebooks/
│   ├── EDA.ipynb
│   ├── Feature_Engineering.ipynb
│   └── Model_Training.ipynb
│
├── models/
│   └── ...
│
├── app/
│   └── ...
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## 🎯 Objective

The ultimate objective is to develop a reliable Machine Learning solution capable of estimating laptop prices from their specifications and to demonstrate the complete workflow of a real-world regression project — **from raw data to deployment**.

---

## 📈 Project Progress

* [x] Dataset collection
* [x] Initial data exploration
* [x] Exploratory Data Analysis
* [x] Feature Engineering
* [x] Categorical Encoding
* [ ] Train-Test Split
* [ ] Model Training
* [ ] Model Evaluation
* [ ] Hyperparameter Tuning
* [ ] Final Model Selection
* [ ] Deployment

---

## 👨‍💻 Author

**Hassan Ibrahim**

This project is being developed as part of my Machine Learning learning journey, with the aim of applying ML concepts to practical, end-to-end projects.

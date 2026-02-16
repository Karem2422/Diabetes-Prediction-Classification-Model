# Advanced Multi-Stage Diabetes Prediction: Comparison with Comprehensive Tuning

## 📌 Project Overview
This project presents an in-depth analysis and comparative study of **Multi-class** versus **Binary Classification** for diabetes prediction. Utilizing the CDC Behavioral Risk Factor Surveillance System (BRFSS) 2015 dataset, the study explores various machine learning models across multiple experimental phases to identify the most effective predictive approach.


- **Group Name:** The Avengers
- **Members:** 
  - Abdulkarem Ghassan 
  - Baraa Alaa 
  - Sara Al-Saeedi 

---

## 🛠️ Methodology
The project follows a rigorous three-phase methodology applied to both binary and multi-class tasks:

1.  **Phase 1 (Baseline):** Training and evaluating models using Stratified Cross-Validation on the original scaled dataset.
2.  **Phase 2 (Tuning):** Performing Hyperparameter Optimization via `GridSearchCV` for all models to maximize performance.
3.  **Phase 3 (SMOTE):** Implementing Synthetic Minority Over-sampling Technique (SMOTE) to address class imbalance and retraining the tuned models.

---

## 📊 Dataset
The dataset used is `diabetes_012_health_indicators_BRFSS2015.csv`, which contains 253,680 responses with 21 health indicators (features) and a target variable:
- **0:** No diabetes
- **1:** Prediabetes
- **2:** Diabetes

For binary classification, classes 1 and 2 are merged into a single "Diabetes/Prediabetes" category.

---

## 🤖 Models Implemented
The following algorithms were compared:
- **Logistic Regression**
- **Random Forest Classifier**
- **XGBoost Classifier**
- **Gradient Boosting Classifier**
- **Decision Tree Classifier**
- **Gaussian Naive Bayes**
- **K-Nearest Neighbors (KNN)**

---

## 📈 Key Results
The study evaluated models based on Accuracy, Precision, Recall, F1-Score, and ROC-AUC.

### Best Performances:
| Task | Best Model | Phase | F1-Score | Recall | ROC-AUC |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Multi-Class** | Gradient Boosting | SMOTE | 0.8224 | 0.8373 | 0.8124 |
| **Binary** | Logistic Regression | SMOTE | 0.4702 | 0.7578 | 0.8165 |

---

## 🚀 How to Run
1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    ```
2.  **Install dependencies:**
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn xgboost
    ```
3.  **Ensure the dataset is present:** Place `diabetes_012_health_indicators_BRFSS2015.csv` in the project root.
4.  **Run the Notebook:** Open `ML Project.ipynb` in Jupyter or VS Code and run all cells.

---

## 📂 Project Structure
- `ML Project.ipynb`: Core implementation, EDA, and evaluation.
- `ML Project .pptx`: Presentation of results and methodology.
- `diabetes_012_health_indicators_BRFSS2015.csv`: Raw dataset file.

---

## 💡 Visualizations
The project includes several diagnostic plots:
- **Correlation Heatmaps** for feature dependency analysis.
- **Confusion Matrices** for each model and phase.
- **ROC Curves** (including One-Vs-Rest for multi-class).
- **Comparison Bar Charts** for performance metrics across phases.

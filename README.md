# Census Income Classification

This project applies machine learning to predict whether a person earns more than \$50K per year based on demographic and employment features from the 1994 U.S. Census dataset. It was completed as part of a Machine Learning lab that followed the end-to-end ML lifecycle — from data exploration and preprocessing to model evaluation and hyperparameter tuning.

---

## 📁 Project Structure

---

## 🎯 Objective

The goal of this project is to build and evaluate models that predict **income level (≤50K or >50K)** based on demographic and work-related attributes such as age, education, occupation, hours worked per week, and capital gains/losses.

---

## 🧩 Dataset

- **Name:** Census Income Dataset (1994 U.S. Census)
- **File:** `censusData.csv`
- **Rows:** ~32,000 individuals  
- **Features:** 14 attributes including:
  - Age
  - Workclass
  - Education
  - Marital status
  - Occupation
  - Relationship
  - Race
  - Sex
  - Hours per week
  - Capital gain/loss
  - Native country  
- **Target variable:** `income_binary` — whether income is `>50K` or `<=50K`.

---

## 🔍 Exploratory Data Analysis (EDA)

Key steps:
- Handled missing values using mean imputation for numeric features.
- Applied **Winsorization** to cap extreme outliers in capital gains/losses.
- **One-hot encoded** categorical features.
- Examined **class imbalance** (approximately 76% ≤50K vs 24% >50K).
- Visualized relationships between features and income (e.g., hours worked vs. income).

---

## ⚙️ Modeling Approach

Two supervised learning models were trained and compared:
1. **Logistic Regression** — interpretable linear model.
2. **Random Forest Classifier** — ensemble model capable of capturing nonlinear relationships.

Both models were trained using:
- **Stratified train-test split** (80/20)
- **StandardScaler** normalization for numeric features
- **Class weights** to address class imbalance

---

## 🧪 Results

| Model                | Cross-Validation AUC | Test AUC | Notes |
|----------------------|----------------------|----------|-------|
| Logistic Regression  | 0.906 | **0.909** | Tuned `C=0.01`, `solver='liblinear'` |
| Random Forest        | 0.908 | **0.913** | Tuned `n_estimators=200`, `min_samples_split=5` |

Both models performed well, with Random Forest slightly outperforming Logistic Regression. The AUC > 0.90 indicates strong predictive capability in distinguishing income categories.

---

## 🧰 Technologies Used

- **Python**
- **Pandas**, **NumPy**, **Matplotlib**, **Seaborn** for EDA
- **Scikit-learn** for preprocessing, modeling, and evaluation
- **Jupyter Notebook** for analysis and visualization

---

## 📈 Key Takeaways

- Logistic Regression and Random Forest models both achieved **AUC > 0.9**, showing strong generalization performance.
- Feature scaling, one-hot encoding, and hyperparameter tuning were essential for model improvement.
- The project demonstrates a full ML workflow: data wrangling, EDA, feature engineering, modeling, and evaluation.

---

## 🧑‍💻 Author

**Priya Sinha**  
Machine Learning & AI Enthusiast  
📍 New York, NY  
🔗 [LinkedIn](https://www.linkedin.com/in/priya-sinha45) | [GitHub](https://github.com/prisinha45)

---

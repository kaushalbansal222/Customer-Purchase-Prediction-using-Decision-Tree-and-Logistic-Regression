# Customer Purchase Prediction using Decision Tree & Logistic Regression

This project demonstrates a **basic Machine Learning pipeline** using Scikit-learn to predict whether a customer will make a purchase based on demographic and behavioral features.

---

## Dataset

A synthetic dataset of **5,000 customers** with the following features:

* `Age`
* `Income`
* `Spending_Score`
* **Target:** `Purchased` (0 = Not Purchased, 1 = Purchased)

---

## Models Trained

1. **Logistic Regression**

   * Accuracy: \~57.9%
   * Failed to detect buyers due to **class imbalance**.

2. **Decision Tree Classifier**

   * Significantly improved accuracy.
   * Provided **interpretable rules** for customer classification.

---

## Decision Tree Visualization

The decision tree shows how features are used to classify customers:

* **Root Split:** Income (most influential factor).
* **Further Splits:** Spending Score and Age refine predictions.
* **Interpretability:** Example rule:

  * *If Income <= -1.025 AND Spend\_Score <= -1.592 AND Age <= 0.322 → Prediction = Purchased.*

### How to Read the Tree

* **Root Node:** First split based on Income.
* **Decision Paths:** Branches represent conditions (e.g., `Income <= 1.734`).
* **Leaf Nodes:** Show the final prediction and class distribution.
* **Node Info:** Gini index, sample count, value distribution, predicted class.

### Insights

* Income is the strongest predictor.
* Spending Score & Age refine predictions deeper in the tree.
* Some nodes are perfectly pure (`gini = 0.0`).
* Helps explain why the model predicts a certain outcome.

---

## Model Explainability

Decision Trees are highly interpretable, mirroring human decision-making.

* Businesses can see **which factors drive purchases**.
* Clear rules help stakeholders trust and act on predictions.
* Demonstrates the trade-off between **linear models (Logistic Regression)** vs. **tree-based models (Decision Tree)**.

---

## Tech Stack

* **Python** (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)
* **Jupyter Notebook / Google Colab**

---

## 📈 Future Improvements

* Handle **class imbalance** (SMOTE, resampling).
* Try **ensemble methods** (Random Forest, XGBoost).
* Deploy model with **Streamlit/Flask** for interactive predictions.

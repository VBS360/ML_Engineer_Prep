# 📅 Day 14 – Imbalanced Data, Encoding & Cross Validation

## 🎯 Objective

To strengthen practical machine learning concepts by working on real problems like class imbalance, encoding strategies, and model evaluation using cross-validation.

---

# 🔴 1. Class Imbalance

## 📌 Concept

Class imbalance occurs when the target variable is not equally distributed.

Example:

* No → 73%
* Yes → 27%

## ❌ Problem

Accuracy becomes misleading because the model may predict only the majority class.

## ✅ Solution Metrics

* Precision
* Recall
* F1-score (most important)

---

# 💻 Implementation

## 🔹 Baseline Model

```python
model = LogisticRegression(max_iter=1000)
model.fit(X_train, y_train)
```

### 📊 Result (Churn Class - Yes)

* Precision: 0.70
* Recall: 0.60
* F1-score: 0.64

---

## 🔹 Using class_weight

```python
model = LogisticRegression(class_weight='balanced', max_iter=1000)
```

### 📊 Result

* Precision: 0.55 ↓
* Recall: 0.79 ↑🔥
* F1-score: 0.65

### 📌 Insight

Improved recall at the cost of precision. Suitable for churn problems where identifying potential churn customers is more important.

---

## 🔹 Using SMOTE

```python
from imblearn.over_sampling import SMOTE

sm = SMOTE(random_state=42)
X_res, y_res = sm.fit_resample(X_train, y_train)
```

### 📊 Result

* Precision: 0.64
* Recall: 0.65
* F1-score: 0.64

### 📌 Insight

Balanced performance but less aggressive than class_weight.

---

# 🧠 Key Learning

* Recall is more important in churn prediction
* Trade-off between precision and recall is expected
* Model choice depends on business requirement

---

# 🔵 2. Cross Validation

## 📌 Concept

Cross-validation evaluates model performance across multiple splits instead of a single train-test split.

## 💻 Implementation

```python
from sklearn.model_selection import cross_val_score
from sklearn.metrics import make_scorer, f1_score

f1 = make_scorer(f1_score, pos_label='Yes')

scores = cross_val_score(
    LogisticRegression(class_weight='balanced', max_iter=1000),
    X, y,
    cv=5,
    scoring=f1
)
```

### 📊 Result

* Average F1 Score: ~0.63

## 📌 Insight

Provides more reliable and stable model performance.

---

# 🟡 3. Encoding Techniques

## 🔹 One-Hot Encoding

* Converts categorical values into binary columns
* Does not cause data leakage
* May cause column mismatch → solved using alignment

---

## 🔹 Target Encoding

### 📌 Concept

Replace category with mean of target variable

Example:

* Gujarat → 0.33
* Maharashtra → 0.66

### ⚠️ Important

* Apply only on training data
* Avoid data leakage

---

## 🔹 Frequency Encoding

Replace category with frequency count.

---

## 🔹 Label Encoding

Assign numeric values (useful for tree-based models)

---

# 🧠 Key Learning

* Encoding is not just get_dummies
* Choose method based on:

  * Model
  * Data size
  * Business need

---

# 🚨 4. Data Leakage

## ❌ Wrong

Applying target encoding before train-test split

## ✅ Correct

Apply encoding after split using only training data

---

# 🧠 Golden Rule

> Any technique using target variable must be applied after train-test split.

---

# 🔥 5. Important Concepts Learned

* Row vs Column importance (alignment based on rows)
* Feature space consistency
* Trade-offs in ML decisions
* Business-driven evaluation

---

# 🚀 Summary

* Implemented imbalance handling techniques
* Compared multiple models
* Applied cross-validation
* Understood encoding deeply
* Learned to avoid data leakage

---

**Status:** ✅ Completed Day 14

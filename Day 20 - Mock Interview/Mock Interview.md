# 🧠 AI/ML Interview Preparation – Core Questions & Answers

This repository contains my preparation notes for AI/ML interviews, covering Python, Machine Learning, and Generative AI concepts.

---

# 👤 1. Tell Me About Yourself

Hello, my name is Vatsal Shah. I have around 4 years of experience starting from QA engineering and prompt engineering, and recently I have transitioned into Machine Learning and AI roles.

Currently, I am working on my startup, WellMitra, where I have built an AI-based health management system. One of the key features I developed is a health report analyzer that allows users to understand their reports and get insights. Through this, I have gained hands-on experience in solving real-world problems using machine learning.

Before this, I worked as a prompt engineer at Soul AI, where I worked with large language models like GPT-4 and Gemini, focusing on prompt optimization and improving model responses. Earlier, I worked as a QA engineer and technical coordinator, where I also handled team responsibilities.

Now, I am looking for an opportunity where I can apply my Machine Learning and AI skills in a professional environment and continue growing in this domain.

---

# 🐍 2. Python

## Difference Between List and Tuple

| Feature     | List    | Tuple     |
| ----------- | ------- | --------- |
| Mutability  | Mutable | Immutable |
| Performance | Slower  | Faster    |
| Syntax      | []      | ()        |

* Lists can be modified (add/remove elements)
* Tuples cannot be changed after creation
* Both support indexing and iteration

---

# 🤖 3. Machine Learning

## What is Overfitting?

Overfitting occurs when a model learns the training data too well, including noise and patterns, but performs poorly on unseen data.

### Causes:

* Complex model
* Small dataset
* Too many features

### Prevention:

* Cross-validation
* Regularization (L1/L2)
* Simpler models
* More data

---

## What is Regularization?

Regularization helps prevent overfitting by adding a penalty to large model coefficients.

### Types:

* L1 (Lasso): Can reduce features to zero
* L2 (Ridge): Reduces coefficient values

---

## Evaluation Metrics

### Accuracy

* Works well for balanced datasets

### Precision

* Focuses on false positives

### Recall

* Focuses on false negatives

### F1 Score

* Balance of precision and recall
* Best for imbalanced datasets

---

## Handling Missing Data

Steps:

1. Identify data type (categorical / numerical)
2. Apply:

   * Mean → if no outliers
   * Median → if outliers present
   * Mode → for categorical data
3. Drop column if too many missing values (>80–90%)
4. Use domain knowledge when needed

---

## Model Evaluation Process

### Classification:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC
* Cross-validation

### Regression:

* MAE (Mean Absolute Error)
* MSE (Mean Squared Error)
* RMSE
* R² Score

---

# 🚀 4. Model Deployment (Basic Understanding)

Steps:

1. Train model
2. Save model (pickle/joblib)
3. Create API using Flask/FastAPI
4. Deploy on server/cloud

### Important Factors:

* Scalability
* Monitoring
* Retraining (model drift)

---

# 🧠 5. Generative AI

## What is Prompt Engineering?

Prompt engineering is the process of designing inputs to guide LLM outputs effectively.

### Importance:

* Controls model behavior
* Improves response quality
* Reduces ambiguity

---

## What is RAG (Retrieval-Augmented Generation)?

RAG combines:

* LLM (generation)
* External data source (retrieval)

### How it works:

1. User asks question
2. System retrieves relevant documents
3. LLM generates answer using retrieved data

### Benefits:

* More accurate
* Up-to-date responses
* Reduces hallucination

---

## What is a Vector Database?

A vector database stores data as embeddings (numerical vectors).

### Use Case:

* Semantic search
* RAG systems

### Examples:

* Pinecone
* FAISS
* Weaviate

---

# 🔍 6. Model Monitoring (Basic Idea)

After deployment:

* Track accuracy over time
* Detect data drift
* Retrain model if performance drops

---

# 🎯 Final Note

This preparation focuses on:

* Clear concepts
* Real-world understanding
* Interview-ready explanations

---

⭐ Consistency and clarity are key to cracking AI/ML interviews.

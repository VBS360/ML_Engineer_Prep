# 🤖 Generative AI Interview – Spoken Answers (High Priority)

This document contains important Generative AI interview questions with **clear, spoken-style answers** for real interview use.

---

## ❓ 1. What is a Large Language Model (LLM) and how does it work?

A Large Language Model is a deep learning model trained on a large amount of text data to understand and generate human-like language.

At a high level, it works by predicting the next word in a sequence based on context. It learns patterns, grammar, and relationships from the training data and uses that knowledge to generate responses.

---

## ❓ 2. What is the difference between fine-tuning and prompt engineering?

Fine-tuning involves training a pre-trained model further on a specific dataset to make it more specialized.

Prompt engineering, on the other hand, focuses on designing better input prompts to guide the model’s output without changing the model itself.

---

## ❓ 3. What is RAG and why is it better than using an LLM alone?

RAG stands for Retrieval-Augmented Generation.

It combines an LLM with an external data source. When a user asks a question, the system first retrieves relevant information and then uses the LLM to generate a response.

It is better than a standalone LLM because it provides more accurate and up-to-date information and reduces hallucination.

---

## ❓ 4. What are embeddings and why are they important?

Embeddings are numerical representations of text in vector form.

They help capture the meaning of text so that similar words or sentences are closer in vector space.

They are important for tasks like semantic search, similarity matching, and RAG systems.

---

## ❓ 5. How would you design a chatbot that answers questions based on company documents?

I would first convert the documents into embeddings and store them in a vector database.

When a user asks a question, I would convert the query into an embedding and retrieve the most relevant documents.

Then I would pass this information to an LLM to generate a final response.

---

## ❓ 6. What is hallucination in LLMs and how can you reduce it?

Hallucination is when the model generates incorrect or made-up information confidently.

It can be reduced by using RAG, improving prompts, and grounding responses with real data.

---

## ❓ 7. What is temperature in LLMs?

Temperature controls the randomness of the output.

A low temperature makes responses more deterministic and focused, while a high temperature makes responses more creative and diverse.

---

## ❓ 8. What is the role of a vector database?

A vector database stores embeddings and allows fast similarity search.

It is used to find relevant information based on meaning rather than exact keywords.

---

## ❓ 9. How do you evaluate a GenAI system?

Evaluation can be done by checking response accuracy, relevance, and consistency.

We can also use human feedback or compare outputs with expected results.

---

## ❓ 10. What are some limitations of LLMs?

Some limitations include hallucination, lack of real-time knowledge, bias in data, and high computational cost.

They also depend heavily on the quality of prompts.

---

# 🚀 Final Tip

In interviews:

* Keep answers simple
* Use real-world examples
* Stay confident even if unsure

---

⭐ Focus on clarity, not complexity

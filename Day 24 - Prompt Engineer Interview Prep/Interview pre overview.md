# 📘 AI Prompt Engineer – Interview Preparation Log

## 🏢 Company: Bosch

## 📅 Session Summary: Interview Preparation & Mock Practice

---

# 🚀 Objective

To prepare for an AI Prompt Engineer role by developing:

* Strong understanding of prompt engineering
* System design thinking using LLMs
* Real-world problem-solving approach
* Confidence through mock interviews

---

# 🧠 Key Problem Discussed

## 📌 Use Case:

Extract invoice numbers from invoices across multiple countries with varying formats.

### Challenges:

* Different invoice formats per vendor/country
* Different labels (Invoice No, ID, Ref, etc.)
* Numerical vs alphanumeric formats
* No fixed structure
* High manual effort currently

---

# 🏗️ Proposed Solution: Hybrid System

## 🔹 Architecture Overview:

1. **Data Extraction Layer**

   * OCR / PDF parsing
   * Convert invoice → text

2. **Rule-Based Layer**

   * Regex / pattern matching
   * Handles known formats
   * Fast and low-cost

3. **LLM Layer**

   * Handles unstructured / unknown formats
   * Prompt-based extraction
   * Returns structured output (JSON)

4. **Manual Review Layer**

   * For low-confidence cases
   * Human validation

---

## 🔄 Flow:

Input → OCR → Rule-based → (Fail) → LLM → (Low confidence) → Manual Review → Store Result

---

# 🎯 Key Concepts Learned

## 🔹 Prompt Engineering Structure

* Role
* Task
* Context
* Constraints
* Output format

---

## 🔹 Improving Prompt Accuracy

* Add clear instructions
* Define what NOT to extract
* Include examples
* Use structured output (JSON)
* Iterate based on failures

---

## 🔹 Handling Hallucination

* Add constraints
* Use validation rules
* Use confidence scoring
* Manual fallback

---

## 🔹 Evaluation Metrics

* Field-level accuracy (correct invoice number)
* Automation rate (manual reduction %)
* Cost per invoice
* Consistency over time

---

## 🔹 Cost Optimization

* Hybrid approach (rules + LLM)
* Reduce input size
* Use LLM selectively
* Use local models (Ollama, Llama)
* Batch processing

---

## 🔹 Performance Optimization

* Parallel processing
* Reduce unnecessary processing
* Cache repeated vendor formats
* Optimize pipelines

---

# 🧠 Snowflake Integration

## 📌 Understanding:

* Snowflake = Cloud data warehouse (data storage)

## 📌 Role in system:

* Input: Store invoice data
* Processing: External Python pipeline
* Output: Store extracted invoice numbers

---

# 💬 Interview Q&A Practice

## 🔹 Core Questions Practiced:

1. Design invoice extraction system
2. Handling incorrect outputs
3. Cost optimization
4. Performance scaling
5. Measuring success
6. Improving reliability
7. Rule-based vs LLM
8. Real project experience

---

## 🔹 Key Answer Strategy:

* Structure answers (Step 1, 2, 3)
* Keep answers concise
* Focus on business impact
* Show trade-offs
* Use real examples

---

# 🧪 Mock Interview Highlights

## Strengths:

* Strong system thinking
* Good understanding of hybrid models
* Real-world problem-solving
* Clear improvement mindset

## Improvements:

* Keep answers concise
* Avoid repetition
* Speak in structured format
* Pause before answering

---

# 🏆 Real Project Example (WellMitra)

## Problem:

* Incorrect helpline numbers (US instead of India)

## Solution:

* Added constraints in prompt
* Restricted country codes
* Added examples

## Result:

* Reduced hallucination
* Improved relevance
* Better user experience

---

# 💰 Salary Discussion Strategy

* Current: 7.2 LPA
* Offered expectation: 9 LPA
* Justification:

  * Domain transition
  * Gap consideration
  * Entry into AI field

## Insight:

* Role value > immediate salary
* Focus on long-term growth

---

# 🚀 Final Outcome

* Cleared technical round ✅
* Cleared manager round ✅
* HR initiated document process ✅

---

# 🔥 Key Takeaways

* Prompt engineering = system thinking
* LLMs should be used selectively
* Hybrid systems are practical and scalable
* Real-world reliability > theoretical perfection
* Communication and structure are critical in interviews

---

# 🎯 Next Steps

* Join role successfully
* Build strong AI/ML foundation
* Convert work into ML experience
* Target higher salary roles in 6–12 months

---

# 💡 Final Note

> “Focus on trajectory, not immediate salary.”

---
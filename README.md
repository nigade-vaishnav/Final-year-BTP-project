# Final-year-BTP-project
In-Context Learning Assisted Prompt Optimization in LLMs for Classification Tasks
# 🧠 Fake News Detection using Feature-Driven Optimization & LLMs (FDOF)

## 📌 Overview

This project presents a **hybrid AI system** for detecting fake news by combining:

* Classical Machine Learning
* Evolutionary Feature Selection
* Large Language Models (LLMs)

The system is designed as a **two-stage pipeline**:

1. **Feature-Driven Evolutionary Learning (FEL)**
2. **Feature-Informed LLM Classification**

This approach improves both:

* ✅ Accuracy
* ✅ Interpretability
* ✅ Robustness against noisy data

---

## 🚀 Key Features

* 🔍 **220-dimensional feature extraction**

  * 200 TF-IDF features
  * 20 engineered linguistic & psychological features

* 🧬 **Genetic Algorithm (GA) based Feature Selection**

  * Selects optimal subset of features
  * Reduces noise and improves performance

* ⚙️ **Hybrid Outlier Detection**

  * Mahalanobis Distance
  * KNN-based anomaly detection

* 🤖 **Feature-Informed LLM Classification**

  * Uses structured prompts with indicators
  * Retrieval-Augmented In-Context Learning (ICL)

* 🧠 **QLoRA Fine-Tuning**

  * Efficient LLM adaptation using 4-bit quantization
  * Low memory, high performance

---

## 🏗️ System Architecture

### 🔹 Stage 1: Feature-Driven Evolutionary Learning (FEL)

* Feature Extraction (TF-IDF + Engineered)
* Outlier Removal (MD + KNN)
* Genetic Algorithm for Feature Selection
* Baseline Model Training (SVM, Random Forest, XGBoost)

### 🔹 Stage 2: LLM-Based Classification

* Retrieval of similar examples (k-shot)
* Feature-informed prompt construction
* QLoRA fine-tuning of LLM
* Constrained classification output (0 = Real, 1 = Fake)

---

## 📊 Models Used

### Classical Models

* Linear SVM
* Random Forest
* XGBoost

### LLM Models

* Fine-tuned causal language model (e.g., Tiny-GPT2 / Phi-2)
* Retrieval-Augmented In-Context Learning

---

## 📈 Results

| Model                   | Accuracy   | F1 Score |
| ----------------------- | ---------- | -------- |
| XGBoost                 | **0.8411** | 0.8324   |
| LLM (QLoRA + Dense ICL) | 0.8325     | 0.8127   |
| Random Forest           | 0.8285     | 0.8041   |
| SVM                     | 0.8148     | 0.7954   |

### 🔍 Insights

* XGBoost achieved the highest accuracy
* LLM approach performed competitively (~1% difference)
* Dense retrieval significantly improved LLM performance
* Feature selection enhanced classical models

---

## 🧪 Experimental Setup

* Python 3.10
* PyTorch, HuggingFace Transformers
* Scikit-learn, XGBoost
* BitsAndBytes (4-bit quantization)
* PEFT (QLoRA)

---

## 📂 Project Structure

```id="3j5rta"
├── data/
├── src/
│   ├── preprocessing/
│   ├── feature_engineering/
│   ├── feature_selection/
│   ├── models/
│   ├── llm_pipeline/
│   └── evaluation/
├── configs/
├── scripts/
│   └── run_pipeline.py
├── outputs/
└── README.md
```

---

## ⚙️ How It Works

1. Load and preprocess dataset
2. Extract 220-dimensional features
3. Remove outliers using MD + KNN
4. Apply Genetic Algorithm for feature selection
5. Train classical models (SVM, RF, XGBoost)
6. Retrieve similar examples for LLM
7. Generate feature-informed prompts
8. Fine-tune LLM using QLoRA
9. Perform classification

---

## 🎯 Key Contributions

* Hybrid pipeline combining **ML + Evolutionary Algorithms + LLMs**
* Feature-informed prompting for improved LLM reasoning
* Efficient LLM training using QLoRA
* Robust handling of noisy and imbalanced data

---

## 🔮 Future Work

* Real-time fake news detection system
* Integration with social media APIs
* Multilingual fake news detection
* Deployment as SaaS platform

---

## 👨‍💻 Author

**Vaishnav Nigade**
B.Tech CSE (AI & Data Science)

---

## ⭐ Acknowledgements

* HuggingFace Transformers
* Scikit-learn
* Open-source NLP community

---

## 📌 Note

This project was developed as part of a **Final Year B.Tech Project (BTP)** and demonstrates advanced concepts in:

* Machine Learning
* Natural Language Processing
* Large Language Models
* Optimization Algorithms

---

⭐ If you like this project, consider giving it a star!


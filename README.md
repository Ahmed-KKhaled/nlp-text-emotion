# nlp-text-emotion
This project compares three different approaches for emotion detection in text: Traditional Machine Learning, LSTM, and BERT. The goal is to classify text into five emotions (joy, sadness, fear, anger, neutral) and evaluate the performance of each model to determine the most effective approach.

# Emotion Detection: ML vs LSTM vs BERT

A comparison between three different approaches for emotion detection in text, classifying into five emotions: **joy, sadness, fear, anger, and neutral**.

---

## 📌 Problem Statement
Understanding human emotions from text is a challenging NLP task. Unlike simple sentiment analysis (positive/negative), emotion detection requires the model to distinguish between fine-grained emotional states. The challenge lies in the fact that different emotions can be expressed in very similar ways, and the same sentence can carry different emotions depending on context.

For example:
- *"I can't believe this happened"* → could be **joy** or **anger**
- *"I'm done"* → could be **sadness** or **anger**

This project explores how different model architectures handle this complexity.

---
📂 Dataset

🔗 Dataset Link: (https://github.com/Ahmed-KKhaled/nlp-text-emotion/tree/main/Text_Emotion_project/data)
Number of classes: 5 (joy, sadness, fear, anger, neutral)

## 🧪 Approach
Three different approaches were implemented and compared:

**1. Traditional Machine Learning**
Uses hand-crafted features (TF-IDF) with classic classifiers. Fast and simple, but struggles to capture context and word order.

**2. LSTM**
A deep learning model that processes text sequentially and captures some context. Better than traditional ML, but still limited in understanding long-range dependencies.

**3. BERT**
A transformer-based model pre-trained on massive amounts of text. Understands context from both directions (left and right) and leverages transfer learning, which gives it a significant advantage over the other approaches.

---

## 📊 Results

### Traditional Machine Learning
| Model | F1 Score |
|-------|----------|
| Naive Bayes | 64% |
| Logistic Regression | 68.9% |
| Linear SVC | 70% |

### LSTM
| Model | F1 Score |
|-------|----------|
| LSTM | 70% |

### BERT
| Model | F1 Score |
|-------|----------|
| BERT | **82.4%** ✅ |

---

## 🔍 Why BERT is Better?
- **Pre-trained on massive data:** BERT was trained on billions of words, so it already understands language deeply before fine-tuning.
- **Bidirectional context:** Unlike LSTM which reads text left-to-right, BERT looks at the full sentence at once, giving it better understanding of context.
- **Transfer Learning:** Instead of training from scratch, BERT adapts its existing knowledge to the emotion detection task, which is a huge advantage especially with limited data.
- **Handles ambiguity better:** Because of its deep contextual understanding, BERT can distinguish between emotions that are expressed similarly.

---

## 🛠️ Models Used
- Naive Bayes
- Logistic Regression
- Linear SVC
- LSTM (PyTorch)
- BERT `bert-base-uncased` (HuggingFace Transformers)

# Fine-Tuning Transformer for Question Answering

## 1. Introduction
This report presents the development and evaluation of a
**Transformer-based Question Answering (QA) system**
fine-tuned using a **Seq2Seq approach**.
The goal is to accurately generate short textual answers
given a question and its supporting context.

---

## 2. Experimental Setup

### 2.1 Environment
- **PyTorch**: 2.9.0
- **CUDA**: Enabled
- **Device**: GPU (CUDA)
- **Trainer**: Hugging Face `Seq2SeqTrainer`

### 2.2 Dataset
- Training set: **5,000 samples**
- Validation set: **1,000 samples**
- Evaluation set: **500 samples**

Each sample consists of:
- Context paragraph
- Question
- One or more reference answers

---

## 3. Training Configuration
- **Epochs**: 2
- **Total steps**: 2,500
- **Final training loss**: 0.1019
- **Training runtime**: ~1,415 seconds

### Training Loss Trend
Training loss dropped sharply during early steps
and stabilized toward the end,
indicating successful convergence.

---

## 4. Evaluation Results

### 4.1 Quantitative Metrics

| Metric | Score |
|------|------|
| Exact Match (EM) | 85.40% |
| F1 Score | 89.02% |

- **Exact Match (EM)** measures strict string equality
- **F1 Score** captures partial overlap between predicted and gold answers

---

## 5. Qualitative Analysis

### 5.1 Correct Predictions
The model accurately answers:
- Factual questions
- Entity-based queries
- Short descriptive questions

Example:

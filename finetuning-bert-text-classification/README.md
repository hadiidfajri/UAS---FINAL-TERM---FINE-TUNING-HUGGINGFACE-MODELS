# Natural Language Inference (NLI) with BERT on MNLI (GLUE)

This repository implements an **end-to-end Transformer encoder-based**
**Natural Language Inference (NLI)** system using a **BERT-family model**
fine-tuned on the **Multi-Genre Natural Language Inference (MNLI)**
dataset from the **GLUE benchmark**.

The project covers dataset exploration, preprocessing,
model training, and evaluation on both **matched** and **mismatched**
validation sets.

---

## 🎯 Task Description
Given a **premise** and a **hypothesis**, the model predicts one of three labels:

- **Entailment** – the hypothesis logically follows from the premise
- **Neutral** – the hypothesis is neither entailed nor contradicted
- **Contradiction** – the hypothesis contradicts the premise

---

## 📊 Dataset
- **Name**: MNLI (Multi-Genre Natural Language Inference)
- **Source**: GLUE Benchmark
- **Total Training Samples**: 392,702
- **Validation (Matched)**: 9,815
- **Validation (Mismatched)**: 9,832
- **Test (Matched)**: 9,796
- **Test (Mismatched)**: 9,847

### Dataset Features
- `premise` (string)
- `hypothesis` (string)
- `label` (entailment, neutral, contradiction)

---

## 🧠 Model Architecture
- **Model Type**: Encoder-only Transformer
- **Base Model**: BERT (e.g. `bert-base-uncased`)
- **Task Head**: Sequence Classification
- **Number of Labels**: 3

---

## ⚙️ Environment & Setup

### Hardware
- **Device**: GPU (CUDA)
- **GPU**: Tesla T4

### Software
- **PyTorch**
- **Hugging Face Transformers**
- **Hugging Face Datasets**
- **Scikit-learn**

---

## 📦 Installation

```bash
pip install transformers datasets evaluate accelerate


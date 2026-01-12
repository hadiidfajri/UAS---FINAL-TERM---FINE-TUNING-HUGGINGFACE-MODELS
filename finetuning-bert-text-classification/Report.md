# Natural Language Inference (NLI) with BERT on MNLI (GLUE)

---

## 📌 Project Overview
Proyek ini mengimplementasikan **end-to-end Transformer encoder-based**
**Natural Language Inference (NLI)** menggunakan **BERT-family model**
yang di-*fine-tune* pada dataset **MNLI (Multi-Genre Natural Language Inference)**
dari **GLUE benchmark**.

Tujuan utama adalah mengevaluasi kemampuan model dalam memahami
hubungan logis antara **premise** dan **hypothesis** pada berbagai domain.

---

## 🎯 Task Definition
Diberikan sepasang kalimat:
- **Premise**
- **Hypothesis**

Model memprediksi salah satu label berikut:
- **Entailment** → hypothesis mengikuti premise
- **Neutral** → tidak ada hubungan logis langsung
- **Contradiction** → hypothesis bertentangan dengan premise

---

## 📊 Dataset Description

### Dataset Information
- **Name**: MNLI (GLUE Benchmark)
- **Task Type**: Sentence-pair classification
- **Number of Labels**: 3

### Dataset Splits
| Split | Number of Samples |
|-----|------------------|
| Train | 392,702 |
| Validation (Matched) | 9,815 |
| Validation (Mismatched) | 9,832 |
| Test (Matched) | 9,796 |
| Test (Mismatched) | 9,847 |

### Dataset Features
- `premise` (string)
- `hypothesis` (string)
- `label` (class label)
- `idx` (index)

### Label Mapping

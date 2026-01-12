# Transformer-Based NLP Models: Encoder, Seq2Seq, and LLM

---

## 📌 Project Overview
Repository ini berisi **tiga proyek end-to-end NLP** yang mengimplementasikan
tiga paradigma utama dalam arsitektur Transformer:

1. **Encoder-only Models** (BERT family)
2. **Sequence-to-Sequence Models** (T5)
3. **Large Language Models (Decoder-only)** (Phi-2)

Tujuan utama proyek ini adalah untuk memberikan pemahaman praktis
tentang bagaimana setiap paradigma Transformer digunakan
untuk jenis tugas NLP yang berbeda.

---

## 🧠 Model Paradigms Overview

| Paradigm | Model | Task | Dataset |
|--------|------|------|--------|
| Encoder-only | BERT | Natural Language Inference | MNLI (GLUE) |
| Seq2Seq | T5 | Abstractive Text Summarization | XSum |
| Decoder-only (LLM) | Phi-2 | Lightweight Abstractive Summarization | XSum |

---

## 1️⃣ Encoder-Only Transformer  
### Natural Language Inference using BERT

### Task Description
Model menerima **sepasang kalimat**:
- Premise
- Hypothesis

dan memprediksi hubungan logis:
- **Entailment**
- **Neutral**
- **Contradiction**

### Model Details
- Architecture: Encoder-only Transformer
- Base Model: `bert-base-uncased`
- Task Head: Sequence Classification
- Loss: Cross-Entropy Loss

### Dataset
- **MNLI (Multi-Genre Natural Language Inference)** – GLUE Benchmark
- Total training samples: **392,702**

### Evaluation Results
| Validation Set | Accuracy |
|--------------|----------|
| Matched | 84.90% |
| Mismatched | 84.77% |

✔️ Model menunjukkan **generalization capability** yang baik
dengan accuracy drop hanya **0.13%**.

---

## 2️⃣ Sequence-to-Sequence Transformer  
### Text Summarization using T5

### Task Description
Model menerima **dokumen panjang**
dan menghasilkan **ringkasan abstraktif**.

### Model Details
- Architecture: Encoder–Decoder Transformer
- Base Model: `t5-small`
- Task Type: Abstractive Summarization
- Loss: Cross-Entropy (Teacher Forcing)

### Dataset
- **XSum (Extreme Summarization)**
- Artikel berita BBC dan ringkasan satu kalimat

### Training Characteristics
- Input: Artikel
- Target: Ringkasan
- Prefix instruction: `summarize:`

### Evaluation
- ROUGE-1
- ROUGE-2
- ROUGE-L

✔️ T5 efektif untuk sequence generation terkontrol
dan cocok untuk summarization terstruktur.

---

## 3️⃣ Decoder-Only Transformer (LLM)  
### Lightweight Summarization using Phi-2

### Task Description
Model **Large Language Model (LLM)** digunakan untuk
**abstractive summarization** dengan pendekatan prompting.

### Model Details
- Architecture: Decoder-only Transformer
- Base Model: `microsoft/phi-2`
- Parameters: ~2.7B
- Fine-tuning Strategy:
  - Dataset subsampling
  - Gradient checkpointing
  - FP16
  - Small batch size

### Dataset
- **XSum**
- Subset untuk efisiensi komputasi

### Hardware Constraints
- GPU ≤ 8GB VRAM
- Feasible on Google Colab / consumer GPU

✔️ Phi-2 mampu menghasilkan ringkasan yang koheren
meskipun dengan resource terbatas.

---

## 📁 Repository Structure



# Transformer-Based Question Answering (Fine-Tuning)

This repository contains an **end-to-end Transformer-based Question Answering (QA) system**
fine-tuned using a **Seq2Seq architecture** on a subset of a QA dataset
(similar to SQuAD-style extractive QA).

The project demonstrates training, evaluation, error analysis,
and decoding ablation under a **GPU-accelerated PyTorch environment**.

---

## 🚀 Features
- Transformer-based Seq2Seq QA model
- Fine-tuning with PyTorch & Hugging Face Transformers
- Exact Match (EM) & F1 evaluation
- Error analysis (worst predictions)
- Ablation study on decoding strategy (`num_beams`)
- Custom inference demo

---

## ⚙️ Environment
- **Framework**: PyTorch 2.9.0
- **CUDA**: Enabled
- **Device**: GPU (CUDA)
- **Trainer**: `Seq2SeqTrainer`
- **Tracking**: Weights & Biases (offline mode)

---

## 📊 Dataset
- **Training samples**: 5,000
- **Validation samples**: 1,000
- **Evaluation samples**: 500
- **Fields**:
  - `context`
  - `question`
  - `answers`

Example:

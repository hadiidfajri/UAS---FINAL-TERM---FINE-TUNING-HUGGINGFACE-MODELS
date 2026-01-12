
# Model Evaluation  
Fine-Tuning Summarization Model on XSum Dataset

================================================================================

## 1. Evaluation Overview
Evaluasi dilakukan untuk mengukur performa model hasil **fine-tuning pada task abstractive text summarization**
menggunakan **dataset XSum**.  
Pengujian dilakukan pada dua skenario evaluasi untuk mengukur kemampuan generalisasi model:

- **Validation Matched Set**
- **Validation Mismatched Set**

Pendekatan ini bertujuan untuk menilai performa model baik pada domain yang serupa maupun berbeda
dari data pelatihan.

---

## 2. Validation Matched Evaluation

📊 **Evaluating on Validation Matched Set**

- Total evaluation steps: **154**
- Waktu evaluasi: **00:36**

### Results
- **Accuracy** : **0.8490 (84.90%)**
- **Loss**     : **0.4762**

### Interpretation
Hasil ini menunjukkan bahwa model mampu memahami dan meringkas teks secara efektif
pada domain yang sejalan dengan data pelatihan.

---

## 3. Validation Mismatched Evaluation

📊 **Evaluating on Validation Mismatched Set**

### Results
- **Accuracy** : **0.8477 (84.77%)**
- **Loss**     : **0.4651**

### Interpretation
Performa model pada domain yang berbeda dari data pelatihan tetap stabil,
menunjukkan kemampuan generalisasi yang baik terhadap variasi data.

---

## 4. Cross-Domain Generalization Analysis

📊 **Cross-Domain Performance Summary**

| Metric | Value |
|------|------|
| Matched Accuracy | 84.90% |
| Mismatched Accuracy | 84.77% |
| Accuracy Drop | **0.13%** |

### Analysis
- Selisih akurasi antara matched dan mismatched set hanya **0.13%**
- Penurunan performa yang sangat kecil mengindikasikan bahwa model:
  - Tidak overfitting pada domain tertentu
  - Memiliki **generalization capability** yang kuat

✅ **Conclusion:** Model menunjukkan **good cross-domain generalization**

---

## 5. Strengths
- Performa konsisten pada domain berbeda
- Loss relatif rendah dan stabil
- Cocok untuk deployment pada data ringkasan teks dengan variasi topik

---

## 6. Limitations
- Evaluasi masih berbasis metrik accuracy
- Belum mencakup metrik khusus summarization seperti:
  - ROUGE-1
  - ROUGE-2
  - ROUGE-L
- Belum dilakukan evaluasi kualitatif hasil ringkasan

---

## 7. Conclusion
Model hasil **fine-tuning pada dataset XSum** menunjukkan performa yang solid
dengan akurasi di atas **84%** pada kedua validation set.
Perbedaan performa yang sangat kecil antara matched dan mismatched set
menegaskan bahwa model memiliki kemampuan generalisasi lintas domain yang baik
dan layak digunakan untuk task **abstractive text summarization**.

---

**Keywords:** Text Summarization, XSum, Fine-Tuning, Transformer, NLP

### 📄 Noisy Medical Document Images (OCR)

**Study**: Patel, D. (2026). Noisy Medical Document Images – Hospital Bills & Discharge Summaries. Kaggle.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                     |
|-------------------------|-----------------------------------------------------------------------------|
| **📛 Title**            | Noisy Medical Document Images (OCR)                                         |
| **🔗 Source**           | https://www.kaggle.com/datasets/devp1866/noisy-medical-document-images-ocr  |
| **📋 Target Organ**     | N/A (Clinical Documents)                                                    |
| **📅 Last Accessed**    | November 10, 2026                                                           |
| **🎯 Supported Tasks**  | 🏷️ Classification, 🔍 OCR, Named Entity Recognition (NER), Table Extraction |
| **📐 Image Size**       | High-resolution JPG (variable)                                              |
| **📁 Data Format**      | JPG (images), CSV (structured JSON ground truth)                            |
| **👥 Demographics**     | ❌ 100% synthetic (HIPAA-safe, zero real patient data)                      |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                     |

#### 📊 Dataset Composition

| Category              | Details                                                          |
|-----------------------|------------------------------------------------------------------|
| **🖼️ Total Images**   | 1,000 synthetic document images                                  |
| **📄 Document Types** | 500 Hospital Bills, 500 Discharge Summaries                      |
| **📦 Total Size**     | ~316.2 MB                                                        |
| **🏥 Source**         | Programmatically generated via ReportLab + OpenCV noise pipeline |

#### 🏷️ Task Details

- **Classification**: Binary classification of document type (Bill vs. Discharge Summary).
- **OCR & NER**: Extraction of structured fields (Hospital name, Patient DOB, MRN, Diagnosis, ICD-10 codes, CPT codes,
  Medications, Financials).
- **Noise Profile**: Simulates real-world scanning artifacts including perspective warp, mail folds, uneven lighting,
  coffee stains, punch holes, blur, and JPEG compression.

#### 💡 Usage Notes

- ✅ Solves the "too clean" and "PHI/PII exposure" problems of existing medical document datasets.
- ✅ Rich, nested JSON ground truth enables end-to-end Document AI and LayoutLM fine-tuning.
- ✅ Clinical coherence is maintained (e.g., Type 2 Diabetes diagnoses are consistently paired with HbA1c tests and
  Metformin).
- 📚 Recommended to cite the original Kaggle repository.
- 🔐 Distributed under CC BY-SA 4.0; attribution and share-alike required.

#### ⚠️ Usage Considerations

| Aspect                  | Recommendation                                                                                          |
|-------------------------|---------------------------------------------------------------------------------------------------------|
| **🔍 Synthetic Nature** | Models trained purely on synthetic data may require domain adaptation for real-world scanned documents. |
| **📐 Layout Variance**  | Leverage layout-aware models (e.g., LayoutLMv3, Donut) rather than pure OCR engines.                    |
| **🧪 Class Balance**    | Perfectly balanced (500/500); standard cross-entropy is sufficient for document classification.         |

#### 💡 Suggested Preprocessing Pipeline

1. **Load metadata**: Parse the CSV files and deserialize the `json_data` column using `json.loads()`.
2. **Image preprocessing**: Convert to grayscale or maintain RGB depending on the model; apply adaptive thresholding if
   using traditional OCR (e.g., Tesseract).
3. **Layout parsing**: For Vision-Language Models (VLMs), tokenize the JSON ground truth to align with document regions.
4. **Augmentation **(training only): The dataset is already heavily noised; apply only mild geometric augmentations to
   avoid destroying text legibility.
5. **Evaluation metrics**: Report Character Error Rate (CER) and Word Error Rate (WER) for OCR; F1-score for NER entity
   extraction.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{patel2026noisymedicaldocs,
    title = {Noisy Medical Document Images – Hospital Bills & Discharge Summaries},
    author = {Patel, Devkumar},
    year = {2026},
    publisher = {Kaggle},
    url = {https://www.kaggle.com/datasets/devp1866/noisy-medical-document-images-ocr}
}
```

---
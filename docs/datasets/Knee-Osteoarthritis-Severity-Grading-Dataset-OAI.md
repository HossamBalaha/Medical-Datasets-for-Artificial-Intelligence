### 🦴 Knee Osteoarthritis Severity Grading Dataset (OAI)

**Study**: Chen, P. (2018). Knee Osteoarthritis Severity Grading Dataset. Mendeley Data, V1.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                          |
|-------------------------|------------------------------------------------------------------|
| **📛 Title**            | Knee Osteoarthritis Severity Grading Dataset                     |
| **🔗 Source**           | https://data.mendeley.com/datasets/56rmx5bjcr/1                  |
| **🦴 Target Organ**     | Knee Joint                                                       |
| **📅 Last Accessed**    | October 06, 2026                                                 |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification, 📍 Localization (Joint Detection) |
| **📐 Image Size**       | Variable (Radiographic X-rays)                                   |
| **📁 Data Format**      | ZIP archive containing organized X-ray images                    |
| **👥 Demographics**     | ❌ Not explicitly detailed in summary                             |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)           |

#### 📊 Dataset Composition

| Category                | Details                                                                 |
|-------------------------|-------------------------------------------------------------------------|
| **🖼️ Total Images**    | Large-scale collection derived from the Osteoarthritis Initiative (OAI) |
| **🏥 Imaging Modality** | Radiographic X-ray (Frontal knee views)                                 |
| **📦 Total Size**       | ~6.68 GB (compressed)                                                   |
| **🏥 Source**           | Osteoarthritis Initiative (OAI) data release                            |

#### 🏷️ Classification Task Details

- **Task Type**: Ordinal multiclass classification of knee osteoarthritis severity
- **Number of Classes**: 5️⃣ (Kellgren-Lawrence Grades 0–4)
    - 🔘 Grade 0: Normal
    - 🟡 Grade 1: Doubtful
    - 🟠 Grade 2: Mild
    - 🔴 Grade 3: Moderate
    - ⚫ Grade 4: Severe

#### 💡 Usage Notes

- ✅ Derived from the highly reputable Osteoarthritis Initiative (OAI), ensuring high clinical validity.
- ✅ Suitable for benchmarking both knee joint detection/localization and subsequent KL severity grading pipelines.
- ✅ Large-scale nature supports robust deep learning model training and generalization studies.
- 📚 Required to cite the original Mendeley Data repository (DOI: 10.17632/56rmx5bjcr.1) in publications.
- 🔐 Distributed under CC BY 4.0; attribution required.

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                           |
|----------------------------|------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**     | Verify grade distribution; lower grades (0-1) typically dominate in population cohorts.  |
| **📐 Resolution Variance** | OAI images may vary in acquisition parameters; standardize dimensions prior to training. |
| **🧪 Validation Strategy** | Implement patient-aware splitting to prevent data leakage across train/test sets.        |

#### 💡 Suggested Preprocessing Pipeline

1. **Extract and organize**: Unzip the dataset and structure images by patient or grade for efficient loading.
2. **Joint Localization **(optional): Apply a detection model or heuristic cropping to isolate the knee joint region,
   removing extraneous background.
3. **Standardize geometry**: Resize cropped images to a uniform dimension (e.g., 224×224 or 512×512).
4. **Intensity normalization**: Apply histogram equalization (e.g., CLAHE) to enhance bone and joint space visibility.
5. **Ordinal encoding**: Encode KL grades as ordered integers (0–4) for ordinal regression or use one-hot vectors with
   ordinal constraints.
6. **Stratified evaluation**: Report per-grade precision, recall, F1-score, and ordinal-aware metrics (e.g., weighted
   kappa).

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{chen2018kneeoa,
    author = {Chen, Pingjun},
    title = {Knee Osteoarthritis Severity Grading Dataset},
    year = {2018},
    publisher = {Mendeley Data},
    version = {1},
    doi = {10.17632/56rmx5bjcr.1},
    url = {https://data.mendeley.com/datasets/56rmx5bjcr/1}
}
```

---

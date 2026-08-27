### 🩸 Uterus Cancer (HISTOPANTUME Subset)

**Study**: Zamanitajeddin, N., et al. (2024). HISTOPANTUME: Histological Pan-cancer Tumor Image Dataset. Zenodo.  
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                          |
|-------------------------|------------------------------------------------------------------|
| **📛 Title**            | HISTOPANTUME Uterus Cancer Histopathology Subset                 |
| **🔗 Source**           | https://www.kaggle.com/datasets/samihamuntahamahin/uterus-cancer |
| **🫁 Target Organ**     | Uterus                                                           |
| **📅 Last Accessed**    | August 27, 2026                                                  |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification (Tumor vs. Non-Tumor)                  |
| **📐 Image Size**       | 224 × 224 pixels                                                 |
| **📁 Data Format**      | JPEG (.jpg)                                                      |
| **👥 Demographics**     | ❌ Not included                                                   |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)           |

#### 📊 Dataset Composition

| Category                | Details                                               |
|-------------------------|-------------------------------------------------------|
| **🖼️ Total Images**    | 6,334 histopathological image patches                 |
| **🏥 Imaging Modality** | Histopathology (H&E stained, derived from TCGA)       |
| **📦 Total Size**       | ~135 MB                                               |
| **🏥 Source**           | Curated subset of the HISTOPANTUME pan-cancer dataset |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification
- **Number of Classes**: 2️⃣
    - 🟢 Non-Tumor: 3,334 images
    - 🔴 Tumor: 3,000 images

#### 💡 Usage Notes

- ✅ Provides a relatively balanced distribution for binary tumor detection, making it ideal for lightweight deep
  learning models and transfer learning.
- ✅ Filenames encode TCGA slide and patch coordinate information, allowing for potential spatial reconstruction or
  patient-level grouping.
- 🔐 License: CC0: Public Domain.

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                                                                          |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Subset Limitation**   | This is a curated subset (sampled from the middle/end of original folders). For comprehensive pan-cancer research, consider using the full HISTOPANTUME dataset.        |
| **📐 Resolution**          | Fixed at 224x224, which is standard for CNNs, but may lack the context of larger tissue architectures.                                                                  |
| **🧪 Validation Strategy** | Group images by their TCGA slide ID prefix (e.g., `TCGA-2E-A9G8`) during splitting to prevent data leakage from the same patient appearing in both train and test sets. |

#### 💡 Suggested Preprocessing Pipeline

1. **Metadata Parsing**: Extract the TCGA slide ID from the filename to enable patient-aware stratified splitting.
2. **Standardize Input**: Ensure all JPEGs are loaded as 3-channel RGB tensors and scaled to [0, 1].
3. **Class Balancing**: Although relatively balanced, apply slight oversampling or class weighting if validation metrics
   show bias toward the majority class.
4. **Augmentation**: Apply standard histopathology augmentations: 90°/180°/270° rotations, horizontal/vertical flips,
   and color jittering.
5. **Model Selection**: Ideal for benchmarking lightweight CNNs (e.g., MobileNet, EfficientNet-B0) or self-supervised
   learning frameworks.

#### 📚 Citation

If you use this dataset, please cite the original HISTOPANTUME publication:

```bibtex
@dataset{zamanitajeddin2024histopantume,
  author = {Zamanitajeddin, N. and Jahanifar, M. and Siraj, F. and Rajpoot, N.},
  title = {HISTOPANTUME: Histological Pan-cancer Tumor Image Dataset},
  year = {2024},
  publisher = {Zenodo},
  doi = {10.5281/zenodo.14555794},
  url = {https://doi.org/10.5281/zenodo.14555794}
}
```

---

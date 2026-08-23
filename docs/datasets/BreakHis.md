### 🫀 BreakHis: Breast Cancer Histopathological Database

**Study**: Spanhol, F. A., Oliveira, L. S., Petitjean, C., & Heutte, L. (2016). A Dataset for Breast Cancer
Histopathological Image Classification. *IEEE Transactions on Biomedical Engineering*, 63(7), 1455-1462.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                  |
|-------------------------|----------------------------------------------------------|
| **📛 Title**            | BreakHis: Breast Cancer Histopathological Database       |
| **🔗 Source**           | https://www.kaggle.com/datasets/ambarishganguly/breakhis |
| **🫀 Target Organ**     | Breast                                                   |
| **📅 Last Accessed**    | August 14, 2026                                          |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                            |
| **📐 Image Size**       | 700 × 460 pixels                                         |
| **📁 Data Format**      | PNG (.png), 3-channel RGB, 8-bit depth                   |
| **👥 Demographics**     | ❌ Not included (82 patients)                             |
| **🔄 Train/Test Split** | ✅ Yes (65% Train / 35% Test, provided in Folds.csv)      |

#### 📊 Dataset Composition

| Category                | Details                                                                 |
|-------------------------|-------------------------------------------------------------------------|
| **🖼️ Total Images**    | 9,109 microscopic images of breast tumor tissue                         |
| **🏥 Imaging Modality** | Brightfield histopathology (H&E stained)                                |
| **🔬 Magnification**    | 40X, 100X, 200X, and 400X                                               |
| **📦 Total Size**       | ~4.28 GB                                                                |
| **🏥 Source**           | P&D Laboratory – Pathological Anatomy and Cytopathology, Parana, Brazil |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of breast tumors (Binary and Fine-grained)
- **Number of Classes**:
    - **Binary**: 2️⃣ (Benign, Malignant)
    - **Fine-grained**: 8️⃣
        - *Benign*: Adenosis (A), Fibroadenoma (F), Phyllodes Tumor (PT), Tubular Adenoma (TA)
        - *Malignant*: Ductal Carcinoma (DC), Lobular Carcinoma (LC), Mucinous Carcinoma (MC), Papillary Carcinoma (PC)

#### 💡 Usage Notes

- ✅ Benchmark dataset for breast cancer histopathological image classification.
- ✅ Includes multiple magnification factors, enabling research on scale-invariant feature learning.
- ✅ Pre-defined patient-aware cross-validation folds (`Folds.csv`) prevent data leakage.
- 📚 Required to cite the original *IEEE Transactions on Biomedical Engineering* publication.
- 🔐 License: Verify specific terms on the source repository (typically academic/research use).

#### ⚠️ Usage Considerations

| Aspect                      | Recommendation                                                                                                           |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------|
| **🔍 Patient Leakage**      | Multiple images originate from the same patient/slide. **Must** use the provided `Folds.csv` for splitting.              |
| **📐 Multi-scale Analysis** | Images are captured at 4 different magnifications; consider multi-branch architectures or magnification-specific models. |
| **🧪 Class Imbalance**      | Malignant samples (5,429) outnumber benign samples (2,480); apply class weighting or focal loss.                         |

#### 💡 Suggested Preprocessing Pipeline

1. **Parse metadata**: Load `Folds.csv` to map image paths to labels, magnification, and cross-validation folds.
2. **Standardize input format**: Resize images to a uniform dimension (e.g., 224x224) while preserving aspect ratio.
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using ImageNet statistics.
4. **Augmentation **(training only): Incorporate rotation, flipping, and color jittering; avoid aggressive distortions
   that alter cellular morphology.
5. **Stratified evaluation**: Report patient-level accuracy, alongside per-class precision, recall, and F1-score.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{spanhol2016dataset,
  title={A dataset for breast cancer histopathological image classification},
  author={Spanhol, Fabio A and Oliveira, Luiz S and Petitjean, Caroline and Heutte, Laurent},
  journal={IEEE transactions on biomedical engineering},
  volume={63},
  number={7},
  pages={1455--1462},
  year={2016},
  publisher={IEEE},
  doi={10.1109/TBME.2015.2496264}
}
```

---

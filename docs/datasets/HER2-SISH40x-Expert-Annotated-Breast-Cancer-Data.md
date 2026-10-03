### 🫀 HER2-SISH40x: Expert-Annotated Breast Cancer Data

**Study**: Rehman, Z. U., et al. (2024). HER2-SISH40x: Expert-Annotated Breast Cancer Data. Kaggle.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                           |
|-------------------------|-------------------------------------------------------------------|
| **📛 Title**            | HER2-SISH40x: Expert-Annotated Breast Cancer Data                 |
| **🔗 Source**           | https://www.kaggle.com/datasets/zakaurrehmanmmu/her2-sish-dataset |
| **🫀 Target Organ**     | Breast                                                            |
| **📅 Last Accessed**    | October 03, 2026                                                  |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                                     |
| **📐 Image Size**       | Variable (high-resolution patches)                                |
| **📁 Data Format**      | PNG (image patches)                                               |
| **👥 Demographics**     | ❌ Not included                                                    |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)            |

#### 📊 Dataset Composition

| Category                | Details                                                      |
|-------------------------|--------------------------------------------------------------|
| **🖼️ Total Patches**   | 537 image patches                                            |
| **🔬 Imaging Modality** | Brightfield histopathology (SISH stained, 40x magnification) |
| **📦 Total Size**       | ~12.86 GB                                                    |
| **🏥 Source**           | 3DHistech Pannoramic DESK scanner                            |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of HER2 amplification status
- **Number of Classes**: 3️⃣
    - 🔴 Amplified
    - 🔵 Non-Amplified
    - ✅ Normal (sampled from both amplified and non-amplified WSIs)

#### 💡 Usage Notes

- ✅ Curated from 50 HER2-SISH stained whole slide images (WSIs) of breast cancer biopsy samples.
- ✅ Expert pathologists annotated 237 Regions of Interest (ROIs), with 300 additional normal ROIs sampled to enrich the
  dataset.
- ✅ Specifically designed to support deep learning applications in HER2 scoring and digital pathology workflows.
- 📚 Recommended to cite the original Kaggle repository when using this dataset.
- 🔐 License: CC BY-NC-SA 4.0 (Non-commercial use with attribution and share-alike).

#### ⚠️ Usage Considerations

| Aspect                    | Recommendation                                                                                    |
|---------------------------|---------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**    | Verify distribution across Amplified, Non-Amplified, and Normal; apply class weighting if needed. |
| **📦 Large File Sizes**   | High-resolution PNGs require significant storage; consider efficient data loaders.                |
| **🧪 Patch-Level Focus**  | Patches are extracted regions; whole-slide inference requires aggregation strategies.             |
| **🔐 Ethical Compliance** | Dataset contains de-identified human tissue; adhere to institutional review requirements.         |

#### 💡 Suggested Preprocessing Pipeline

1. **Organize directory structure**: Arrange patches into class-labeled subfolders (`Amplified`, `Non-Amplified`,
   `ROI_Normal`).
2. **Standardize input**: Confirm uniform dimensions or resize to model-compatible sizes (e.g., 224×224 or 512×512).
3. **Color normalization**: Apply stain normalization to mitigate inter-slide SISH staining variability.
4. **Augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering; preserve
   morphological integrity of SISH signals.
5. **Stratified splitting**: Implement patient-aware or slide-aware partitioning to prevent data leakage.
6. **Evaluation metrics**: Report macro-averaged F1-score, AUC-ROC, and confusion matrices to assess HER2 amplification
   prediction accuracy.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{rehman2024her2sish,
    author = {Rehman, Zaka Ur},
    title = {HER2-SISH40x: Expert-Annotated Breast Cancer Data},
    year = {2024},
    publisher = {Kaggle},
    url = {https://www.kaggle.com/datasets/zakaurrehmanmmu/her2-sish-dataset}
}
```

---

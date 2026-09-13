### 🩺 General Dataset (TCIA Histopathology Patches)
**Study**: Cuticchia, G. (2024). General Dataset (TCIA). Kaggle.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                 |
|-------------------------|-------------------------------------------------------------------------|
| **📛 Title**            | General Dataset (TCIA Histopathology Patches)                           |
| **🔗 Source**           | https://www.kaggle.com/datasets/giancarlocuticchia/general-dataset-tcia |
| **🩺 Target Organ**     | Multi-organ (Blood, Bone, Brain, Breast, Colon, Esophagus, Kidney, Lung, Ovary, Pancreas, Prostate, Skin, Uterus) |
| **📅 Last Accessed**    | September 11, 2026                                                      |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification, 🔍 Super-Resolution                      |
| **📐 Image Size**       | HR: 2000–2276 px; LR_bicubic/X4: 500–569 px                             |
| **📁 Data Format**      | PNG (.png)                                                              |
| **👥 Demographics**     | ❌ Not included                                                          |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                  |

#### 📊 Dataset Composition
| Category                | Details                                                                 |
|-------------------------|-------------------------------------------------------------------------|
| **🖼️ Total Images**    | 5,000 image patches (2,500 HR + 2,500 LR)                               |
| **🔬 Imaging Modality** | Brightfield histopathology (20x magnification)                          |
| **📦 Total Size**       | ~22.66 GB (compressed)                                                  |
| **🏥 Source**           | The Cancer Imaging Archive (TCIA) collections (e.g., CPTAC, CMB)        |

#### 🏷️ Classification & Super-Resolution Task Details
- **Task Type**: Multiclass tissue classification and/or image super-resolution
- **Data Structure**: 
  - `HR` folder: High-resolution patches (2000–2276 px) from 20x magnification.
  - `LR_bicubic/X4` folder: Down-scaled versions of the HR patches by a factor of 4 (500–569 px).
- **Organ Diversity**: Spans 13+ organ systems, providing a highly heterogeneous histopathological dataset.

#### 💡 Usage Notes
- ✅ Unique paired HR/LR structure makes it suitable for both tissue classification and medical image super-resolution research.
- ✅ High diversity across multiple cancer types and organs supports robust domain generalization studies.
- 📚 Required to cite the original Kaggle repository and acknowledge the underlying TCIA collections.
- 🔐 License: MIT

#### ⚠️ Usage Considerations
| Aspect                     | Recommendation                                                                     |
|----------------------------|------------------------------------------------------------------------------------|
| **🔍 Extreme Heterogeneity**| The dataset spans vastly different tissue types; consider training organ-specific models or using domain adaptation techniques. |
| **📐 Memory Constraints**  | HR images are very large (up to 2276px); ensure adequate GPU memory or use patch-based processing. |
| **🧪 Validation Strategy** | Implement stratified splitting by organ or TCIA collection to evaluate cross-domain generalization. |

#### 💡 Suggested Preprocessing Pipeline
1. **Select task variant**: Use the `HR` folder for classification/super-resolution targets, and `LR_bicubic/X4` for low-resolution inputs.
2. **Patch extraction **(for HR): If GPU memory is limited, extract smaller, fixed-size tiles (e.g., 512×512) from the HR images.
3. **Standardize input**: Resize LR images to match the target HR dimensions if performing super-resolution evaluation.
4. **Color normalization**: Apply stain normalization to mitigate inter-collection staining variability.
5. **Augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering.
6. **Stratified evaluation**: Report per-class metrics and, if applicable, PSNR/SSIM for super-resolution quality assessment.

#### 📚 Citation
If you use this dataset, please cite:
```bibtex
@dataset{cuticchia2024generaltcia,
  author = {Cuticchia, Giancarlo},
  title = {General Dataset (TCIA)},
  year = {2024},
  publisher = {Kaggle},
  url = {https://www.kaggle.com/datasets/giancarlocuticchia/general-dataset-tcia}
}
```

---

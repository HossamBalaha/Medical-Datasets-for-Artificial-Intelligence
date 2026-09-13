### 🫀 Breast Ultrasound Image Database

**Study**: Ardakani, A. A., Mohammadi, A., Mirza-Aghazadeh-Attari, M., & Acharya, U. R. (2023). An open-access breast
lesion ultrasound image database: Applicable in artificial intelligence studies. *Computers in Biology and Medicine*,
152, 106438.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                |
|-------------------------|--------------------------------------------------------|
| **📛 Title**            | Breast Ultrasound Image Database                       |
| **🔗 Source**           | https://qamebi.com/breast-ultrasound-images-database/  |
| **🫀 Target Organ**     | Breast                                                 |
| **📅 Last Accessed**    | September 10, 2026                                     |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification, 🎭 Semantic Segmentation    |
| **📐 Image Size**       | Variable (ultrasound acquisitions)                     |
| **📁 Data Format**      | Images (JPEG/PNG) and radiologist-defined masks        |
| **👥 Demographics**     | ❌ Not explicitly detailed (multi-center cohorts)       |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended) |

#### 📊 Dataset Composition

| Category                | Details                                                               |
|-------------------------|-----------------------------------------------------------------------|
| **🖼️ Total Images**    | Two distinct sets: Histologically proven Benign and Malignant lesions |
| **🏥 Imaging Modality** | Medical Ultrasound Imaging                                            |
| **🔬 Scanner**          | Aixplorer Ultimate ultrasound system (Supersonic Imagine)             |
| **🏥 Source**           | Multi-center cohorts (QAMEBI research group)                          |

#### 🏷️ Classification & Segmentation Task Details

- **Task Type**: Binary classification of breast lesions and pixel-wise segmentation of lesion boundaries.
- **Number of Classes**: 2️⃣
    - ✅ Benign lesions
    - ⚠️ Malignant lesions
- **Annotation Targets**: Radiologist-defined segmentation masks for each lesion.

#### 💡 Usage Notes

- ✅ Vital resource for developing robust Computer-Aided Diagnosis (CAD) systems for breast cancer.
- ✅ Multi-center data collection helps minimize confounding factors and improves model generalizability across different
  populations.
- ✅ Includes both raw ultrasound images and corresponding ground-truth segmentation masks.
- 📚 Required to cite the original *Computers in Biology and Medicine* publication when using this dataset.
- 🔐 License: Free for research use with proper citation (verify specific terms for commercial deployment).

#### ⚠️ Usage Considerations

| Aspect                       | Recommendation                                                                                                              |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**       | Verify the exact ratio of benign to malignant cases; apply class weighting if needed.                                       |
| **🎨 Speckle Noise**         | Ultrasound images inherently contain speckle noise; consider applying specialized despeckling filters during preprocessing. |
| **🧪 Domain Generalization** | Multi-center data is a strength, but ensure your evaluation strategy tests cross-center robustness.                         |

#### 💡 Suggested Preprocessing Pipeline

1. **Load data**: Ingest images and corresponding radiologist-defined masks.
2. **Despeckling **(optional): Apply ultrasound-specific noise reduction (e.g., Non-Local Means or Anisotropic
   Diffusion).
3. **Standardize geometry**: Resize images and masks to uniform dimensions (e.g., 256×256 or 512×512) while preserving
   aspect ratio.
4. **Intensity normalization**: Scale pixel values to [0, 1] or apply Contrast Limited Adaptive Histogram Equalization (
   CLAHE) to enhance lesion visibility.
5. **Augmentation **(training only): Incorporate rotation, flipping, and elastic deformations; preserve morphological
   integrity of the lesion.
6. **Evaluation metrics**: Report AUC-ROC and F1-score for classification; compute Dice coefficient and IoU for
   segmentation.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{ardakani2023open,
  title={An open-access breast lesion ultrasound image database: Applicable in artificial intelligence studies},
  author={Ardakani, A Abbasian and Mohammadi, A and Mirza-Aghazadeh-Attari, M and Acharya, U Rajendra},
  journal={Computers in Biology and Medicine},
  volume={152},
  pages={106438},
  year={2023},
  publisher={Elsevier},
  doi={10.1016/j.compbiomed.2022.106438}
}
```

---

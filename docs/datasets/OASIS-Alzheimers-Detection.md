### 🧠 OASIS Alzheimer's Detection

**Study**: Marcus, D., Buckner, R., Csernansky, J., & Morris, J. (2007). OASIS-1: Cross-Sectional. Journal of Cognitive
Neuroscience. (Kaggle adaptation by NINAD AITHAL).
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                            |
|-------------------------|--------------------------------------------------------------------|
| **📛 Title**            | OASIS Alzheimer's Detection                                        |
| **🔗 Source**           | https://www.kaggle.com/datasets/ninadaithal/imagesoasis            |
| **🧠 Target Organ**     | Brain                                                              |
| **📅 Last Accessed**    | August 13, 2026                                                    |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                                      |
| **📐 Image Size**       | 2D slices extracted from 3D volumes (variable, resized for Kaggle) |
| **📁 Data Format**      | JPEG (.jpg) (converted from original NIfTI format)                 |
| **👥 Demographics**     | ❌ Not included in this specific Kaggle subset (461 patients total) |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)             |

#### 📊 Dataset Composition

| Category                | Details                                                         |
|-------------------------|-----------------------------------------------------------------|
| **🖼️ Total Images**    | ~86,400 2D slices (slices 100–160 along the z-axis per patient) |
| **🏥 Imaging Modality** | Magnetic Resonance Imaging (MRI)                                |
| **📦 Total Size**       | ~1.36 GB (compressed)                                           |
| **🏥 Source**           | Open Access Series of Imaging Studies (OASIS)                   |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of Alzheimer's disease progression
- **Number of Classes**: 4️⃣ (Based on Clinical Dementia Rating, CDR)
    - ✅ Non Demented (CDR = 0, ~67.2k images)
    - 🟡 Very Mild Dementia (CDR = 0.5, ~13.7k images)
    - 🟠 Mild Dementia (CDR = 1, ~5,002 images)
    - 🔴 Moderate Dementia (CDR = 2, ~488 images)

#### 💡 Usage Notes

- ✅ Large-scale resource for early Alzheimer's detection and disease progression modeling.
- ✅ Pre-sliced 2D format reduces the computational barrier to entry compared to full 3D NIfTI volumes.
- 📚 Required to cite both the original OASIS publication and the Kaggle repository.
- 🔐 License: Apache 2.0

#### ⚠️ Usage Considerations

| Aspect                        | Recommendation                                                                                                                     |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Severe Class Imbalance** | Non-demented class heavily dominates (~77%); apply focal loss, class weighting, or oversampling.                                   |
| **🧪 Data Leakage Risk**      | Multiple slices belong to the same patient. **Must** split by patient ID, not by individual image, to prevent severe data leakage. |
| **📐 2D vs 3D Limitation**    | Converting 3D MRI to 2D slices loses volumetric context; consider reconstructing volumes if using 3D architectures.                |
| **🎨 Format Conversion**      | JPEG compression may introduce artifacts; verify image quality before training.                                                    |

#### 💡 Suggested Preprocessing Pipeline

1. **Patient-aware splitting**: Group images by patient ID (if metadata is available) and partition into train/val/test
   sets to ensure no patient overlap.
   the dataset.
3. **Intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
4. **Augmentation**: Incorporate rotation, flipping, and mild intensity jittering to improve model generalization.
5. **Stratified evaluation**: Report per-class precision, recall, F1-score, and ordinal-aware metrics (e.g., weighted
   kappa) to assess progression detection.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{marcus2007oasis,
  author = {Marcus, D. S. and Wang, T. H. and Parker, J. and Csernansky, J. G. and Morris, J. C. and Buckner, R. L.},
  title = {Open Access Series of Imaging Studies (OASIS): Cross-sectional MRI Data in Young, Middle Aged, Nondemented, and Demented Older Adults},
  journal = {Journal of Cognitive Neuroscience},
  volume = {19},
  number = {9},
  pages = {1498--1507},
  year = {2007},
  doi = {10.1162/jocn.2007.19.9.1498}
}
```

---

### 👁️ Glaucoma Fundus Images with OD/OC Masks

**Study**: Meesam, S. (2025). Glaucoma Fundus Images with OD/OC Masks. Kaggle. (Derived from Kiefer, R. et al.,
EyePACS-AIROGS-Light-V2).
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------|
| **📛 Title**            | Glaucoma Fundus Images with OD/OC Masks                                                      |
| **🔗 Source**           | https://www.kaggle.com/datasets/meesamrizvi/glaucoma-fundus-images-with-predicted-odoc-masks |
| **👁️ Target Organ**    | Eye (Retina / Fundus)                                                                        |
| **📅 Last Accessed**    | September 10, 2026                                                                           |
| **🎯 Supported Tasks**  | 🎭 Semantic Segmentation                                                                     |
| **📐 Image Size**       | Variable (standardized fundus images)                                                        |
| **📁 Data Format**      | Images (JPEG/PNG) and predicted segmentation masks                                           |
| **👥 Demographics**     | ❌ Not included (de-identified clinical fundus images)                                        |
| **🔄 Train/Test Split** | ❌ Not provided (unified structure)                                                           |

#### 📊 Dataset Composition

| Category                | Details                                             |
|-------------------------|-----------------------------------------------------|
| **🖼️ Total Images**    | 9,540 fundus images                                 |
| **🎭 Total Masks**      | 9,540 Optic Cup masks, 9,432 Optic Disc masks       |
| **🏥 Imaging Modality** | Color Fundus Photography                            |
| **📦 Total Size**       | ~582.67 MB (compressed)                             |
| **🏥 Source**           | Derived from EyePACS-AIROGS-Light-V2 (Riley Kiefer) |

#### 🎭 Segmentation Task Details

- **Task Type**: Binary semantic segmentation of optic nerve head structures
- **Annotation Targets**:
    - ⚪ Optic Disc (OD)
    - 🔴 Optic Cup (OC)
- **Annotation Protocol**: Masks were generated using a custom AI segmentation pipeline by the dataset author, providing
  ready-to-use pseudo-labels for glaucoma research.

#### 💡 Usage Notes

- ✅ Provides a unified, simplified folder structure (merged train/val/test) for easier data loading.
- ✅ Offers immediate access to OD/OC segmentation masks, which are critical biomarkers for glaucoma detection (e.g.,
  Cup-to-Disc Ratio calculation).
- ✅ Useful for benchmarking segmentation models or as a pre-training dataset for glaucoma-related computer vision tasks.
- 📚 Required to cite both this Kaggle repository and the original EyePACS-AIROGS-Light-V2 source datasets.
- 🔐 License: CC BY-NC-SA 4.0

#### ⚠️ Usage Considerations

| Aspect                      | Recommendation                                                                                               |
|-----------------------------|--------------------------------------------------------------------------------------------------------------|
| **🔍 Pseudo-Label Quality** | Masks are model-predicted, not manually annotated by experts; verify mask quality for critical applications. |
| **📐 Resolution Variance**  | Original fundus images vary in dimensions; standardize to fixed dimensions prior to training.                |
| **🧪 Data Leakage**         | Since train/val/test were merged, implement your own patient-aware splitting to prevent leakage.             |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Ingest images and corresponding OD/OC masks from their respective folders.
2. **Standardize geometry**: Resize images and masks to uniform dimensions (e.g., 256×256 or 512×512) while preserving
   aspect ratio.
3. **Intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide statistics.
4. **Augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering; apply identical
   geometric transforms to images and masks.
5. **Evaluation metrics**: Report Dice coefficient and Intersection over Union (IoU) for both Optic Disc and Optic Cup
   segmentation.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{meesam2025glaucoma,
  author = {Meesam, Syed},
  title = {Glaucoma Fundus Images with OD/OC Masks},
  year = {2025},
  publisher = {Kaggle},
  url = {https://www.kaggle.com/datasets/meesamrizvi/glaucoma-fundus-images-with-predicted-odoc-masks}
}
```

---

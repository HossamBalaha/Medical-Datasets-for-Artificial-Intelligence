### 🫁 CRD: Chest X-Ray Images with Lung Segmented Masks

**Study**: Shah, M. (2025). CRD: Chest X-Ray Images with Lung Segmented Masks. Kaggle.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------|
| **📛 Title**            | CRD: Chest X-Ray Images with Lung Segmented Masks                                            |
| **🔗 Source**           | https://www.kaggle.com/datasets/mrunalnshah/crd-chest-x-ray-images-with-lung-segmented-masks |
| **🫁 Target Organ**     | Lungs / Chest                                                                                |
| **📅 Last Accessed**    | August 31, 2026                                                                              |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification, 🎭 Semantic Segmentation                                          |
| **📐 Image Size**       | Variable (standardization recommended)                                                       |
| **📁 Data Format**      | PNG (.png) for both images and masks                                                         |
| **👥 Demographics**     | ❌ Not included (de-identified clinical images)                                               |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                                       |

#### 📊 Dataset Composition

| Category                   | Details                                                                       |
|----------------------------|-------------------------------------------------------------------------------|
| **🖼️ Total Images**       | 3,311 chest X-ray images + 3,311 corresponding segmentation masks             |
| **🏥 Imaging Modality**    | Radiographic X-ray (Frontal)                                                  |
| **📦 Total Size**          | ~2.55 GB (compressed)                                                         |
| **🏥 Source Institutions** | Aggregated from Darwin (2,607), Montgomery (138), and Shenzhen (566) datasets |

#### 🏷️ Classification & Segmentation Task Details

- **Classification Task**: Binary classification based on radio density.
    - **Radio-Opaque**: 1,691 images (appear white/light gray; represent dense structures like fluid, masses, or bones).
    - **Radio-Lucent**: 1,620 images (appear dark/black; indicate air-filled spaces like healthy lung tissue).
- **Segmentation Task**: Binary semantic segmentation of the lung fields.
    - **Annotation Targets**: Pixel-wise mask isolating the lung regions from the background and mediastinum.

#### 💡 Usage Notes

- ✅ Unique dataset providing both radio-density classification labels and lung segmentation masks.
- ✅ Aggregated from three well-known public datasets, offering a diverse set of imaging protocols and patient
  demographics.
- ✅ Perfectly balanced classification targets (1,691 vs. 1,620) support stable training without aggressive resampling.
- 📚 Recommended to cite the original Kaggle repository and the constituent source datasets when using this data.
- 🔐 License: CC0: Public Domain.

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                      |
|----------------------------|-----------------------------------------------------------------------------------------------------|
| **📦 Data Heterogeneity**  | Sourced from multiple databases with varying resolutions; standardize dimensions prior to training. |
| **🧪 Validation Strategy** | No predefined split; implement patient-aware or source-aware partitioning to prevent data leakage.  |
| **🔐 Ethical Compliance**  | Dataset contains de-identified clinical imagery; adhere to institutional review requirements.       |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Ingest images and corresponding masks from their respective folders.
2. **Standardize geometry**: Resize images and masks to uniform dimensions (e.g., 256×256 or 512×512) while preserving
   aspect ratio.
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide statistics.
4. **Augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering; preserve lung
   boundary integrity.
5. **Stratified splitting**: Partition data by source dataset to evaluate cross-domain generalization.
6. **Evaluation metrics**: Report Dice/IoU for segmentation, and accuracy, sensitivity, specificity, and AUC-ROC for
   classification.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{shah2025crd,
  author = {Shah, Mrunal},
  title = {CRD: Chest X-Ray Images with Lung Segmented Masks},
  year = {2025},
  publisher = {Kaggle},
  url = {https://www.kaggle.com/datasets/mrunalnshah/crd-chest-x-ray-images-with-lung-segmented-masks}
}
```

---

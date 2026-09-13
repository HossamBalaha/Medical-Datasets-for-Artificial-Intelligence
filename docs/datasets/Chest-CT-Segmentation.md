### 🫁🫀 Chest CT Segmentation (Lung, Heart, Trachea)

**Study**: Polo, M. (2020). Chest CT Segmentation. Kaggle. (Modified from Kónya et al., 2020).
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                            |
|-------------------------|--------------------------------------------------------------------|
| **📛 Title**            | Chest CT Segmentation                                              |
| **🔗 Source**           | https://www.kaggle.com/datasets/polomarco/chest-ct-segmentation    |
| **🫁🫀 Target Organ**   | Lungs / Heart / Trachea                                            |
| **📅 Last Accessed**    | September 11, 2026                                                 |
| **🎯 Supported Tasks**  | 🎭 Semantic Segmentation                                           |
| **📐 Image Size**       | Variable (slice width/height individual to each tensor ID)         |
| **📁 Data Format**      | RGB images and masks (converted from original NRRD/Pickle tensors) |
| **👥 Demographics**     | ❌ Not included                                                     |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)             |

#### 📊 Dataset Composition

| Category                | Details                                                       |
|-------------------------|---------------------------------------------------------------|
| **🖼️ Total Slices**    | ~16,708 image slices (with corresponding masks)               |
| **🔬 Imaging Modality** | Computed Tomography (CT)                                      |
| **🎨 Color Format**     | RGB (converted from single tensor format)                     |
| **📦 Total Size**       | ~1.79 GB (compressed)                                         |
| **🏥 Source**           | Modified from Lung segmentation dataset by Kónya et al., 2020 |

#### 🎭 Segmentation Task Details

- **Task Type**: Multiclass semantic segmentation of thoracic anatomy
- **Number of Classes**: 3️⃣
    - 🫁 Lungs
    - 🫀 Heart
    - 🌬️ Trachea
- **Annotation Format**: RGB mask images where channels correspond to the three classes.

#### 💡 Usage Notes

- ✅ Provides a ready-to-use RGB image and mask format, simplifying the preprocessing pipeline compared to raw NRRD or
  pickle tensors.
- ✅ Suitable for benchmarking multi-organ thoracic segmentation models (e.g., U-Net variants).
- 📚 Recommended to cite the original Kónya et al. work and this Kaggle repository.
- 🔐 License: Unknown (Verify specific terms on Kaggle before commercial use).

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                      |
|----------------------------|---------------------------------------------------------------------------------------------------------------------|
| **📦 Data Format**         | Original data was NRRD/Pickle; this version uses RGB images. Ensure channel mapping aligns with your loss function. |
| **📐 Slice Variance**      | Width, height, and number of slices vary per patient ID; standardize dimensions prior to batch training.            |
| **🧪 Validation Strategy** | Implement patient-aware splitting (group by ImageId prefix) to prevent data leakage across train/test sets.         |

#### 💡 Suggested Preprocessing Pipeline

1. **Load metadata**: Parse `train.csv` to map `ImageId` to `MaskId`.
2. **Standardize geometry**: Resize images and masks to uniform dimensions (e.g., 256×256 or 512×512). Use
   nearest-neighbor interpolation for masks.
3. **Intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide statistics.
4. **Augmentation **(training only): Apply synchronized geometric transformations (rotation, flipping, elastic
   deformations) to both images and masks.
5. **Evaluation metrics**: Report Dice Similarity Coefficient (DSC) and Intersection over Union (IoU) for each of the
   three organ classes.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{polo2020chestctseg,
  author = {Polo, Marco},
  title = {Chest CT Segmentation},
  year = {2020},
  publisher = {Kaggle},
  url = {https://www.kaggle.com/datasets/polomarco/chest-ct-segmentation}
}
```

---

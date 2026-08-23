### 🫁 Finding and Measuring Lungs in CT Data

**Study**: Mader, K. S. (2017). Finding and Measuring Lungs in CT Data. Kaggle.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                         |
|-------------------------|-----------------------------------------------------------------|
| **📛 Title**            | Finding and Measuring Lungs in CT Data                          |
| **🔗 Source**           | https://www.kaggle.com/datasets/kmader/finding-lungs-in-ct-data |
| **🫁 Target Organ**     | Lungs / Chest                                                   |
| **📅 Last Accessed**    | August 21, 2026                                                 |
| **🎯 Supported Tasks**  | 🎭 Semantic Segmentation                                        |
| **📐 Image Size**       | Variable (2D slices and 3D NIfTI volumes)                       |
| **📁 Data Format**      | ZIP archives (2D/3D images and masks), CSV (lung statistics)    |
| **👥 Demographics**     | ❌ Not included (de-identified)                                  |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)          |

#### 📊 Dataset Composition

| Category                | Details                                                                         |
|-------------------------|---------------------------------------------------------------------------------|
| **🖼️ Total Volumes**   | Collection of 2D and 3D CT images                                               |
| **🏥 Imaging Modality** | Computed Tomography (CT)                                                        |
| **🎨 Color Format**     | Grayscale (Hounsfield Units)                                                    |
| **📦 Total Size**       | ~662.59 MB (compressed archives)                                                |
| **🏥 Source**           | Aggregated from public medical imaging challenges (e.g., LUNA, Kaggle DSB 2017) |

#### 🎭 Segmentation Task Details

- **Task Type**: Binary semantic segmentation of lung fields in CT scans
- **Annotation Targets**: Manually segmented lung masks to isolate lung tissue from the chest wall, mediastinum, and
  background.
- **Associated Metrics**: Includes a `lung_stats.csv` file with clinical measurements such as lung volume and Percentile
  Density (PD) (e.g., 5th and 95th percentile Hounsfield units), which are critical for assessing conditions like
  emphysema in smokers.

#### 💡 Usage Notes

- ✅ Essential preprocessing dataset: Accurate lung segmentation is a critical first step for downstream tasks like
  nodule detection (e.g., LUNA16) or disease classification in CT scans.
- ✅ Provides both 2D slice-level and 3D volume-level data, supporting research into both 2D CNNs and 3D volumetric
  networks (e.g., 3D U-Net).
- ✅ Includes ground-truth clinical measurements, enabling research into quantitative radiomics and automated biomarker
  extraction.
- 📚 Recommended to cite the original Kaggle dataset and associated challenge publications.
- 🔐 License: Unknown (Verify specific terms on Kaggle; typically for research use).

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                                                        |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| **📦 3D Data Handling**    | 3D NIfTI volumes require significant memory; utilize libraries like `nibabel` or `SimpleITK` and consider patch-based training.                       |
| **🎨 HU Windowing**        | CT scans contain a wide range of Hounsfield Units; apply lung windowing (e.g., -1000 to 400 HU) before normalization to enhance lung tissue contrast. |
| **🧪 Validation Strategy** | Implement patient-aware splitting to ensure no slices from the same 3D volume leak into both training and testing sets.                               |

#### 💡 Suggested Preprocessing Pipeline

1. **Load NIfTI/ZIP data**: Use `nibabel` or `SimpleITK` to read 3D volumes and their corresponding segmentation masks.
2. **Apply HU Windowing**: Clip Hounsfield Units to a lung-specific window (e.g., -1000 to 400 HU) and normalize
   to [0, 1].
3. **Resampling **(for 3D): Resample volumes to isotropic voxel spacing (e.g., 1.0 × 1.0 × 1.0 mm) for consistent 3D CNN
   input.
4. **Patch Extraction **(optional): For memory efficiency, extract 3D patches (e.g., 64x64x64) centered around the lung
   regions.
5. **Synchronized Augmentation**: Apply 3D rotations, flips, and elastic deformations identically to both the image
   volume and the mask.
6. **Evaluation metrics**: Report 3D Dice coefficient and Volumetric IoU to assess segmentation accuracy.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{mader2017findinglungs,
  author = {Mader, K Scott},
  title = {Finding and Measuring Lungs in CT Data},
  year = {2017},
  publisher = {Kaggle},
  url = {https://www.kaggle.com/datasets/kmader/finding-lungs-in-ct-data}
}
```

---

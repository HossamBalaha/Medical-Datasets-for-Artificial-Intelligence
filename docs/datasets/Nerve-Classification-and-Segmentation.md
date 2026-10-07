### 🧠 Nerve Classification and Segmentation

**Study**: He, Z. (2022). Nerve Classification and Segmentation. Figshare.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                                |
|-------------------------|----------------------------------------------------------------------------------------|
| **📛 Title**            | Nerve Classification and Segmentation                                                  |
| **🔗 Source**           | https://figshare.com/articles/dataset/Nerve_Classification_and_Segmentation/20787751/1 |
| **🧠 Target Organ**     | Nervous System (Peripheral Nerves)                                                     |
| **📅 Last Accessed**    | October 06, 2026                                                                       |
| **🎯 Supported Tasks**  | 🏷️ Classification, 🎭 Semantic Segmentation                                           |
| **📐 Image Size**       | Variable                                                                               |
| **📁 Data Format**      | ZIP archive (Images and corresponding masks)                                           |
| **👥 Demographics**     | ❌ Not included                                                                         |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                                 |

#### 📊 Dataset Composition

| Category                | Details                                                               |
|-------------------------|-----------------------------------------------------------------------|
| **🖼️ Total Images**    | Collection of medical images featuring peripheral nerves              |
| **🏥 Imaging Modality** | Medical Imaging (Typically Ultrasound or MRI for nerve visualization) |
| **📦 Total Size**       | ~2.71 GB (compressed)                                                 |
| **🏥 Source**           | Figshare Health Informatics repository                                |

#### 🎭 Segmentation Task Details

- **Task Type**: Binary/Multiclass semantic segmentation of nerve structures
- **Annotation Targets**: Nerve boundaries and internal fascicular patterns vs. background tissue.

#### 💡 Usage Notes

- ✅ Valuable resource for developing automated nerve identification and segmentation tools, which are critical for
  regional anesthesia and surgical planning.
- ✅ Supports joint classification and segmentation workflows.
- 📚 Required to cite the original Figshare repository (DOI: 10.6084/m9.figshare.20787751.v1) in publications.
- 🔐 Distributed under CC BY 4.0; attribution required.

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                  |
|----------------------------|-------------------------------------------------------------------------------------------------|
| **🔍 Annotation Quality**  | Verify mask alignment with image boundaries; medical segmentation requires high precision.      |
| **📐 Resolution Variance** | Standardize input dimensions while preserving the aspect ratio of anatomical structures.        |
| **🧪 Domain Specificity**  | Models trained on this specific modality may require domain adaptation for other imaging types. |

#### 💡 Suggested Preprocessing Pipeline

1. **Extract archives**: Unzip the dataset to access paired images and segmentation masks.
2. **Standardize geometry**: Resize images and corresponding masks to a uniform dimension (e.g., 256×256 or 512×512).
   Use nearest-neighbor interpolation for masks.
3. **Intensity normalization**: Scale image pixel values to [0, 1] or standardize using dataset-wide statistics.
4. **Augmentation **(training only): Apply synchronized geometric transformations (rotation, flipping, elastic
   deformations) to both images and masks to simulate anatomical variance.
5. **Stratified evaluation**: Report Dice Similarity Coefficient (DSC) and Intersection over Union (IoU) for
   segmentation accuracy.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{he2022nerve,
    author = {He, ZeBang},
    title = {Nerve Classification and Segmentation},
    year = {2022},
    publisher = {Figshare},
    version = {1},
    doi = {10.6084/m9.figshare.20787751.v1},
    url = {https://figshare.com/articles/dataset/Nerve_Classification_and_Segmentation/20787751/1}
}
```

---

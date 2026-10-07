### 🗣️ CE-NBI Data Set for Laryngeal Lesion Assessment

**Study**: Esmaeili, N., Davaris, N., Boese, A., Illanes, A., Friebe, M., & Arens, C. (2022). Contact Endoscopy – Narrow
Band Imaging (CE-NBI) Data Set for Laryngeal Lesion Assessment. Zenodo.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                |
|-------------------------|--------------------------------------------------------|
| **📛 Title**            | CE-NBI Data Set for Laryngeal Lesion Assessment        |
| **🔗 Source**           | https://zenodo.org/records/6674034                     |
| **🗣️ Target Organ**    | Larynx / Vocal Folds                                   |
| **📅 Last Accessed**    | October 06, 2026                                       |
| **🎯 Supported Tasks**  | 🏷️ Multiclass / Binary Classification                 |
| **📐 Image Size**       | Variable (Endoscopic images)                           |
| **📁 Data Format**      | ZIP archive (Images) + Excel (metadata mapping)        |
| **👥 Demographics**     | ✅ 210 adult patients                                   |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended) |

#### 📊 Dataset Composition

| Category                | Details                                                        |
|-------------------------|----------------------------------------------------------------|
| **🖼️ Total Images**    | 11,144 Contact Endoscopy – Narrow Band Imaging (CE-NBI) images |
| **🏥 Imaging Modality** | Endoscopy (Narrow Band Imaging)                                |
| **📦 Total Size**       | ~1.4 GB (compressed)                                           |
| **🏥 Source**           | Clinical study on vocal fold subepithelial vascular variations |

#### 🏷️ Classification Task Details

- **Task Type**: Binary/Multiclass classification of laryngeal lesions based on vascular patterns
- **Number of Classes**:
    - **Primary**: 2️⃣ (Benign, Malignant)
    - **Secondary Annotations**: Histopathology label, Leukoplakia diagnosis label.

#### 💡 Usage Notes

- ✅ First publicly available dataset with enhanced, magnified visualization of vocal fold subepithelial blood vessels.
- ✅ Highly valuable for developing Computer-Aided Diagnosis (CAD) systems to reduce subjective evaluation in laryngeal
  cancer assessment.
- ✅ Includes comprehensive Excel metadata mapping each image to patient ID and multiple diagnostic labels.
- 📚 Required to cite the original Zenodo repository and associated publications in derivative works.
- 🔐 Distributed under CC BY 4.0; attribution required.

#### ⚠️ Usage Considerations

| Aspect                       | Recommendation                                                                                                                      |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Patient-Level Leakage** | Multiple images belong to the same patient (210 total); **must** split by patient ID, not by image, to prevent severe data leakage. |
| **🎨 Image Characteristics** | CE-NBI images have distinct green/blue vascular contrast; models may need specific preprocessing to enhance vessel texture.         |
| **🧪 Class Imbalance**       | Verify the ratio of benign to malignant lesions; apply class weighting if necessary.                                                |

#### 💡 Suggested Preprocessing Pipeline

1. **Parse metadata**: Load the provided Excel file to map image filenames to patient IDs and diagnostic labels.
2. **Patient-aware splitting**: Partition the data into train/validation/test sets ensuring no patient ID overlaps
   between splits.
3. **Standardize geometry**: Resize images to a uniform dimension (e.g., 224×224 or 512×512) while preserving aspect
   ratio.
4. **Vessel enhancement **(optional): Apply green-channel extraction or CLAHE to highlight the narrow-band vascular
   patterns.
5. **Augmentation **(training only): Incorporate rotation, flipping, and mild color jittering to improve generalization
   across different endoscopic angles.
6. **Stratified evaluation**: Report per-class AUC-ROC, sensitivity, and specificity, which are critical metrics for
   clinical cancer detection tasks.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{esmaeili2022cenbi,
    author = {Esmaeili, Nazila and Davaris, Nikolaos and Boese, Axel and Illanes, Alfredo and Friebe, Michael and Arens, Christoph},
    title = {Contact Endoscopy – Narrow Band Imaging (CE-NBI) Data Set for Laryngeal Lesion Assessment},
    year = {2022},
    publisher = {Zenodo},
    version = {1},
    doi = {10.5281/zenodo.6674034},
    url = {https://doi.org/10.5281/zenodo.6674034}
}
```

---

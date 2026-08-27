### 🩺 Gastric Cancer Histopathology Tissue Image Dataset (GCHTID)

**Study**: Lou, S., et al. (2024). Gastric Cancer Histopathology Tissue Image Dataset (GCHTID). figshare.  
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                                   |
|-------------------------|-------------------------------------------------------------------------------------------|
| **📛 Title**            | Gastric Cancer Histopathology Tissue Image Dataset (GCHTID)                               |
| **🔗 Source**           | https://www.kaggle.com/datasets/orvile/gastric-cancer-histopathology-tissue-image-dataset |
| **🫁 Target Organ**     | Stomach / Gastric                                                                         |
| **📅 Last Accessed**    | August 27, 2026                                                                           |
| **🎯 Supported Tasks**  | 🏷️ Multi-class Tissue Classification                                                     |
| **📐 Image Size**       | 224 × 224 pixels                                                                          |
| **📁 Data Format**      | Image patches (JPEG/PNG) + Clinical Metadata (CSV)                                        |
| **👥 Demographics**     | ✅ Included (Age, gender, T/N/M staging, histology type in CSV)                            |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                                    |

#### 📊 Dataset Composition

| Category                | Details                                                 |
|-------------------------|---------------------------------------------------------|
| **🖼️ Total Images**    | 31,096 non-overlapping image patches                    |
| **🏥 Imaging Modality** | Histopathology (H&E-stained whole slide image extracts) |
| **📦 Total Size**       | ~3.25 GB                                                |
| **🏥 Source**           | Harbin Medical University Cancer Hospital               |

#### 🏷️ Classification Task Details

- **Task Type**: Multi-class tissue classification (Tumor Microenvironment analysis)
- **Number of Classes**: 8️⃣
    - 🧈 ADI: Adipose (fat tissue)
    - 🌫️ BACK: Background (non-tissue areas)
    - 🗑️ DEB: Debris (cellular waste)
    - 🛡️ LYM: Lymphocytes (immune cells)
    - 🧴 MUC: Mucus (protective secretion)
    - 💪 MUS: Smooth Muscle (muscle tissue)
    - 🌱 NORM: Normal Colon Mucosa (healthy reference tissue)
    - 🕸️ STR: Cancer-associated Stroma (connective tissue)
    - 🦠 TUM: Tumor (cancerous tissue)

#### 💡 Usage Notes

- ✅ Specifically designed for analyzing the complex tumor microenvironment (TME) in gastric cancer.
- ✅ Includes a companion clinical CSV file linking patches to patient-level metadata (stage, grade, demographics).
- 📚 Recommended to cite the original figshare/Kaggle repository and the associated Nature Scientific Data publication.
- 🔐 License: Creative Commons Attribution 4.0 International (CC BY 4.0).

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                                                                  |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**     | Certain tissue types (e.g., TUM, NORM) may be overrepresented compared to others (e.g., DEB). Apply class weighting or oversampling during training.            |
| **📐 Resolution Variance** | All patches are standardized to 224x224, but verify color distribution as H&E staining can vary across different WSIs.                                          |
| **🧪 Validation Strategy** | Implement patient-aware splitting (group by patient ID in the CSV) to prevent data leakage, as multiple patches originate from the same 300 whole slide images. |

#### 💡 Suggested Preprocessing Pipeline

1. **Metadata Alignment**: Join the image filenames with the `HMU-GC-Clinical.csv` to enable patient-level stratified
   splitting.
2. **Color Normalization**: Apply stain normalization (e.g., Macenko or Vahadane methods) to mitigate H&E staining
   variability across different slides.
3. **Standardize input format**: Ensure all images are loaded as 3-channel RGB tensors and scaled to [0, 1].
4. **Stratified splitting**: Partition the data into train, validation, and test sets, ensuring balanced representation
   of the 8 tissue classes.
5. **Augmentation**: Incorporate rotation, horizontal/vertical flipping, and mild color jittering to improve model
   generalization.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{lou2024gchtid,
  author = {Lou, Shenghan and Ji, Jianxin and Zhang, Xuan and Li, Huiying and Jiang, Yang and Hua, Menglei and Chen, Kexin and Zheng, Xiaohan and Zhang, Qi and Han, Peng and Cao, Lei and Wang, Liuying},
  title = {Gastric Cancer Histopathology Tissue Image Dataset (GCHTID)},
  year = {2024},
  publisher = {figshare},
  doi = {10.6084/m9.figshare.26014469.v1},
  url = {https://doi.org/10.6084/m9.figshare.26014469.v1}
}
```

---

### 👁️ SMDG: Standardized Fundus Glaucoma Dataset

**Study**: Kiefer, R., et al. (2023). A Catalog of Public Glaucoma Datasets for Machine Learning Applications. Kaggle.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                              |
|-------------------------|--------------------------------------------------------------------------------------|
| **📛 Title**            | SMDG, A Standardized Fundus Glaucoma Dataset (SMDG-19)                               |
| **🔗 Source**           | https://www.kaggle.com/datasets/deathtrooper/multichannel-glaucoma-benchmark-dataset |
| **👁️ Target Organ**    | Eye (Retina / Fundus)                                                                |
| **📅 Last Accessed**    | August 13, 2026                                                                      |
| **🎯 Supported Tasks**  | 🏷️ Classification, 🎭 Segmentation                                                  |
| **📐 Image Size**       | 512 × 512 pixels (standardized)                                                      |
| **📁 Data Format**      | PNG (images and segmentation maps), CSV (metadata)                                   |
| **👥 Demographics**     | ✅ Age, Sex (where available in original datasets)                                    |
| **🔄 Train/Test Split** | ❌ Not provided (Exploratory, open-ended benchmark)                                   |

#### 📊 Dataset Composition

| Category                | Details                                                                    |
|-------------------------|----------------------------------------------------------------------------|
| **🖼️ Total Instances** | 12,449 fundus images (aggregated and standardized from 19 public datasets) |
| **🏥 Imaging Modality** | Color Fundus Photography (and some Spectral OCT)                           |
| **📦 Total Size**       | ~3.18 GB                                                                   |
| **🏥 Source**           | Multi-source aggregation (BEH, DRISHTI-GS1, EyePACS-AIROGS, REFUGE1, etc.) |

#### 🏷️ Task Details

- **Classification**:
    - **Number of Classes**: 3️⃣ (0 = Non-Glaucoma, 1 = Glaucoma, -1 = Glaucoma Suspect)
    - **Total Instances**: 12,449
- **Segmentation**:
    - **Optic Cup**: 2,874 instances
    - **Optic Disc**: 3,103 instances
    - **Blood Vessel**: 462 instances

#### 💡 Usage Notes

- ✅ Largest public repository of standardized fundus images with glaucoma labels and multi-channel segmentation maps.
- ✅ Background cropped, centered, padded, and resized to 512x512 to maximize foreground information during machine
  learning processing.
- ✅ Includes rich metadata linking each image to its original source dataset, enabling source-aware domain
  generalization studies.
- 📚 Required to cite the original ICIVC 2023 publication and the Kaggle repository.
- 🔐 License: Other (specified in description; varies by original source dataset, generally CC BY).

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                                                                                                    |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **🧪 Heterogeneity**       | Combines 19 different sources with varying camera types and protocols. Implement domain adaptation or source-aware cross-validation to prevent overfitting to a single dataset's characteristics. |
| **🔍 Class Imbalance**     | Glaucoma Suspect (-1) is a minority class; apply class-weighted loss or focal loss.                                                                                                               |
| **📦 Multi-Task Learning** | Tasks share input images but have independent labels. Design multi-task architectures accordingly, or isolate tasks for single-objective benchmarking.                                            |
| **🔐 Ethical Compliance**  | Dataset contains de-identified clinical imagery; adhere to institutional review requirements for derivative works.                                                                                |

#### 💡 Suggested Preprocessing Pipeline

1. **Parse metadata**: Load `metadata - standardized.csv` to map image filenames to diagnostic labels, segmentation
   paths, and source dataset identifiers.
2. **Standardize input**: Confirm uniform 512×512 dimensions for both fundus images and corresponding segmentation
   masks.
3. **Color normalization**: Apply histogram matching or stain normalization to mitigate inter-dataset color variation.
4. **Augmentation**: Incorporate rotation, flipping, and mild photometric jittering. Ensure segmentation masks are
   transformed identically to the input images.
5. **Stratified splitting**: Partition data by source dataset or patient ID to ensure rigorous evaluation of domain
   generalization.
6. **Evaluation metrics**: Report AUC-ROC and F1-score for classification; compute Dice coefficient and IoU for
   segmentation tasks.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@inproceedings{kiefer2023smdg,
  author = {Kiefer, Riley and Abid, M. and Ardali, M. R. and Steen, J. and Amjadian, E.},
  title = {A Catalog of Public Glaucoma Datasets for Machine Learning Applications: A detailed description and analysis of public glaucoma datasets available to machine learning engineers},
  booktitle = {Proceedings of the 2023 7th International Conference on Information System and Data Mining},
  year = {2023}
}
@dataset{kiefer2023smdgkaggle,
  author = {Kiefer, Riley},
  title = {SMDG, A Standardized Fundus Glaucoma Dataset},
  year = {2023},
  publisher = {Kaggle},
  doi = {10.34740/KAGGLE/DS/2329670},
  url = {https://www.kaggle.com/datasets/deathtrooper/multichannel-glaucoma-benchmark-dataset}
}
```

---

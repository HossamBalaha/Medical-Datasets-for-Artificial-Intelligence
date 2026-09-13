### 🩺 SEED-gastric carcinoma dataset
**Study**: Wang, T. (2021). SEED-gastric carcinoma dataset. Kaggle.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                 |
|-------------------------|-------------------------------------------------------------------------|
| **📛 Title**            | SEED-gastric carcinoma dataset                                          |
| **🔗 Source**           | https://www.kaggle.com/datasets/wangtyi/seedgastric-carcinoma-dataset   |
| **🩺 Target Organ**     | Gastrointestinal Tract (Stomach)                                        |
| **📅 Last Accessed**    | September 11, 2026                                                      |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                                           |
| **📐 Image Size**       | Variable (preprocessed)                                                 |
| **📁 Data Format**      | Images and CSV metadata                                                 |
| **👥 Demographics**     | ❌ Not included                                                          |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                  |

#### 📊 Dataset Composition
| Category                | Details                                                                 |
|-------------------------|-------------------------------------------------------------------------|
| **🖼️ Total Images**    | ~7,081 files (images + metadata)                                        |
| **🔬 Imaging Modality** | Brightfield histopathology (gastric carcinoma tissue)                   |
| **📦 Total Size**       | ~1.24 GB (compressed)                                                   |
| **🏥 Source**           | SEED (Specific institutional or research group source)                  |

#### 🏷️ Classification Task Details
- **Task Type**: Multiclass classification of gastric carcinoma stages
- **Number of Classes**: 2️⃣ (Stage 1, Stage 2)
- **Metadata**: Includes a `train.csv` file linking image identifiers to their respective stage labels.

#### 💡 Usage Notes
- ✅ Provides a focused dataset for distinguishing between different stages of gastric carcinoma.
- ✅ Preprocessed data structure simplifies the initial data loading and parsing steps.
- 📚 Recommended to cite the original Kaggle repository when using this dataset.
- 🔐 License: Unknown (Verify specific terms on Kaggle before commercial use).

#### ⚠️ Usage Considerations
| Aspect                     | Recommendation                                                                     |
|----------------------------|------------------------------------------------------------------------------------|
| **🔍 Limited Documentation**| The source lacks detailed descriptions; perform exploratory data analysis (EDA) to verify label quality and distribution. |
| **🧪 Validation Strategy** | Implement stratified k-fold cross-validation to ensure robust performance estimation given the staging focus. |
| **🔐 Licensing**           | Verify usage terms on Kaggle; assume non-commercial research use unless otherwise stated. |

#### 💡 Suggested Preprocessing Pipeline
1. **Parse metadata**: Load `train.csv` to map image filenames to their corresponding stage labels.
2. **Standardize geometry**: Resize images to uniform dimensions (e.g., 224×224 or 512×512) while preserving aspect ratio.
3. **Color normalization**: Apply stain normalization to mitigate inter-slide H&E staining variability.
4. **Augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering.
5. **Stratified evaluation**: Report per-class precision, recall, F1-score, and AUC-ROC to assess staging accuracy.

#### 📚 Citation
If you use this dataset, please cite:
```bibtex
@dataset{wang2021seedgastric,
  author = {Wang, Tianyi},
  title = {SEED-gastric carcinoma dataset},
  year = {2021},
  publisher = {Kaggle},
  url = {https://www.kaggle.com/datasets/wangtyi/seedgastric-carcinoma-dataset}
}
```

---

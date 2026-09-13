### 🫁 Chest CT-Scan images Dataset (Lung Cancer)
**Study**: Hany, M. (2020). Chest CT-Scan images Dataset. Kaggle.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                 |
|-------------------------|-------------------------------------------------------------------------|
| **📛 Title**            | Chest CT-Scan images Dataset                                            |
| **🔗 Source**           | https://www.kaggle.com/datasets/mohamedhanyyy/chest-ctscan-images       |
| **🫁 Target Organ**     | Lungs / Chest                                                           |
| **📅 Last Accessed**    | September 11, 2026                                                      |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                                           |
| **📐 Image Size**       | Variable (converted to JPG/PNG)                                         |
| **📁 Data Format**      | JPEG/PNG (.jpg/.png)                                                    |
| **👥 Demographics**     | ❌ Not included                                                          |
| **🔄 Train/Test Split** | ✅ Yes (70% Train, 20% Test, 10% Validation)                             |

#### 📊 Dataset Composition
| Category                | Details                                                                 |
|-------------------------|-------------------------------------------------------------------------|
| **🖼️ Total Images**    | 1,000 CT scan images                                                    |
| **🔬 Imaging Modality** | Computed Tomography (CT)                                                |
| **📦 Total Size**       | ~124.96 MB (compressed)                                                 |
| **🏥 Source**           | Aggregated from multiple public medical imaging resources               |

#### 🏷️ Classification Task Details
- **Task Type**: Multiclass classification of chest cancer types and normal tissue
- **Number of Classes**: 4️⃣
  - 🟠 Adenocarcinoma (Most common form, ~30% of cases)
  - 🔴 Large cell carcinoma (Undifferentiated, grows quickly)
  - 🟡 Squamous cell carcinoma (Central lung location, linked to smoking)
  - ✅ Normal (Healthy CT-Scan images)

#### 💡 Usage Notes
- ✅ Pre-organized into `train`, `test`, and `valid` directories, enabling immediate integration with standard deep learning data loaders.
- ✅ Provides a focused benchmark for differentiating between major non-small cell lung cancer (NSCLC) subtypes and healthy tissue.
- 📚 Recommended to cite the original Kaggle repository when using this dataset.
- 🔐 License: Database: Open Database, Contents: © Original Authors.

#### ⚠️ Usage Considerations
| Aspect                     | Recommendation                                                                     |
|----------------------------|------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**     | Verify the exact distribution of the four classes within the train/test splits; apply class weighting if necessary. |
| **📐 Format Conversion**   | Original DICOM files were converted to JPG/PNG; some 3D spatial context and Hounsfield Unit (HU) data may be lost. |
| **🧪 Validation Strategy** | Utilize the provided `valid` set for hyperparameter tuning and the `test` set for final, unbiased performance evaluation. |

#### 💡 Suggested Preprocessing Pipeline
1. **Load directory structure**: Utilize framework-native utilities (e.g., `torchvision.datasets.ImageFolder`) to ingest the labeled subfolders.
2. **Standardize input format**: Convert all images to a consistent color space (single-channel grayscale) and fixed resolution (e.g., 224×224).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard deviation.
4. **Augmentation **(training only): Incorporate rotation, flipping, and intensity jittering to improve model generalization.
5. **Stratified evaluation**: Report per-class precision, recall, F1-score, and a confusion matrix to assess subtype discrimination.

#### 📚 Citation
If you use this dataset, please cite:
```bibtex
@dataset{hany2020chestct,
  author = {Hany, Mohamed},
  title = {Chest CT-Scan images Dataset},
  year = {2020},
  publisher = {Kaggle},
  url = {https://www.kaggle.com/datasets/mohamedhanyyy/chest-ctscan-images}
}
```

---

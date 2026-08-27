### 🎗️ Multi-Cancer Dataset (Ovarian, Skin, Breast, Lung)

**Study**: Fakirde, N. (2026). Multi-Cancer Medical Image Dataset for Deep Learning. Kaggle.  
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                                    |
|-------------------------|--------------------------------------------------------------------------------------------|
| **📛 Title**            | Multi-Cancer Dataset (Ovarian, Skin, Breast, Lung)                                         |
| **🔗 Source**           | https://www.kaggle.com/datasets/namanfakirde/multi-cancer-dataset-ovarian-skin-breast-skin |
| **🫁 Target Organ**     | Ovarian, Skin, Breast, Lung                                                                |
| **📅 Last Accessed**    | August 27, 2026                                                                            |
| **🎯 Supported Tasks**  | 🏷️ Binary & Multi-class Classification                                                    |
| **📐 Image Size**       | Variable (Depends on source dataset)                                                       |
| **📁 Data Format**      | JPEG / PNG (Mixed, depending on source)                                                    |
| **👥 Demographics**     | ❌ Not included                                                                             |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                                     |

#### 📊 Dataset Composition

| Category                | Details                                                          |
|-------------------------|------------------------------------------------------------------|
| **🖼️ Total Images**    | ~43,400 files                                                    |
| **🏥 Imaging Modality** | Histopathology (Breast, Lung, Ovarian), Dermatoscopy (Skin)      |
| **📦 Total Size**       | ~6.78 GB                                                         |
| **🏥 Source**           | Curated aggregation of public datasets (e.g., HAM10000 for Skin) |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification per cancer type, or 8-class multi-class classification
- **Number of Classes**: 8️⃣ (2 per organ system)
    - 🫁 Lung: Benign, Malignant
    - 🎀 Breast: Benign, Malignant
    - 🩸 Ovarian: Benign, Malignant
    - 🖼️ Skin: Benign, Malignant

#### 💡 Usage Notes

- ✅ Provides a unified directory structure compatible with TensorFlow `image_dataset_from_directory` and PyTorch
  `ImageFolder`.
- ✅ Excellent for multi-task learning or evaluating a single model's ability to generalize across different imaging
  modalities (dermatoscopy vs. histopathology).
- 🔐 License: CC BY-NC-SA 4.0 (Non-commercial, share-alike).

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                                                                                    |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Modality Shift**      | Skin cancer images (dermatoscopy) have vastly different visual features compared to histopathology. Avoid training a single model on all 8 classes without modality conditioning. |
| **📐 Resolution Variance** | Source datasets have varying resolutions. Aggressive resizing may distort critical diagnostic features, especially in dermatoscopic images.                                       |
| **🧪 Validation Strategy** | Strictly separate by cancer type during evaluation to measure per-domain accuracy, rather than relying solely on overall macro-average accuracy.                                  |

#### 💡 Suggested Preprocessing Pipeline

1. **Directory Parsing**: Use framework-native tools (e.g., PyTorch `ImageFolder`) to automatically infer labels from
   the nested folder structure.
2. **Modality-Specific Resizing**: Resize histopathology images to 224x224, but consider larger sizes (e.g., 299x299 or
   512x512) for dermatoscopy images to preserve lesion details.
3. **Color Normalization**: Apply histogram matching or CLAHE to standardize lighting conditions, especially for the
   skin cancer subset.
4. **Stratified Splitting**: Split the data ensuring each of the 8 classes is proportionally represented in train,
   validation, and test sets.
5. **Augmentation**: Apply modality-appropriate augmentations (e.g., elastic deformations for histopathology, random
   cropping and color jitter for dermatoscopy).

#### 📚 Citation

If you use this dataset, please cite the curator and the original source datasets (e.g., HAM10000):

```bibtex
@dataset{fakirde2026multicancer,
  author = {Fakirde, Naman},
  title = {Multi-Cancer Dataset (Ovarian, Skin, Breast, Lung)},
  year = {2026},
  publisher = {Kaggle},
  url = {https://www.kaggle.com/datasets/namanfakirde/multi-cancer-dataset-ovarian-skin-breast-skin}
}
```

---

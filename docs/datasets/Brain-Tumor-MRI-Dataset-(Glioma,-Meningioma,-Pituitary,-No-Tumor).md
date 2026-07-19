### 🧠 Brain Tumor MRI Dataset (Glioma, Meningioma, Pituitary, No Tumor)

**Study**: Hira, M. I. K., Hossain, M. S., Bithee, M. M. A., Sara, U. S., Hasan, M. M., Towsif, A. A., & Ahmed, M. K. (
2025). Brain Tumor MRI Dataset (Glioma, Meningioma, Pituitary, No Tumor). Mendeley Data, V4.

[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                           |
|-------------------------|-------------------------------------------------------------------|
| **📛 Title**            | Brain Tumor MRI Dataset (Glioma, Meningioma, Pituitary, No Tumor) |
| **🔗 Source**           | https://data.mendeley.com/datasets/zwr4ntf94j/4                   |
| **🧠 Target Organ**     | Brain                                                             |
| **📅 Last Accessed**    | March 28, 2026                                                    |
| **🎯 Supported Tasks**  | 🏷️ Classification                                                |
| **📐 Image Size**       | Variable (pre-processed; standardized dimensions recommended)     |
| **📁 Data Format**      | JPEG (.jpg) for images                                            |
| **👥 Demographics**     | ❌ Not included                                                    |
| **🔄 Train/Test Split** | ✅ Yes (80% training / 20% testing)                                |

#### 📊 Dataset Composition

| Category                | Details                                                        |
|-------------------------|----------------------------------------------------------------|
| **🖼️ Total Images**    | 12,064 T1-weighted contrast-enhanced MRI scans                 |
| **🏥 Imaging Modality** | T1-weighted contrast-enhanced Magnetic Resonance Imaging (MRI) |
| **🎨 Color Format**     | Grayscale or RGB (scan-dependent)                              |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification
- **Number of Classes**: 4️⃣
    - 🧠 Glioma
    - 🧠 Meningioma
    - 🧠 Pituitary tumor
    - ✅ No tumor (normal)

**📊 Training Set Distribution (80%)**:

| Class         | Image Count |
|---------------|-------------|
| 🧠 Glioma     | 3,018       |
| 🧠 Pituitary  | 2,504       |
| 🧠 Meningioma | 2,183       |
| ✅ No Tumor    | 1,945       |
| **Total**     | **9,650**   |

**📊 Test Set Distribution (20%)**:

| Class         | Image Count |
|---------------|-------------|
| 🧠 Glioma     | 755         |
| 🧠 Pituitary  | 546         |
| 🧠 Meningioma | 626         |
| ✅ No Tumor    | 487         |
| **Total**     | **2,414**   |

#### 💡 Usage Notes

- ✅ Suitable for benchmarking convolutional neural networks (CNNs) and transfer learning architectures
- ✅ Pre-organized directory structure enables direct integration with standard deep learning data loaders
- ✅ Applicable to computer-aided diagnosis (CAD), radiology education, and tumor detection research
- 📚 Recommended to cite the original Mendeley Data repository (DOI: 10.17632/zwr4ntf94j.4) when using this dataset in
  publications

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                     |
|----------------------------|------------------------------------------------------------------------------------|
| **🔍 Class Distribution**  | Moderate imbalance across classes; consider class-weighted loss functions          |
| **🎨 Color Consistency**   | Images may be grayscale or RGB; standardize input channels during preprocessing    |
| **📐 Resolution Variance** | Original scans vary in dimensions; apply uniform resizing prior to training        |
| **🔐 Licensing**           | Distributed under CC BY 4.0; attribution required for redistribution or adaptation |
| **🧪 Validation Strategy** | Use provided train/test split for reproducible benchmarking; avoid data leakage    |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Utilize framework-native dataset utilities (e.g., `torchvision.datasets.ImageFolder`)
   to ingest labeled subfolders.
2. **Standardize input format**: Convert all images to a consistent color space (e.g., single-channel grayscale) and
   fixed resolution (e.g., 224x224 or 256x256).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
4. **Augmentation **(training only): Incorporate rotation, flipping, and intensity jittering to improve model
   generalization.
5. **Stratified evaluation**: Report per-class metrics (precision, recall, F1-score) in addition to overall accuracy to
   assess performance across tumor subtypes.


### 🦴 Osteosarcoma Dataset

**Study**: Upadhyay, G. (2024). Osteosarcoma Dataset. Kaggle.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                         |
|-------------------------|-----------------------------------------------------------------|
| **📛 Title**            | Osteosarcoma Dataset                                            |
| **🔗 Source**           | https://www.kaggle.com/datasets/gauravupadhyay0312/osteosarcoma |
| **🦴 Target Organ**     | Bone                                                            |
| **📅 Last Accessed**    | October 03, 2026                                                |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                                   |
| **📐 Image Size**       | Variable                                                        |
| **📁 Data Format**      | Images (organized in train/test/validate directories)           |
| **👥 Demographics**     | ❌ Not included                                                  |
| **🔄 Train/Test Split** | ✅ Yes (Train, Test, Validate directories provided)              |

#### 📊 Dataset Composition

| Category                | Details                                        |
|-------------------------|------------------------------------------------|
| **🖼️ Total Images**    | 1,048 images                                   |
| **🔬 Imaging Modality** | Medical Imaging (Histopathology / Radiography) |
| **📦 Total Size**       | ~185.76 MB                                     |
| **🏥 Source**           | Kaggle                                         |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of osteosarcoma
- **Number of Classes**: Multiple (Tumor types / grades, as organized in subdirectories)

#### 💡 Usage Notes

- ✅ Pre-organized into `train`, `test`, and `validate` directories for immediate integration with standard deep learning
  data loaders.
- ✅ Suitable for benchmarking convolutional neural networks (CNNs) for bone tumor detection and classification.
- 📚 Recommended to cite the original Kaggle repository when using this dataset.
- 🔐 License: Verify specific terms on the Kaggle dataset page.

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                                    |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Limited Metadata**    | No detailed description is provided on the source page; perform rigorous exploratory data analysis (EDA) to verify label quality. |
| **📐 Resolution Variance** | Images may vary in dimensions; apply uniform resizing and padding prior to model ingestion.                                       |
| **🧪 Validation Strategy** | Utilize the provided split, but verify class balance across all three directories.                                                |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Utilize framework-native utilities (e.g., `torchvision.datasets.ImageFolder`) to ingest
   labeled subfolders.
2. **Exploratory Analysis**: Visually inspect a random sample of images to understand the modality, quality, and
   labeling consistency.
3. **Standardize input format**: Convert all images to a consistent color space and fixed resolution (e.g., 224×224).
4. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
5. **Augmentation **(training only): Incorporate rotation, flipping, and intensity jittering to improve model
   generalization.
6. **Stratified evaluation**: Report per-class metrics (precision, recall, F1-score) to assess performance across tumor
   subtypes.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{upadhyay2024osteosarcoma,
    author = {Upadhyay, Gaurav},
    title = {Osteosarcoma},
    year = {2024},
    publisher = {Kaggle},
    url = {https://www.kaggle.com/datasets/gauravupadhyay0312/osteosarcoma}
}
```

---

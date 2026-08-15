### 🫁 Atelectasis

**Study**: AIT, A. (2021). Atelectasis. Kaggle.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                  |
|-------------------------|----------------------------------------------------------|
| **📛 Title**            | Atelectasis                                              |
| **🔗 Source**           | https://www.kaggle.com/datasets/adnanenasser/atelectasis |
| **🫁 Target Organ**     | Lungs / Chest                                            |
| **📅 Last Accessed**    | August 13, 2026                                          |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification                                |
| **📐 Image Size**       | Variable                                                 |
| **📁 Data Format**      | JPEG (.jpg)                                              |
| **👥 Demographics**     | ❌ Not included                                           |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)   |

#### 📊 Dataset Composition

| Category                | Details                                         |
|-------------------------|-------------------------------------------------|
| **🖼️ Total Images**    | 2,571 files                                     |
| **🏥 Imaging Modality** | Radiographic X-ray (Frontal chest views)        |
| **📦 Total Size**       | ~213.53 MB                                      |
| **🏥 Source**           | Aggregated from public chest X-ray repositories |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification
- **Number of Classes**: 2️⃣
    - 🫁 Atelectasis (Collapsed lung tissue)
    - ✅ Normal (or Other non-atelectasis conditions, depending on the negative class formulation)

#### 💡 Usage Notes

- ✅ Focused dataset for detecting atelectasis, a common finding in chest radiographs that can mimic or co-occur with
  other pathologies.
- ✅ Lightweight size makes it suitable for quick experimentation and algorithmic prototyping.
- 📚 Recommended to cite the original Kaggle repository.
- 🔐 License: Unknown (Verify specific terms on the Kaggle dataset page before commercial use).

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                                                                         |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Limited Metadata**    | No detailed description or predefined split is provided on the source page. Perform rigorous exploratory data analysis (EDA) to verify label quality and distribution. |
| **📐 Resolution Variance** | Images vary in dimensions; apply uniform resizing and padding prior to model ingestion.                                                                                |
| **🧪 Validation Strategy** | Implement patient-aware or source-aware partitioning to prevent data leakage, as the provenance of the images is not explicitly detailed.                              |

#### 💡 Suggested Preprocessing Pipeline

1. **Exploratory Analysis**: Visually inspect a random sample of images to understand the quality, resolution, and
   labeling consistency.
2. **Standardize input format**: Convert all images to a consistent color space (single-channel grayscale) and fixed
   resolution (e.g., 224x224).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
4. **Stratified splitting**: Partition the data into train, validation, and test sets, ensuring balanced representation
   of the target class.
5. **Augmentation**: Incorporate rotation, flipping, and intensity jittering to improve model generalization.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{ait2021atelectasis,
  author = {AIT, Adnane},
  title = {Atelectasis},
  year = {2021},
  publisher = {Kaggle},
  url = {https://www.kaggle.com/datasets/adnanenasser/atelectasis}
}
```

---

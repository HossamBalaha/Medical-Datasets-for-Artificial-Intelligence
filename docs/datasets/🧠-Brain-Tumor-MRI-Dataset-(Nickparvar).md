### 🧠 Brain Tumor MRI Dataset (Nickparvar)

**Author**: Masoud Nickparvar. Kaggle Dataset.
[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                  |
|-------------------------|--------------------------------------------------------------------------|
| **📛 Title**            | Brain Tumor MRI Dataset                                                  |
| **🔗 Source**           | https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset |
| **🧠 Target Organ**     | Brain                                                                    |
| **📅 Last Accessed**    | July 19, 2026                                                            |
| **🎯 Supported Tasks**  | 🏷️ Classification                                                       |
| **📐 Image Size**       | Variable (preprocessing recommended)                                     |
| **📁 Data Format**      | JPEG/PNG images organized in class-labeled directories                   |
| **👥 Demographics**     | ❌ Not included                                                           |
| **🔄 Train/Test Split** | ✅ Yes (5,600 Training / 1,600 Testing)                                   |

#### 📊 Dataset Composition

| Category                | Details                                                                               |
|-------------------------|---------------------------------------------------------------------------------------|
| **🖼️ Total Images**    | 7,200 human brain MRI images                                                          |
| **🏥 Imaging Modality** | Magnetic Resonance Imaging (MRI)                                                      |
| **📦 Total Size**       | ~167.85 MB (Testing set) + Training set                                               |
| **📦 Data Sources**     | Curated combination of figshare brain MRI dataset, SARTAJ dataset, and Br35H dataset. |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification
- **Number of Classes**: 4️⃣
    - 🧠 Glioma
    - 🧠 Meningioma
    - 🧠 Pituitary tumor
    - ✅ No tumor (Normal)

**📊 Dataset Distribution**:
| Split | Glioma | Meningioma | Pituitary | No Tumor | Total |
|---------------|--------|------------|-----------|----------|-------|
| **Training**  | 1,400 | 1,400 | 1,400 | 1,400 | 5,600 |
| **Testing**   | 400 | 400 | 400 | 400 | 1,600 |
| **Total**     | 1,800 | 1,800 | 1,800 | 1,800 | 7,200 |

#### 💡 Usage Notes

- ✅ Perfectly balanced classes (1,400 train / 400 test per class) prevent bias during training.
- ✅ Overlap between training and testing sets has been explicitly eliminated to prevent data leakage (Version 2 update).
- ✅ Inconsistent glioma images from the original SARTAJ dataset were removed and replaced with verified images from the
  figshare dataset to improve label reliability.
- 📚 Recommended to cite the original Kaggle dataset when using this data in publications.
- 🔐 License: Attribution 4.0 International (CC BY 4.0)

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                 |
|----------------------------|----------------------------------------------------------------------------------------------------------------|
| **📐 Resolution Variance** | Image sizes vary across the dataset; uniform resizing is required prior to training.                           |
| **🎨 Preprocessing**       | Margin removal, normalization, and resizing are highly recommended to significantly improve model performance. |
| **🧪 Validation Strategy** | Use the provided train/test split for reproducible benchmarking; avoid reshuffling across the split boundary.  |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Utilize framework-native dataset utilities (e.g., `torchvision.datasets.ImageFolder`)
   to ingest labeled subfolders.
2. **Standardize input format**: Convert all images to a consistent color space (e.g., single-channel grayscale or RGB)
   and fixed resolution (e.g., 224×224).
3. **Margin removal **(optional): Crop or remove black margins from MRI scans to focus the model's attention on the
   brain region.
4. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
5. **Augmentation **(training only): Incorporate rotation, flipping, and intensity jittering to improve model
   generalization.
6. **Stratified evaluation**: Report per-class metrics (precision, recall, F1-score) in addition to overall accuracy to
   assess performance across all four categories.

---

## 🤝 How to Contribute or Request a Dataset

- ➕ **Add a Dataset**: Submit a pull request with dataset metadata following the structure above.
- 🐛 **Report Issues**: Use the GitHub Issues tab to flag broken links, metadata errors, or accessibility concerns.
- 💡 **Suggest New Datasets**: Open an issue with the dataset name, DOI/link, tasks, and brief description.

---

## ⚖️ License and Ethical Use

- 📜 All datasets included in this repository are subject to the licenses and terms of use specified by their original
  publishers.
- 🛡️ Users are responsible for ensuring compliance with ethical guidelines, institutional review board (IRB)
  requirements, and data usage agreements applicable to their research context.
- 🔗 This repository does not host raw data files; it provides curated metadata and direct links to authoritative
  sources.

---

## 📚 Citation

If you use this repository or any of its listed datasets in your research, please cite both:

1. 🔗 The original dataset source (e.g., the Figshare DOI above)
2. 📦 This repository (citation details to be added upon formal release)

---

## 📬 Contact

This repository is prepared by `Hossam Magdy Balaha`. For any questions or inquiries, please contact me using the
contact information available on my CV at the following
link: https://hossambalaha.github.io/

*🕒 Last Updated: July 19, 2026*

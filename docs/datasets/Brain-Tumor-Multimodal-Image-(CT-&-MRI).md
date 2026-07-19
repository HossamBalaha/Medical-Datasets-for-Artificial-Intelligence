### 🧠 Brain Tumor Multimodal Image (CT & MRI)

**Author**: Md. Golam Murtoza. Kaggle Dataset.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                               |
|-------------------------|---------------------------------------------------------------------------------------|
| **📛 Title**            | Brain tumor multimodal image (CT & MRI)                                               |
| **🔗 Source**           | https://www.kaggle.com/datasets/murtozalikhon/brain-tumor-multimodal-image-ct-and-mri |
| **🧠 Target Organ**     | Brain                                                                                 |
| **📅 Last Accessed**    | July 19, 2026                                                                         |
| **🎯 Supported Tasks**  | 🏷️ Classification, 🎭 Segmentation                                                   |
| **📐 Image Size**       | Variable (high-resolution CT and MRI scans)                                           |
| **📁 Data Format**      | Images (organized in CT and MRI subdirectories)                                       |
| **👥 Demographics**     | ❌ Not included                                                                        |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                                |

#### 📊 Dataset Composition

| Category                | Details                                                                 |
|-------------------------|-------------------------------------------------------------------------|
| **🖼️ Total Images**    | 9,620 files (across CT and MRI directories)                             |
| **🏥 Imaging Modality** | Computed Tomography (CT) and Magnetic Resonance Imaging (MRI)           |
| **📦 Total Size**       | ~394.67 MB (compressed)                                                 |
| **📦 Data Sources**     | Curated from multiple public sources (Roboflow, Kaggle, Mendeley, etc.) |

#### 🏷️ Classification & Segmentation Task Details

- **Task Type**: Multiclass classification and segmentation of brain tumors
- **Number of Classes**: Multiple (e.g., Glioma, Meningioma, etc., depending on the source subset)
- **Modality Synergy**: Combines CT scans (for clear bone structure visualization) and MRI scans (for detailed soft
  tissue analysis) to enable comprehensive tumor detection.

#### 💡 Usage Notes

- ✅ Suitable for benchmarking multimodal deep learning frameworks that fuse CT and MRI features.
- ✅ Provides a diverse collection of high-resolution scans for robust model training.
- 📚 Recommended to cite the original Kaggle dataset and acknowledge the constituent source datasets when using this data
  in publications.
- 🔐 License: CC BY-NC-SA 4.0

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                                      |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Data Heterogeneity**  | Sourced from multiple platforms; expect variations in resolution, contrast, and formatting.                                         |
| **📐 Resolution Variance** | Apply uniform resizing and normalization prior to model ingestion.                                                                  |
| **🧪 Validation Strategy** | Implement patient-aware or source-aware partitioning to prevent data leakage, as the dataset is an aggregation of multiple sources. |

#### 💡 Suggested Preprocessing Pipeline

1. **Separate modalities**: Isolate CT and MRI directories to apply modality-specific preprocessing if required by your
   architecture.
2. **Standardize input format**: Convert all images to a consistent color space (e.g., single-channel grayscale) and
   fixed resolution (e.g., 224×224 or 256×256).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
4. **Augmentation **(training only): Incorporate rotation, flipping, and intensity jittering to improve model
   generalization across varied source domains.
5. **Stratified evaluation**: Report per-class metrics (precision, recall, F1-score) to assess performance across
   different tumor subtypes and imaging modalities.

---


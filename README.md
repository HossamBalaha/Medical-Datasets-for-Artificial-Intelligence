# Medical AI Datasets Repository

## 📋 Dataset Summary

| Dataset                                                                                                                                          | Organ         | Tasks                                                | Classes                                                                           | Split            | Last Accessed   | Quick Link                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------|-----------------------------------------------------------------------------------|------------------|-----------------|----------------------------------------------------------------------|
| [🧠 BRISC 2025: Brain Tumor Segmentation & Classification](#-brisc-2025-annotated-dataset-for-brain-tumor-image-segmentation-and-classification) | 🧠 Brain      | 🏷️ Classification, 🎭 Segmentation                  | 4️⃣ Multiclass (Classification) / ⚪⚫ Binary (Segmentation)                        | ✅ Train/Test     | 📅 Mar 28, 2026 | [🔗 Source](https://www.kaggle.com/datasets/briscdataset/brisc2025/) |
| [🧠 Brain Tumor MRI Dataset](#-brain-tumor-mri-dataset-glioma-meningioma-pituitary-no-tumor)                                                     | 🧠 Brain      | 🏷️ Classification                                   | 4️⃣ Multiclass (Glioma, Meningioma, Pituitary, No Tumor)                          | ✅ Train/Test     | 📅 Mar 28, 2026 | [🔗 Source](https://data.mendeley.com/datasets/zwr4ntf94j/4)         |
| [🦴 BTXRD: Bone Tumor X-ray Radiograph Dataset](#-btxrd-bone-tumor-x-ray-radiograph-dataset)                                                     | 🦴 Bone       | 🏷️ Classification, 🎭 Segmentation, 📍 Localization | Multiple (see details)                                                            | ❌ No split       | 📅 Mar 28, 2026 | [🔗 Source](https://doi.org/10.6084/m9.figshare.27865398)            |
| [🔬 Dartmouth Kidney Cancer Histology Dataset](#-dartmouth-kidney-cancer-histology-dataset)                                                      | 🫘 Kidney     | 🏷️ Classification                                   | 4️⃣ Multiclass (Renal Oncocytoma, Chromophobe RCC, Clear cell RCC, Papillary RCC) | ✅ Train/Val/Test | 📅 Apr 11, 2026 | [🔗 Source](https://bmirds.github.io/KidneyCancer/)                  |
| [🔬 CRC-HGD-v1: Colorectal Cancer Histopathological Grading Dataset](#-crc-hgd-v1-colorectal-cancer-histopathological-grading-dataset)           | 🦴 Colorectal | 🏷️ Classification (Grading)                         | 3️⃣ Ordinal Multiclass (Grade I, Grade II, Grade III)                             | ❌ No split       | 📅 Apr 11, 2026 | [🔗 Source](https://data.mendeley.com/datasets/yfp5sfj47m/2)         |

> **ℹ️ Note**: This repository is under active development. Additional datasets will be incorporated over time. Click
> any dataset name above to navigate to its detailed section.

---

## 🌐 Overview

This repository serves as a curated collection of medical datasets designed to support artificial intelligence research
and development in healthcare. It provides researchers, developers, and practitioners with streamlined access to
high-quality, task-specific medical imaging datasets for classification, segmentation, localization, and other AI-driven
applications.

---

## 🗂️ Dataset Details

### 🧠 BRISC 2025: Annotated Dataset for Brain Tumor Image Segmentation and Classification

**Study**: Fateh, A., Rezvani, Y., Moayedi, S., Rezvani, S., Fateh, F., Fateh, M., & Abolghasemi, V. (2026). BRISC:
Annotated dataset for brain tumor segmentation and classification. Scientific Data.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                             |
|-------------------------|-------------------------------------------------------------------------------------|
| **📛 Title**            | BRISC 2025: Annotated Dataset for Brain Tumor Image Segmentation and Classification |
| **🔗 Source**           | https://www.kaggle.com/datasets/briscdataset/brisc2025/                             |
| **🧠 Target Organ**     | Brain                                                                               |
| **📅 Last Accessed**    | March 28, 2026                                                                      |
| **🎯 Supported Tasks**  | 🏷️ Classification, 🎭 Segmentation                                                 |
| **📐 Image Size**       | 512 x 512 pixels                                                                    |
| **📁 Data Format**      | JPG (.jpg) for images, PNG (.png) for masks                                         |
| **👥 Demographics**     | ❌ Not included                                                                      |
| **🔄 Train/Test Split** | ✅ Yes                                                                               |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification
- **Number of Classes**: 4️⃣
    - 🧠 Glioma
    - 🧠 Meningioma
    - ✅ No tumor
    - 🧠 Pituitary tumor

**📊 Training Set Distribution**:

- 🧠 Glioma: 1,147 images
- 🧠 Meningioma: 1,329 images
- ✅ No tumor: 1,067 images
- 🧠 Pituitary: 1,457 images

**📊 Test Set Distribution**:

- 🧠 Glioma: 254 images
- 🧠 Meningioma: 306 images
- ✅ No tumor: 140 images
- 🧠 Pituitary: 300 images

#### 🎭 Segmentation Task Details

- **Task Type**: Binary segmentation (tumor vs. background)
- **Mask Format**: ⚪ White-on-⚫ Black binary masks

**📊 Training Set**:

- 🖼️ Images: 3,933
- 🎭 Corresponding Masks: 3,933
- 📁 Organization: Separated folders for images and masks

**📊 Test Set**:

- 🖼️ Images: 860
- 🎭 Corresponding Masks: 860
- 📁 Organization: Separated folders for images and masks

#### 💡 Usage Notes

- ✅ Suitable for benchmarking multi-task learning frameworks
- ✅ Compatible with standard deep learning pipelines for medical imaging
- 📚 Recommended to cite the original Figshare repository when using this dataset in publications

---

### 🧠 Brain Tumor MRI Dataset (Glioma, Meningioma, Pituitary, No Tumor)

**Study**: Hira, M. I. K., Hossain, M. S., Bithee, M. M. A., Sara, U. S., Hasan, M. M., Towsif, A. A., & Ahmed, M. K. (
2025). Brain Tumor MRI Dataset (Glioma, Meningioma, Pituitary, No Tumor). Mendeley Data, V4.

[🔝 Back to Summary](#-dataset-summary)

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

### 🦴 BTXRD: Bone Tumor X-ray Radiograph Dataset

**Study**: Yao, S., Huang, Y., Wang, X., Zhang, Y., Paixao, I. C., Wang, Z., ... & Song, J. (2025). A radiograph dataset
for the Classification, Localization, and segmentation of primary bone tumors. Scientific data, 12(1), 88.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                              |
|-------------------------|----------------------------------------------------------------------|
| **📛 Title**            | BTXRD: Bone Tumor X-ray Radiograph Dataset                           |
| **🔗 Source**           | https://doi.org/10.6084/m9.figshare.27865398                         |
| **🦴 Target Organ**     | Bone (appendicular and axial skeleton)                               |
| **📅 Last Accessed**    | March 28, 2026                                                       |
| **🎯 Supported Tasks**  | 🏷️ Classification, 🎭 Segmentation, 📍 Localization                 |
| **📐 Image Size**       | Different sizes (to be standardized)                                 |
| **📁 Data Format**      | JPEG (.jpeg) for images, LabelMe-format JSON (.json) annotations     |
| **👥 Demographics**     | ✅ Age (3-88 yrs), Gender (M/F), Imaging center (inside dataset.xlsx) |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)               | 

#### 📊 Dataset Composition

| Category               | Details                                                              |
|------------------------|----------------------------------------------------------------------|
| **🖼️ Total Images**   | 3,746 radiographs (IMG000001-IMG003746)                              |
| **🏥 Imaging Centers** | 3 contributing institutions (coded as `center`: 1, 2, 3)             |
| **🧒 Age Range**       | 1-88 years (pediatric to geriatric coverage)                         |
| **⚧ Gender Balance**   | Both Male (M) and Female (F); distribution requires full enumeration |

#### 🦴 Anatomical Coverage

| Region          | Structures Included                                |
|-----------------|----------------------------------------------------|
| **Upper Limb**  | Humerus, Radius, Ulna, Shoulder/Elbow/Wrist joints |
| **Lower Limb**  | Femur, Tibia, Fibula, Foot, Hip/Knee/Ankle joints  |
| **Pelvis**      | Hip bone, Hip joint                                |
| **View Angles** | Frontal, Lateral, Oblique projections              |

#### 🎗️ Tumor Annotation Schema

| Label Category      | Specific Classes                                                                                                                         |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| **Malignancy**      | `benign`, `malignant`, `tumor` (binary/multi-label flags)                                                                                |
| **Benign Types**    | Osteochondroma, Multiple osteochondromas, Simple bone cyst, Giant cell tumor, Osteofibroma, Synovial osteochondroma, Other benign tumors |
| **Malignant Types** | Osteosarcoma, Other malignant tumors (`other mt`)                                                                                        |

#### 🗂️ Annotation Format (LabelMe JSON)

```json
{
  "version": "5.4.1",
  "shapes": [
    {
      "label": "other mt",
      "shape_type": "polygon",
      "points": [
        [
          x1,
          y1
        ],
        [
          x2,
          y2
        ],
        ...
      ],
      "group_id": null
    },
    {
      "label": "other mt",
      "shape_type": "rectangle",
      "points": [
        [
          x_min,
          y_min
        ],
        [
          x_max,
          y_max
        ]
      ]
    }
  ],
  "imagePath": "IMG000001.jpeg",
  "imageWidth": 3213,
  "imageHeight": 2397
}
```

#### ⚠️ Usage Considerations

| Aspect                       | Recommendation                                                                     |
|------------------------------|------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**       | Malignant cases (e.g., osteosarcoma) are rarer; apply stratified sampling          |
| **🧭 Multi-label Cases**     | Images may contain multiple tumor types or anatomical regions; handle accordingly  |
| **📐 Spatial Normalization** | Raw images vary in resolution; resize/normalize before model ingestion             |
| **🔐 Ethical Compliance**    | Dataset contains patient-derived data; adhere to institutional review requirements |
| **🧪 Baseline Splits**       | Consider center-stratified or age-stratified splits to ensure generalizability     |

#### 💡 Suggested Preprocessing Pipeline

1. **Parse metadata**: Load `dataset.xlsx` to extract demographic and label information per `image_id`.
2. **Link annotations**: Match each JPEG with its corresponding LabelMe JSON for segmentation masks.
3. **Standardize geometry**: Resize images to a fixed resolution (e.g., 512x512 or 1024x1024) while preserving aspect
   ratio.
4. **Encode labels**: Convert one-hot or multi-hot vectors for classification; rasterize polygons for segmentation
   masks.
5. **Stratify splits**: Partition data by center, age group, or tumor type to mitigate domain shift.

---

### 🔬 Dartmouth Kidney Cancer Histology Dataset

**Study**: Zhu, M., Ren, B., Richards, R., Suriawinata, M., Tomita, N., & Hassanpour, S. (2021). Development and
Evaluation of a Deep Neural Network for Histologic Classification of Renal Cell Carcinoma on Biopsy and Surgical
Resection Slides. *Scientific Reports*, 11, 7080.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                 |
|-------------------------|-------------------------------------------------------------------------|
| **📛 Title**            | Dartmouth Kidney Cancer Histology Dataset                               |
| **🔗 Source**           | https://bmirds.github.io/KidneyCancer/                                  |
| **🫘 Target Organ**     | Kidney (Renal)                                                          |
| **📅 Last Accessed**    | April 11, 2026                                                          |
| **🎯 Supported Tasks**  | 🏷️ Classification                                                      |
| **📐 Image Size**       | Variable (WSIs downsampled to 5x magnification from original 20x scans) |
| **📁 Data Format**      | PNG (.png) for whole-slide images; CSV (.csv) for metadata              |
| **👥 Demographics**     | ❌ Not included (de-identified per IRB approval)                         |
| **🔄 Train/Test Split** | ✅ Yes (provided in MetaData.csv)                                        |

#### 📊 Dataset Composition

| Category                | Details                                                                    |
|-------------------------|----------------------------------------------------------------------------|
| **🖼️ Total Images**    | 563 whole-slide images (H&E-stained FFPE tissue sections)                  |
| **🏥 Imaging Modality** | Brightfield histopathology (Hematoxylin & Eosin stain)                     |
| **🔬 Scanner**          | Aperio AT2 whole-slide scanner (original 20x; converted to 5x via libvips) |
| **📦 File Structure**   | 11 ZIP archives (DHMC_wsi_01.zip - DHMC_wsi_11.zip) + MetaData.csv         |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of renal cell carcinoma subtypes
- **Number of Classes**: 4️⃣
    - 🟠 Renal Oncocytoma
    - 🟣 Chromophobe RCC
    - 🔵 Clear cell RCC
    - 🟢 Papillary RCC

**📊 Slide Distribution by Type**:

| Slide Type         | Slide IDs | Archive File       | Approx. Size |
|--------------------|-----------|--------------------|--------------|
| Surgical Resection | 001-484   | DHMC_wsi_01-10.zip | ~85.8 GB     |
| Biopsy (Test Set)  | 485-563   | DHMC_wsi_11.zip    | ~4.7 GB      |
| **Metadata**       | All 563   | MetaData.csv       | —            |

**📋 Metadata Contents** (`MetaData.csv`):

- Slide identifier
- Histologic class label
- Slide type (resection/biopsy)
- Dataset split assignment (train/validation/test)

#### 💡 Usage Notes

- ✅ Suitable for benchmarking deep learning models for whole-slide image classification
- ✅ Includes both resection and biopsy specimens for domain generalization studies
- ✅ Pre-defined train/validation/test splits enable reproducible evaluation
- 📚 Required to cite the original *Scientific Reports* publication when using this dataset
- 🔐 Access requires completion of a Research Use Agreement (non-commercial use only)

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                         |
|----------------------------|------------------------------------------------------------------------------------------------------------------------|
| **🔐 Access Protocol**     | Dataset requires form submission; download links expire after 4 hours                                                  |
| **⚖️ Licensing**           | Non-commercial research use only; redistribution prohibited without permission                                         |
| **🔍 Class Distribution**  | Verify class balance via MetaData.csv; consider stratified sampling if needed                                          |
| **📐 Resolution Handling** | Images are downsampled to 5x; account for magnification in model architecture                                          |
| **🧪 Domain Shift**        | Biopsy slides (DHMC_wsi_11.zip) may exhibit different characteristics than resection slides; evaluate generalizability |

#### 💡 Suggested Preprocessing Pipeline

1. **Request access**: Complete the registration form at the source URL to receive download links.
2. **Parse metadata**: Load `MetaData.csv` to map slide identifiers to labels and dataset splits.
3. **Organize data**: Extract ZIP archives into structured directories (e.g., by split or class).
4. **Patch extraction **(optional): For memory-efficient training, extract fixed-size patches from WSIs using libraries
   such as `OpenSlide` or `libvips`.
5. **Normalization**: Apply stain normalization (e.g., Macenko or Vahadane methods) to mitigate inter-slide variability.
6. **Augmentation**: Incorporate rotation, flipping, and color jittering to improve model robustness.
7. **Evaluation**: Report per-subtype metrics (precision, recall, F1-score) alongside overall accuracy.

#### 🔗 Associated Resources

- **Code Repository**: [DeepSlide](https://github.com/hassanpourlab/DeepSlide) - PyTorch framework for WSI
  classification
- **Related Datasets**: [Dartmouth Lung Cancer Histology Dataset](https://bmirds.github.io/LungCancer/) (same research
  group)
- **Contact**: 📧 BMIRDS team via the contact form on the dataset homepage

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{zhu2021development,
  title={Development and evaluation of a deep neural network for histologic classification of renal cell carcinoma on biopsy and surgical resection slides},
  author={Zhu, Mengdan and Ren, Bing and Richards, Ryland and Suriawinata, Matthew and Tomita, Naofumi and Hassanpour, Saeed},
  journal={Scientific Reports},
  volume={11},
  number={1},
  pages={7080},
  year={2021},
  publisher={Nature Publishing Group UK London}
  doi={10.1038/s41598-021-86747-7}
}
```

---

### 🔬 CRC-HGD-v1: Colorectal Cancer Histopathological Grading Dataset

**Study**: Amjadi, E., Bahreini, A., Hakimian, S. M., Emami, M. H., Fahim, A., Rahimi, H., & Bolhasani, H. (2024).
CRC-HGD-v1: A Histopathological Image Dataset for Grading Colorectal Cancer. *Mendeley Data*, V2.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                         |
|-------------------------|-----------------------------------------------------------------|
| **📛 Title**            | CRC-HGD-v1: Colorectal Cancer Histopathological Grading Dataset |
| **🔗 Source**           | https://data.mendeley.com/datasets/yfp5sfj47m/2                 |
| **🦴 Target Organ**     | Colorectal / Colon                                              |
| **📅 Last Accessed**    | April 11, 2026                                                  |
| **🎯 Supported Tasks**  | 🏷️ Classification (Ordinal Grading)                            |
| **📐 Image Size**       | Variable (multi-magnification: 4x, 10x, 20x, 40x)               |
| **📁 Data Format**      | Image files (format unspecified; typical: JPG/PNG)              |
| **👥 Demographics**     | ❌ Not included                                                  |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)          |

#### 📊 Dataset Composition

| Category                    | Details                                                  |
|-----------------------------|----------------------------------------------------------|
| **🖼️ Total Images**        | 1,899 histopathological images                           |
| **🔬 Imaging Modality**     | Brightfield histopathology (H&E-stained tissue sections) |
| **🔍 Magnification Levels** | 4x, 10x, 20x, 40x (multi-scale coverage)                 |
| **📦 Total Size**           | ~457 MB (compressed)                                     |
| **🏥 Curation**             | Poursina-Hakim Digestive Disease Research Center (PDDRC) |

#### 🏷️ Classification Task Details

- **Task Type**: Ordinal multiclass classification (tumor grading)
- **Number of Classes**: 3️⃣
    - 🟢 Grade I: Well Differentiated
    - 🟡 Grade II: Moderately Differentiated
    - 🔴 Grade III: Poorly Differentiated

**📊 Specimen-Level Distribution**:

| Grade     | Description               | Specimens | Images (All Magnifications) |
|-----------|---------------------------|-----------|-----------------------------|
| I         | Well Differentiated       | 103       | 860                         |
| II        | Moderately Differentiated | 75        | 712                         |
| III       | Poorly Differentiated     | 32        | 327                         |
| **Total** | —                         | **210**   | **1,899**                   |

**🔬 Multi-Magnification Sampling Protocol**:

- Per specimen: ~10 images total
    - 1 image at 4x magnification
    - 3 images at 10x magnification
    - 3 images at 20x magnification
    - 3 images at 40x magnification

#### 💡 Usage Notes

- ✅ Suitable for benchmarking ordinal classification and multi-scale learning architectures
- ✅ Multi-magnification design supports research on resolution-aware feature extraction
- ✅ Expert-curated labels under pathology supervision enhance annotation reliability
- 📚 Required to cite the original Mendeley Data repository (DOI: 10.17632/yfp5sfj47m.2) in publications
- 🔗 For dataset updates or inquiries, visit: https://databiox.com (as noted by the authors)

#### ⚠️ Usage Considerations

| Aspect                        | Recommendation                                                                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**        | Grade III (Poorly Differentiated) is underrepresented; consider stratified sampling or class-weighted loss |
| **🔬 Magnification Handling** | Images span 4x-40x; either process magnifications separately or normalize resolution prior to training     |
| **🧪 Ordinal Nature**         | Grades represent an ordered severity scale; consider ordinal regression or monotonic loss functions        |
| **🔐 Licensing**              | Verify usage terms on Mendeley Data; attribution required for redistribution                               |
| **🧭 Domain Generalization**  | Single-center curation may limit external validity; validate on independent cohorts when possible          |

#### 💡 Suggested Preprocessing Pipeline

1. **Organize directory structure**: Group images by grade and magnification level for efficient data loading.
2. **Standardize resolution**: Resize images to a uniform dimension (e.g., 224x224 or 512x512) while preserving aspect
   ratio.
3. **Color normalization**: Apply stain normalization (e.g., Macenko method) to reduce inter-slide variability.
4. **Magnification-aware augmentation**: Apply rotation, flipping, and intensity adjustments; avoid operations that
   distort histological features.
5. **Stratified splitting**: Partition data by specimen (not image) to prevent data leakage across train/test sets.
6. **Ordinal encoding**: Encode grades as ordered integers (0, 1, 2) or use one-hot vectors with ordinal constraints.
7. **Evaluation metrics**: Report per-class precision/recall alongside ordinal-aware metrics (e.g., weighted kappa, mean
   absolute error).

#### 🔗 Associated Resources

- **Dataset Homepage**: https://data.mendeley.com/datasets/yfp5sfj47m/2
- **Query Portal**: https://databiox.com (for updates and support)
- **Related Work**: Consider cross-referencing with other colorectal histopathology datasets (e.g., CRC-VAL-HE-7K,
  PatchGastricADC22)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{amjadi2024crchgd,
  author = {Amjadi, Elham and Bahreini, Amin and Hakimian, Sayyed Mohammadreza and Emami, Mohammad Hasan and Fahim, Alireza and Rahimi, Hojjatollah and Bolhasani, Hamidreza},
  title = {CRC-HGD-v1: A Histopathological Image Dataset for Grading Colorectal Cancer},
  year = {2024},
  publisher = {Mendeley Data},
  version = {2},
  doi = {10.17632/yfp5sfj47m.2},
  url = {https://data.mendeley.com/datasets/yfp5sfj47m/2}
}
```

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

*🕒 Last Updated: April 11, 2026*

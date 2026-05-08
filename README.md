# Medical AI Datasets Repository

## 📋 Dataset Summary

| Dataset                                                                                                                                               | Organ                     | Tasks                                                | Classes                                                                                                                  | Split                                      | Last Accessed   | Quick Link                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|-----------------|-----------------------------------------------------------------------------------------------------|
| [🧠 BRISC 2025: Brain Tumor Segmentation & Classification](#-brisc-2025-annotated-dataset-for-brain-tumor-image-segmentation-and-classification)      | 🧠 Brain                  | 🏷️ Classification, 🎭 Segmentation                  | 4️⃣ Multiclass (Classification) / ⚪⚫ Binary (Segmentation)                                                               | ✅ Train/Test                               | 📅 Mar 28, 2026 | [🔗 Source](https://www.kaggle.com/datasets/briscdataset/brisc2025/)                                |
| [🧠 Brain Tumor MRI Dataset](#-brain-tumor-mri-dataset-glioma-meningioma-pituitary-no-tumor)                                                          | 🧠 Brain                  | 🏷️ Classification                                   | 4️⃣ Multiclass (Glioma, Meningioma, Pituitary, No Tumor)                                                                 | ✅ Train/Test                               | 📅 Mar 28, 2026 | [🔗 Source](https://data.mendeley.com/datasets/zwr4ntf94j/4)                                        |
| [🦴 BTXRD: Bone Tumor X-ray Radiograph Dataset](#-btxrd-bone-tumor-x-ray-radiograph-dataset)                                                          | 🦴 Bone                   | 🏷️ Classification, 🎭 Segmentation, 📍 Localization | Multiple (see details)                                                                                                   | ❌ No split                                 | 📅 Mar 28, 2026 | [🔗 Source](https://doi.org/10.6084/m9.figshare.27865398)                                           |
| [🔬 Dartmouth Kidney Cancer Histology Dataset](#-dartmouth-kidney-cancer-histology-dataset)                                                           | 🫘 Kidney                 | 🏷️ Classification                                   | 4️⃣ Multiclass (Renal Oncocytoma, Chromophobe RCC, Clear cell RCC, Papillary RCC)                                        | ✅ Train/Val/Test                           | 📅 Apr 11, 2026 | [🔗 Source](https://bmirds.github.io/KidneyCancer/)                                                 |
| [🔬 CRC-HGD-v1: Colorectal Cancer Histopathological Grading Dataset](#-crc-hgd-v1-colorectal-cancer-histopathological-grading-dataset)                | 🦴 Colorectal             | 🏷️ Classification (Grading)                         | 3️⃣ Ordinal Multiclass (Grade I, Grade II, Grade III)                                                                    | ❌ No split                                 | 📅 Apr 11, 2026 | [🔗 Source](https://data.mendeley.com/datasets/yfp5sfj47m/2)                                        |
| [🔬 NCT-CRC-HE-100K: Colorectal Cancer Histology Patches](#-nct-crc-he-100k-100000-histological-images-of-human-colorectal-cancer-and-healthy-tissue) | 🦴 Colorectal             | 🏷️ Multiclass Classification                        | 9️⃣ Multiclass (ADI, BACK, DEB, LYM, MUC, MUS, NORM, STR, TUM)                                                           | ✅ Train/Val                                | 📅 Apr 12, 2026 | [🔗 Source](https://doi.org/10.5281/zenodo.1214456)                                                 |
| [🔬 Histopathological Imaging Database for Oral Cancer Analysis](#-histopathological-imaging-database-for-oral-cancer-analysis)                       | 🗣️ Oral Cavity           | 🏷️ Binary Classification                            | 2️⃣ Binary (Normal Epithelium, OSCC)                                                                                     | ❌ No split                                 | 📅 Apr 11, 2026 | [🔗 Source](https://data.mendeley.com/datasets/ftmp4cvtmb/2)                                        |
| [🔬 DeepHisto: Glioma Subtype Classification from WSIs](#-deephisto-dataset-for-glioma-subtype-classification-from-whole-slide-images)                | 🧠 Brain                  | 🏷️ Classification                                   | 5️⃣ Multiclass (IDH-mutant oligodendroglioma, IDH-mutant astrocytoma, IDH-wildtype glioblastoma, Normal brain, Necrosis) | ✅ Train/Test (patient-wise)                | 📅 May 08, 2026 | [🔗 Source](https://doi.org/10.5281/zenodo.7941080)                                                 |
| [🔬 GastroVision: Gastrointestinal Disease Detection](#-gastrovision-gastrointestinal-disease-detection)                                              | 🩺 Gastrointestinal Tract | 🏷️ Classification                                   | 2️⃣7️⃣ Multiclass (Landmarks, abnormalities, polyps, cancer, normal findings)                                            | ❌ No split (user-defined)                  | 📅 May 08, 2026 | [🔗 Source](https://www.kaggle.com/datasets/orvile/gastrovision-gastrointestinal-disease-detection) |
| [🔬 HER2-IHC-40x: HER2 Scoring in Breast Cancer](#-her2-ihc-40x-high-resolution-histopathology-image-dataset-for-her2-scoring-in-breast-cancer)       | 🫀 Breast                 | 🏷️ Classification                                   | 4️⃣ Ordinal Multiclass (HER2: 0, 1+, 2+, 3+)                                                                             | ✅ Train/Test (80/20, two split strategies) | 📅 May 08, 2026 | [🔗 Source](https://doi.org/10.5281/zenodo.15179608)                                                |
| [🔬 MSI-MSS Strong Patches: Microsatellite Status Classification](#-msi-mss-strong-patches-microsatellite-status-classification)                      | 🦴 Colorectal             | 🏷️ Binary Classification                            | 2️⃣ Binary (MSIMUT_strong, MSS_strong)                                                                                   | ❌ No split (user-defined)                  | 📅 May 08, 2026 | [🔗 Source](https://doi.org/10.5281/zenodo.3692380)                                                 |
| [🔬 CRC_DX: MSI vs. MSS Classification in GI Cancer](#-crc_dx-msi-vs-mss-classification-in-gastrointestinal-cancer)                                   | 🦴 Colorectal / Gastric   | 🏷️ Binary Classification                            | 2️⃣ Binary (MSS, MSIMUT)                                                                                                 | ✅ Train/Test (patient-wise, ~70/30)        | 📅 May 08, 2026 | [🔗 Source](https://doi.org/10.5281/zenodo.2530835)                                                 |

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
    title = {Development and evaluation of a deep neural network for histologic classification of renal cell carcinoma on biopsy and surgical resection slides},
    author = {Zhu, Mengdan and Ren, Bing and Richards, Ryland and Suriawinata, Matthew and Tomita, Naofumi and Hassanpour, Saeed},
    journal = {Scientific Reports},
    volume = {11},
    number = {1},
    pages = {7080},
    year = {2021},
    publisher = {Nature Publishing Group UK London},
    doi = {10.1038/s41598-021-86747-7}
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

### 🔬 NCT-CRC-HE-100K: 100,000 Histological Images of Human Colorectal Cancer and Healthy Tissue

**Study**: Kather, J. N., Halama, N., & Marx, A. (2024). 100,000 histological images of human colorectal cancer and
healthy tissue, April 2018. URL https://doi.org/10.5281/zenodo.1214456.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                            |
|-------------------------|--------------------------------------------------------------------|
| **📛 Title**            | NCT-CRC-HE-100K: Colorectal Cancer Histology Patches               |
| **🔗 Source**           | https://doi.org/10.5281/zenodo.1214456                             |
| **🦴 Target Organ**     | Colorectal / Colon                                                 |
| **📅 Last Accessed**    | April 11, 2026                                                     |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification, 🔍 Content-Based Retrieval          |
| **📐 Image Size**       | 224 × 224 pixels @ 0.5 µm/pixel (fixed)                            |
| **📁 Data Format**      | JPEG (.jpg), color-normalized (Macenko method) or raw              |
| **👥 Demographics**     | ❌ Not included (anonymized archival samples; N=136 patients total) |
| **🔄 Train/Test Split** | ✅ Yes (100K training patches + 7K validation patches)              |

#### 📊 Dataset Composition

| Category                   | Details                                                                                                                                                                       |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **🖼️ Total Images**       | 107,180 histopathological image patches                                                                                                                                       |
| **🔬 Imaging Modality**    | Brightfield histopathology (H&E-stained FFPE tissue sections)                                                                                                                 |
| **📦 Variants**            | • `NCT-CRC-HE-100K.zip`: Color-normalized (11.7 GB)<br>• `NCT-CRC-HE-100K-NONORM.zip`: Raw staining (11.7 GB)<br>• `CRC-VAL-HE-7K.zip`: Independent validation set (800.3 MB) |
| **🏥 Source Institutions** | National Center for Tumor Diseases (NCT), Heidelberg; University Medical Center Mannheim (UMM), Germany                                                                       |
| **📅 Collection Period**   | Archival samples; ethics approval renewed December 2017                                                                                                                       |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass tissue-type classification
- **Number of Classes**: 9️⃣

| Class Code | Full Name                            | Description                                    |
|------------|--------------------------------------|------------------------------------------------|
| ADI        | Adipose tissue                       | Fat cells                                      |
| BACK       | Background                           | Empty / non-tissue regions                     |
| DEB        | Debris                               | Necrotic or fragmented tissue                  |
| LYM        | Lymphocytes                          | Immune cell infiltrates                        |
| MUC        | Mucus                                | Extracellular mucin pools                      |
| MUS        | Smooth muscle                        | Muscularis propria or muscularis mucosae       |
| NORM       | Normal colon mucosa                  | Non-neoplastic glandular epithelium            |
| STR        | Cancer-associated stroma             | Desmoplastic reaction / tumor microenvironment |
| TUM        | Colorectal adenocarcinoma epithelium | Malignant glandular structures                 |

**📊 Dataset Distribution**:

| Split                      | Image Count | Patient Count | Purpose                            |
|----------------------------|-------------|---------------|------------------------------------|
| Training (NCT-CRC-HE-100K) | 100,000     | 86            | Model development                  |
| Validation (CRC-VAL-HE-7K) | 7,180       | 50            | Hyperparameter tuning / evaluation |
| **Total**                  | **107,180** | **136**       | —                                  |

> ⚠️ **Note**: Classes are only roughly balanced. Evaluation based solely on overall accuracy is discouraged; report
> per-class metrics and consider stratified sampling.

#### 💡 Usage Notes

- ✅ Benchmark dataset for tissue-type recognition in computational histopathology
- ✅ Pre-extracted, fixed-size patches enable direct integration with standard CNN architectures
- ✅ Color-normalized and non-normalized variants support research on stain invariance
- ✅ Independent validation set (CRC-VAL-HE-7K) enables reproducible benchmarking without data leakage
- 📚 Cite the Zenodo repository (DOI: 10.5281/zenodo.1214456) and associated publications when using this dataset
- 🔐 Distributed under CC BY 4.0; attribution required for redistribution or adaptation

#### ⚠️ Usage Considerations

| Aspect                             | Recommendation                                                                                             |
|------------------------------------|------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**             | Verify per-class distribution; apply class-weighted loss or stratified sampling if needed                  |
| **🎨 Stain Variability**           | Use color-normalized variant for reduced domain shift; or explicitly model staining as a covariate         |
| **🧪 Patch-Level vs. Slide-Level** | Patches are non-overlapping tiles; whole-slide inference requires aggregation strategies                   |
| **🔐 Ethical Compliance**          | Dataset contains anonymized human tissue; adhere to institutional review requirements for derivative works |
| **🧭 Domain Generalization**       | Sourced from two German centers; validate on external cohorts for clinical deployment                      |

#### 💡 Suggested Preprocessing Pipeline

1. **Select variant**: Choose color-normalized (`NCT-CRC-HE-100K.zip`) for reduced stain variability, or raw (`NONORM`)
   for domain adaptation research.
2. **Organize directory structure**: Arrange images by class label for compatibility with framework-native loaders (
   e.g., `torchvision.datasets.ImageFolder`).
3. **Load validation set separately**: Keep `CRC-VAL-HE-7K.zip` isolated to prevent accidental training contamination.
4. **Apply augmentations **(training only): Incorporate rotation, flipping, and mild intensity jittering; avoid
   geometric distortions that alter tissue architecture.
5. **Normalization**: Scale pixel values to [0, 1] or standardize using ImageNet statistics if using pretrained
   backbones.
6. **Stratified evaluation**: Report per-class precision, recall, F1-score, and confusion matrices; compute
   macro-averaged metrics to account for class imbalance.
7. **Aggregation **(optional): For slide-level prediction, implement majority voting, attention-based pooling, or
   multiple-instance learning over patch predictions.

#### 🔗 Associated Resources

- **Primary Publication**: Kather et al., "Predicting survival from colorectal cancer histology slides using deep
  learning: A retrospective multicenter study," *PLOS Medicine*,
    2019. [DOI](https://doi.org/10.1371/journal.pmed.1002730)
- **Color Normalization Reference**: Macenko et al., "A method for normalizing histology slides for quantitative
  analysis," *ISBI*, 2009. [DOI](https://doi.org/10.1109/ISBI.2009.5193250)
- **GitHub Implementations**: Multiple open-source repositories implement benchmarks on this dataset; search "
  NCT-CRC-HE-100K" on GitHub for reference code.
- **Related Datasets**:
    - [CRC-HGD-v1](#-crc-hgd-v1-colorectal-cancer-histopathological-grading-dataset) (grading-focused)
    - [HunCRC](https://doi.org/10.1038/s41597-022-01450-y) (Hungarian colorectal cancer dataset)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{kather2018nctcrc,
    author = {Kather, Jakob Nikolas and Halama, Niels and Marx, Alexander},
    title = {100,000 histological images of human colorectal cancer and healthy tissue},
    year = {2018},
    publisher = {Zenodo},
    version = {v0.1},
    doi = {10.5281/zenodo.1214456},
    url = {https://doi.org/10.5281/zenodo.1214456}
}

@article{kather2019plosmed,
    title = {Predicting survival from colorectal cancer histology slides using deep learning: A retrospective multicenter study},
    author = {Kather, Jakob Nikolas and Krisam, Johannes and Charoentong, Pornpimol and Luedde, Tom and Herpel, Esther and Weis, Cleo-Aron and Gaiser, Timo and Marx, Alexander and Valous, Nektarios A and Ferber, Dyke and others},
    journal = {PLOS Medicine},
    volume = {16},
    number = {1},
    pages = {e1002730},
    year = {2019},
    publisher = {Public Library of Science San Francisco, CA USA},
    doi = {10.1371/journal.pmed.1002730}
}
```

---

### 🔬 Histopathological Imaging Database for Oral Cancer Analysis

**Study**: Rahman, T. Y., Mahanta, L. B., Das, A. K., & Sarma, J. D. (2020). Histopathological imaging database for oral
cancer analysis. *Data in Brief*, 29, 105114.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                           |
|-------------------------|-------------------------------------------------------------------|
| **📛 Title**            | Histopathological Imaging Database for Oral Cancer Analysis       |
| **🔗 Source**           | https://data.mendeley.com/datasets/ftmp4cvtmb/2                   |
| **🗣️ Target Organ**    | Oral Cavity (Buccal Mucosa)                                       |
| **📅 Last Accessed**    | April 11, 2026                                                    |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification, 🎭 Segmentation, 🔍 Feature Extraction |
| **📐 Image Size**       | 2048 x 1536 pixels (fixed resolution)                             |
| **📁 Data Format**      | JPEG (.jpg)                                                       |
| **👥 Demographics**     | ❌ Not included (de-identified; 230 patients total)                |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)            |

#### 📊 Dataset Composition

| Category                    | Details                                                                  |
|-----------------------------|--------------------------------------------------------------------------|
| **🖼️ Total Images**        | 1,224 histopathological images                                           |
| **🔬 Imaging Modality**     | Brightfield histopathology (H&E-stained punch biopsy sections)           |
| **🔍 Magnification Levels** | 100x (10x objective x 10x eyepiece), 400x (40x objective x 10x eyepiece) |
| **📦 Total Size**           | ~2.89 GB (compressed)                                                    |
| **🏥 Curation**             | Ayursundra Healthcare Pvt. Ltd. & Dr. B. Borooah Cancer Institute, India |
| **📅 Collection Period**    | October 2016 - November 2017                                             |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification (Normal vs. Malignant)
- **Number of Classes**: 2️⃣
    - ✅ Normal Epithelium of Oral Cavity
    - ⚠️ Oral Squamous Cell Carcinoma (OSCC)

**📊 Image Distribution by Magnification**:

| Magnification | Category | Image Count | Primary Application Scope                                                                    |
|---------------|----------|-------------|----------------------------------------------------------------------------------------------|
| **100x**      | Normal   | 89          | Architectural/tissue-level analysis, epithelial layer segmentation, tumor invasion detection |
| **100x**      | OSCC     | 439         | —                                                                                            |
| **400x**      | Normal   | 201         | Cellular/nuclear-level analysis, texture-based feature extraction                            |
| **400x**      | OSCC     | 495         | —                                                                                            |
| **Total**     | —        | **1,224**   | —                                                                                            |

**🔬 Multi-Scale Analysis Capability**:

- **100x images**: Optimized for tissue architecture assessment, basement membrane invasion detection, and whole-image
  feature extraction.
- **400x images**: Suitable for cytological analysis, nuclear morphometry, and fine-grained textural pattern
  classification.

#### 💡 Usage Notes

- ✅ First publicly available dataset dedicated to oral cavity histopathology with OSCC labels
- ✅ Dual-magnification design enables multi-scale feature learning and resolution-aware modeling
- ✅ Expert-validated labels derived from corresponding pathological reports
- ✅ Open access under CC BY 4.0 license; attribution required for reuse
- 📚 Cite both the *Data in Brief* article and the Mendeley Data repository in publications

#### ⚠️ Usage Considerations

| Aspect                         | Recommendation                                                                                 |
|--------------------------------|------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**         | OSCC class is substantially larger than Normal; apply class weighting or oversampling          |
| **🔬 Magnification Strategy**  | Process 100x and 400x sets separately or fuse features via multi-branch architectures          |
| **🧪 Domain Specificity**      | Images sourced from buccal mucosa; generalizability to other oral subsites requires validation |
| **🎨 Stain Variability**       | Apply stain normalization (e.g., Macenko) to mitigate inter-slide color variation              |
| **🧭 Data Leakage Prevention** | Partition by patient ID (not image) to ensure no patient appears in both train and test sets   |

#### 💡 Suggested Preprocessing Pipeline

1. **Organize by magnification**: Create separate directories for 100x and 400x images, subdivided by class.
2. **Patient-aware splitting**: Use metadata (if available) or file naming conventions to ensure patient-level
   stratification.
3. **Resolution standardization**: Resize images to model-compatible dimensions (e.g., 224x224, 512x512) while
   preserving aspect ratio.
4. **Color normalization**: Apply histogram matching or stain normalization to reduce batch effects.
5. **Augmentation **(training): Incorporate rotation, flipping, and mild intensity jittering; avoid aggressive
   transformations that distort histological structures.
6. **Feature extraction **(optional): For traditional ML approaches, extract GLCM, LBP, or color histogram features as
   demonstrated in the original study.
7. **Evaluation**: Report sensitivity, specificity, and AUC-ROC alongside accuracy, given the clinical diagnostic
   context.

#### 🔗 Associated Resources

- **GitHub Repository**:
  https://github.com/Tabassum2019/A-histopathological-image-repository-of-normal-epithelium-of-Oral-Cavity-and-OSCC
- **Related Publications**:
    - Rahman, T. Y., Mahanta, L. B., Chakraborty, C., Das, A. K., & Sarma, J. D. (2018). Textural pattern classification
      for oral squamous cell carcinoma. Journal of microscopy, 269(1), 85-93. [DOI](https://doi.org/10.1111/jmi.12611)
    - Rahman, T. Y., Mahanta, L. B., Das, A. K., & Sarma, J. D. (2020). Automated oral squamous cell carcinoma
      identification using shape, texture and color features of whole image strips. Tissue and Cell, 63,
        101322. [DOI](https://doi.org/10.1016/j.tice.2019.101322)
- **Contact**: Corresponding authors via Mendeley Data page or institutional affiliations

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{rahman2023oralcancer,
    author = {Rahman, Tabassum Yesmin and Mahanta, Lipi B. and Das, Anup K. and Sarma, Jagannath D.},
    title = {Histopathological imaging database for Oral Cancer analysis},
    year = {2023},
    publisher = {Mendeley Data},
    version = {2},
    doi = {10.17632/ftmp4cvtmb.2},
    url = {https://data.mendeley.com/datasets/ftmp4cvtmb/2}
}

@article{rahman2020dib,
    title = {Histopathological imaging database for oral cancer analysis},
    author = {Rahman, Tabassum Yesmin and Mahanta, Lipi B. and Das, Anup K. and Sarma, Jagannath D.},
    journal = {Data in Brief},
    volume = {29},
    pages = {105114},
    year = {2020},
    publisher = {Elsevier},
    doi = {10.1016/j.dib.2020.105114}
}
```

---

### 🔬 DeepHisto: Dataset for Glioma Subtype Classification from Whole Slide Images

**Study**: Mittelbronn, M., Hau, A.-C., Kim, S.-Y., Nazarov, P. V., Despotovic, V., Kakoichankava, A., Borgmann, F. B.
K., & Klamminger, G. G. (2023). DeepHisto: Dataset for glioma subtype classification from Whole Slide Images (
0.1) [Data set]. Zenodo.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                              |
|-------------------------|--------------------------------------------------------------------------------------|
| **📛 Title**            | DeepHisto: Dataset for glioma subtype classification from Whole Slide Images         |
| **🔗 Source**           | https://doi.org/10.5281/zenodo.7941080                                               |
| **🧠 Target Organ**     | Brain                                                                                |
| **📅 Last Accessed**    | May 08, 2026                                                                         |
| **🎯 Supported Tasks**  | 🏷️ Classification                                                                   |
| **📐 Image Size**       | 512 × 512 pixels (tile patches)                                                      |
| **📁 Data Format**      | Image tiles extracted from Whole Slide Images (format unspecified; typical: JPG/PNG) |
| **👥 Demographics**     | ❌ Not included (de-identified archival samples; N=28 patients)                       |
| **🔄 Train/Test Split** | ✅ Yes (patient-wise partitioning)                                                    |

#### 📊 Dataset Composition

| Category                 | Details                                                                         |
|--------------------------|---------------------------------------------------------------------------------|
| **🖼️ Total Tiles**      | 42,718 tiles extracted from 28 adult-type diffuse glioma cases                  |
| **🔬 Imaging Modality**  | Brightfield histopathology (Hematoxylin & Eosin stain)                          |
| **🔍 Scanner**           | IntelliSite Ultra Fast digital slide scanner (Philips), 20x/0.75 NA Plan Apo    |
| **📏 Resolution**        | 0.25 µm/pixel (average slide resolution)                                        |
| **📦 File Structure**    | train.zip (~19.2 GB), test.zip (~2.1 GB), readme.txt (1.5 kB)                   |
| **🏥 Source**            | National Center of Pathology (NCP), Luxembourg National Health Laboratory (LNS) |
| **📅 Collection Period** | 2017–2021                                                                       |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of diffuse glioma subtypes per WHO CNS5 classification
- **Number of Classes**: 5️⃣ (4 tumor entities + necrosis; normal brain as control)
    - 🟤 IDH-mutant astrocytoma
    - 🔴 IDH-wildtype glioblastoma
    - 🟣 IDH-mutant, 1p/19q codeleted oligodendroglioma
    - ⚪ Normal brain tissue (white and gray matter controls)
    - ⚫ Necrosis (annotated regions)

**📊 Tile Distribution by Class and Split**:

| Class                | Train Tiles | Test Tiles | Total Tiles |
|----------------------|-------------|------------|-------------|
| 🟤 Astrocytoma       | 3,755       | 465        | 4,220       |
| 🔴 Glioblastoma      | 1,633       | 241        | 1,874       |
| 🟣 Oligodendroglioma | 3,384       | 431        | 3,815       |
| ⚪ Normal Brain       | 29,383      | 2,947      | 32,330      |
| ⚫ Necrosis           | 389         | 90         | 479         |
| **Total**            | **38,544**  | **4,174**  | **42,718**  |

> **ℹ️ Note**: Tile counts reflect patient-wise partitioning to prevent data leakage. Normal brain tissue tiles
> constitute the majority class; consider class-weighted loss functions or stratified sampling during training.

**📋 Annotation Protocol**:

- Region annotation performed by board-certified pathologists
- Regions of interest divided into square 512×512 pixel tiles
- Each tile associated with a class label denoting tumor entity, normal tissue, or necrosis
- Patient-wise split into training and test subsets to ensure subject-level independence

#### 💡 Usage Notes

- ✅ Suitable for benchmarking deep learning models for histopathological glioma classification
- ✅ High-resolution WSI tiles (0.25 µm/pixel) enable fine-grained morphological analysis
- ✅ Patient-wise train/test split ensures robust evaluation without subject-level data leakage
- ✅ WHO CNS5-aligned classification supports clinically relevant subtype prediction
- ✅ Explicit necrosis class enables research on tumor microenvironment and tissue viability
- 📚 Required to cite the original Zenodo repository (DOI: 10.5281/zenodo.7941080) in publications
- 🔐 Distributed under CC BY 4.0; attribution required for redistribution or adaptation

#### ⚠️ Usage Considerations

| Aspect                       | Recommendation                                                                                                        |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**       | Normal brain tiles dominate (~75%); apply class-weighted loss or oversampling for minority classes                    |
| **🎨 Stain Variability**     | Apply stain normalization (e.g., Macenko method) to mitigate inter-slide variation                                    |
| **🧪 Patch-Level vs. WSI**   | Tiles are extracted patches; whole-slide inference requires aggregation strategies                                    |
| **🔐 Ethical Compliance**    | Dataset contains anonymized human tissue; adhere to institutional review requirements                                 |
| **🧭 Domain Generalization** | Single-center Luxembourg cohort; validate on external cohorts for clinical deployment                                 |
| **⚠️ Necrosis Handling**     | Necrosis class is sparse (~1%); consider treating as auxiliary task or excluding if not relevant to research question |

#### 💡 Suggested Preprocessing Pipeline

1. **Extract archives**: Unzip `train.zip` and `test.zip` into structured directories by split.
2. **Organize by label**: Arrange tiles into class-labeled subfolders for framework-native data loading.
3. **Standardize resolution**: Confirm uniform 512×512 pixel dimensions; resize if preprocessing pipelines require fixed
   input sizes.
4. **Color normalization**: Apply stain normalization (e.g., Macenko or Vahadane methods) to reduce inter-slide color
   variability.
5. **Class-aware augmentation **(training only): Incorporate rotation, flipping, and mild intensity jittering; apply
   stronger augmentation to minority classes (glioblastoma, necrosis) to improve generalization.
6. **Patient-aware validation**: Maintain patient-wise separation during cross-validation to prevent data leakage.
7. **Evaluation metrics**: Report per-subtype precision, recall, F1-score, and confusion matrices; compute
   macro-averaged metrics to account for class imbalance.

#### 🔗 Associated Resources

- **Zenodo Repository**: https://doi.org/10.5281/zenodo.7941080
- **WHO Classification Reference**: WHO Classification of Tumours Editorial Board. Central Nervous System Tumours. 5th
  ed. Vol 6. Lyon (France): International Agency for Research on Cancer; 2021.
- **Funding Acknowledgment**: This work was supported by the Luxembourg National Research Fund (FNR) grants
  C21/BM/15739125/DIOMEDES and PEARL P16/BM/11192868.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{mittelbronn2023deephisto,
    author = {Mittelbronn, Michel and Hau, Ann-Christin and Kim, Sang-Yoon and Nazarov, Petr V. and Despotovic, Vladimir and Kakoichankava, Aliaksandra and Borgmann, Felix Bruno Kleine and Klamminger, Gilbert Georg},
    title = {DeepHisto: Dataset for glioma subtype classification from Whole Slide Images},
    year = {2023},
    publisher = {Zenodo},
    version = {0.1},
    doi = {10.5281/zenodo.7941080},
    url = {https://doi.org/10.5281/zenodo.7941080}
}
```

---

### 🔬 GastroVision: Gastrointestinal Disease Detection

**Study**: Jha, D., Sharma, V., Riegler, M., Halvorsen, P., & Bagci, U. (2024). GastroVision: A Compact GI Endoscopy
Dataset. Kaggle.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                                |
|-------------------------|----------------------------------------------------------------------------------------|
| **📛 Title**            | GastroVision: Gastrointestinal Disease Detection                                       |
| **🔗 Source**           | https://www.kaggle.com/datasets/orvile/gastrovision-gastrointestinal-disease-detection |
| **🦴 Target Organ**     | Gastrointestinal Tract (Esophagus, Stomach, Small Bowel, Colon, Rectum)                |
| **📅 Last Accessed**    | May 08, 2026                                                                           |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                                                          |
| **📐 Image Size**       | Variable (endoscopy frames; standardization recommended)                               |
| **📁 Data Format**      | JPEG/PNG (.jpg/.png) organized in class-labeled subdirectories                         |
| **👥 Demographics**     | ❌ Not included (de-identified clinical endoscopy footage)                              |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                                 |

#### 📊 Dataset Composition

| Category                   | Details                                                                    |
|----------------------------|----------------------------------------------------------------------------|
| **🖼️ Total Images**       | 8,000 gastrointestinal endoscopy images                                    |
| **🔬 Imaging Modality**    | White-light endoscopy (WLE) and narrow-band imaging (NBI) frames           |
| **🏥 Source Institutions** | Baerum Hospital (Norway), Karolinska University Hospital (Sweden)          |
| **📦 File Structure**      | 27 class-labeled directories + Google Drive download (~1.81 GB compressed) |
| **👨‍⚕️ Annotation**       | Expert endoscopist-verified labels                                         |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of gastrointestinal findings
- **Number of Classes**: 2️⃣7️⃣ organized into four conceptual groups:

**🔍 Anatomical Landmarks **(10 classes)
| Class | Image Count | Description |
|-------|-------------|-------------|
| Cecum | 113 | Ileocecal region identification |
| Duodenal bulb | 205 | First part of duodenum |
| Gastroesophageal_junction_normal z-line | 330 | GEJ landmark |
| Ileocecal valve | 200 | Valve between ileum and cecum |
| Pylorus | 393 | Gastric outlet |
| Retroflex rectum | 67 | Rectal view in retroflexion |
| Small bowel_terminal ileum | 846 | Distal small intestine |
| Normal esophagus | 140 | Healthy esophageal mucosa |
| Normal stomach | 969 | Healthy gastric mucosa |
| Normal mucosa and vascular pattern in the large bowel | 1,467 | Healthy colonic mucosa |

**⚠️ Pathological Findings **(11 classes)
| Class | Image Count | Description |
|-------|-------------|-------------|
| Angiectasia | 17 | Vascular ectasia/bleeding source |
| Barretts esophagus | 95 | Metaplastic esophageal epithelium |
| Blood in lumen | 171 | Active or recent hemorrhage |
| Colon diverticula | 29 | Colonic outpouchings |
| Colorectal cancer | 139 | Malignant colonic lesions |
| Erythema | 15 | Mucosal inflammation/redness |
| Esophageal varices | 7 | Dilated submucosal veins |
| Esophagitis | 107 | Esophageal inflammation |
| Gastric polyps | 65 | Gastric mucosal protrusions |
| Mucosal inflammation large bowel | 29 | Colonic inflammatory changes |
| Ulcer | 6 | Mucosal defect with fibrinous base |

**🩺 Polyp-Related Interventions **(5 classes)
| Class | Image Count | Description |
|-------|-------------|-------------|
| Colon polyps | 820 | Untreated colonic polyps |
| Dyed-lifted-polyps | 141 | Polyps prepared for resection |
| Dyed-resection-margins | 246 | Post-resection margin assessment |
| Resected polyps | 92 | Removed polyp specimens |
| Resection margins | 25 | Margins after polypectomy |

**🛠️ Procedural/Accessory **(1 class)
| Class | Image Count | Description |
|-------|-------------|-------------|
| Accessory tools | 1,266 | Endoscopic instruments, caps, clips |

**📊 Class Distribution Summary**:

| Category                                | Total Images | % of Dataset |
|-----------------------------------------|--------------|--------------|
| Normal Findings                         | ~2,576       | ~32.2%       |
| Pathological Findings                   | ~588         | ~7.4%        |
| Polyp-Related                           | ~1,324       | ~16.6%       |
| Accessory Tools                         | ~1,266       | ~15.8%       |
| Anatomical Landmarks (excluding normal) | ~2,246       | ~28.1%       |
| **Total**                               | **~8,000**   | **100%**     |

> **ℹ️ Note**: Significant class imbalance exists (e.g., Ulcer: n=6 vs. Normal mucosa large bowel: n=1,467). Stratified
> sampling or class-weighted loss functions are strongly recommended.

#### 💡 Usage Notes

- ✅ Suitable for benchmarking endoscopic image classification and computer-aided diagnosis (CAD) systems
- ✅ Multi-institutional sourcing (Norway/Sweden) supports cross-center generalization studies
- ✅ Expert-annotated labels enhance clinical validity for translational research
- ✅ Includes procedural and post-intervention classes for comprehensive workflow modeling
- 📚 Required to cite the original Kaggle repository and associated publications when using this dataset
- 🔐 Distributed under CC BY 4.0; attribution required for redistribution or adaptation

#### ⚠️ Usage Considerations

| Aspect                            | Recommendation                                                                                                           |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| **🔍 Severe Class Imbalance**     | Apply class-weighted cross-entropy loss, focal loss, or oversampling for rare classes (e.g., Ulcer, Esophageal varices)  |
| **🎨 Image Resolution Variance**  | Endoscopy frames vary in resolution; standardize to fixed dimensions (e.g., 224×224) prior to training                   |
| **🧪 Clinical Context Awareness** | Some classes represent procedural states (e.g., dyed-lifted-polyps); ensure task alignment with research objectives      |
| **🔐 Ethical Compliance**         | Dataset contains de-identified clinical imagery; adhere to institutional review requirements for derivative works        |
| **🧭 Domain Generalization**      | Sourced from two European centers; validate on external cohorts (e.g., Asian, North American) before clinical deployment |
| **📦 Data Organization**          | Class directories include "Accessory tools"; consider excluding or treating as auxiliary class depending on task         |

#### 💡 Suggested Preprocessing Pipeline

1. **Download and extract**: Access via Google Drive link; unzip into structured directory preserving class subfolders.
2. **Filter optional classes**: Optionally exclude "Accessory tools" if focus is purely on diagnostic classification.
3. **Standardize geometry**: Resize all images to uniform dimensions (e.g., 256×256 or 512×512) while preserving aspect
   ratio.
4. **Color normalization**: Apply histogram equalization or adaptive contrast enhancement to mitigate endoscope-specific
   color variation.
5. **Class-aware augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering; apply
   stronger augmentation to underrepresented classes.
6. **Stratified splitting**: Partition data by class to maintain distribution balance; ensure no patient-level leakage
   if metadata permits.
7. **Evaluation metrics**: Report macro-averaged precision, recall, and F1-score alongside per-class metrics to account
   for imbalance; consider hierarchical evaluation grouping related classes.

#### 🔗 Associated Resources

- **Kaggle Repository**: https://www.kaggle.com/datasets/orvile/gastrovision-gastrointestinal-disease-detection
- **Google Drive Download**: https://drive.google.com/drive/folders/1T35gqO7jIKNxC-gVA2YVOMdsL7PSqeAa
- **Related Datasets**:
    - [Kvasir-V2](https://datasets.simula.no/kvasir-v2/) (8,000 GI images, 8 classes)
    - [Kvasir-SEG](https://datasets.simula.no/kvasir-seg/) (Polyp segmentation benchmark)
    - [HyperKvasir](https://datasets.simula.no/hyper-kvasir/) (Multi-label GI classification)
- **Contributors**: Debesh Jha, Vanshali Sharma, Michael Riegler, Pål Halvorsen, Ulas Bagci

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{jha2024gastrovision,
    author = {Jha, Debesh and Sharma, Vanshali and Riegler, Michael and Halvorsen, P{\aa}l and Bagci, Ulas},
    title = {GastroVision: Gastrointestinal Disease Detection},
    year = {2024},
    publisher = {Kaggle},
    url = {https://www.kaggle.com/datasets/orvile/gastrovision-gastrointestinal-disease-detection},
    note = {Accessed: May 08, 2026}
}
```

---

### 🔬 HER2-IHC-40x: High-Resolution Histopathology Image Dataset for HER2 Scoring in Breast Cancer

**Study**: Nabi, M. S., Fauzi, M. F. A., Rehman, Z. U., Karim, H. B. A., Cheah, P. L., Chiew, S. F., & Looi, L. M. (
2025). HER2-IHC-40x: A High-Resolution Histopathology Dataset for HER2 IHC Scoring in Breast Cancer. *Data in Brief*,

111922.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------|
| **📛 Title**            | HER2-IHC-40x: High-Resolution Histopathology Image Dataset for HER2 Scoring in Breast Cancer |
| **🔗 Source**           | https://doi.org/10.5281/zenodo.15179608                                                      |
| **🫀 Target Organ**     | Breast                                                                                       |
| **📅 Last Accessed**    | May 08, 2026                                                                                 |
| **🎯 Supported Tasks**  | 🏷️ Ordinal Classification (HER2 IHC Scoring)                                                |
| **📐 Image Size**       | 1024 × 1024 pixels (fixed patch size)                                                        |
| **📁 Data Format**      | PNG/JPEG patches extracted from Whole Slide Images (.svs); ROI masks in PNG                  |
| **👥 Demographics**     | ❌ Not included (de-identified archival samples; N=107 patients)                              |
| **🔄 Train/Test Split** | ✅ Yes (80/20 split; two variants: WSI-level and patch-level partitioning)                    |

#### 📊 Dataset Composition

| Category                  | Details                                                                                |
|---------------------------|----------------------------------------------------------------------------------------|
| **🖼️ Total Patches**     | Variant 1: 9,940 patches; Variant 2: 10,997 patches                                    |
| **🔬 Imaging Modality**   | Brightfield immunohistochemistry (HER2-stained FFPE tissue sections)                   |
| **🔍 Magnification**      | 40× objective (high-resolution)                                                        |
| **📦 File Structure**     | Two ZIP archives: `her2-ihc-40x-patch.zip` (~1.7 GB), `her2-ihc-40x-wsi.zip` (~1.5 GB) |
| **🏥 Source Institution** | Multimedia University, Malaysia; collaborating clinical centers                        |
| **👨‍⚕️ Annotation**      | Expert pathologist-annotated ROIs using Cytomine platform                              |

#### 🏷️ Classification Task Details

- **Task Type**: Ordinal multiclass classification of HER2 immunohistochemistry (IHC) scoring per ASCO/CAP guidelines
- **Number of Classes**: 4️⃣ (ordered severity scale)

| HER2 Score | Description                                              | Clinical Interpretation               |
|------------|----------------------------------------------------------|---------------------------------------|
| 🔘 0       | No observable staining                                   | Negative                              |
| 🟡 1+      | Weak/incomplete membrane staining in ≤10% of tumor cells | Negative                              |
| 🟠 2+      | Moderate circumferential staining in >10% of tumor cells | Equivocal (requires ISH confirmation) |
| 🔴 3+      | Strong circumferential staining in >10% of tumor cells   | Positive                              |

**📊 Dataset Variants & Statistics**:

**Variant 1: HER2-IHC-40x **(WSI-Level Split)
> Whole-slide images partitioned 80/20 *before* patch extraction to prevent patient-level data leakage.

| HER2 Class | WSIs    | ROIs      | Train Patches | Test Patches | Total Patches |
|------------|---------|-----------|---------------|--------------|---------------|
| 🔘 0       | 23      | 429       | 3,031         | 758          | 3,789         |
| 🟡 1+      | 26      | 131       | 1,722         | 431          | 2,153         |
| 🟠 2+      | 27      | 483       | 507           | 127          | 634           |
| 🔴 3+      | 31      | 156       | 2,691         | 673          | 3,364         |
| **Total**  | **107** | **1,199** | **7,951**     | **1,989**    | **9,940**     |

**Variant 2: HER2-IHC-40x-WSI **(Patch-Level Split)
> Patches extracted first, then partitioned 80/20 *after* extraction (higher patch count due to expanded ROI coverage).

| HER2 Class | WSIs    | ROIs      | Train Patches | Test Patches | Total Patches |
|------------|---------|-----------|---------------|--------------|---------------|
| 🔘 0       | 23      | 429       | 3,031         | 758          | 3,789         |
| 🟡 1+      | 26      | 131       | 2,151         | 538          | 2,689         |
| 🟠 2+      | 27      | 483       | 905           | 226          | 1,131         |
| 🔴 3+      | 31      | 156       | 2,710         | 678          | 3,388         |
| **Total**  | **107** | **1,199** | **8,797**     | **2,200**    | **10,997**    |

> **ℹ️ Note**: Class 2+ (Equivocal) is underrepresented (~6–10% of patches). Consider ordinal regression, class-weighted
> loss, or focal loss to address imbalance. Variant 1 (WSI-level split) is recommended for rigorous generalization
> evaluation.

#### 🔧 Preprocessing & Quality Control Protocol

1. **ROI Selection**: Manual tumor region annotation by board-certified pathologists using Cytomine.
2. **Color Histogram Filtering**: HSV-based filtering to exclude non-tumor tissue, background, and low-quality patches.
3. **Intensity Normalization**: Global intensity normalization applied across all patches to reduce staining
   variability.
4. **Patch Extraction**: Adaptive sliding-window extraction of 1024×1024 pixel patches from annotated ROIs.
5. **Quality Assurance**: Expert review of sampled patches to verify label consistency and image quality.

#### 💡 Usage Notes

- ✅ Suitable for benchmarking deep learning models for HER2 IHC scoring automation
- ✅ High-resolution 40× patches (1024×1024) enable fine-grained membrane staining pattern analysis
- ✅ Two split strategies support research on data leakage prevention and generalization robustness
- ✅ Ordinal class structure enables investigation of monotonic loss functions and ordinal regression architectures
- ✅ Includes original WSIs (.svs) and ROI masks for reproducible patch regeneration
- 📚 Required to cite the original *Data in Brief* publication and Zenodo repository in derivative works
- 🔐 Distributed under CC BY-SA 4.0; attribution and share-alike conditions apply for redistribution

#### ⚠️ Usage Considerations

| Aspect                       | Recommendation                                                                                                                      |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**       | Class 2+ is sparse; apply class-weighted cross-entropy, focal loss, or oversampling                                                 |
| **📊 Ordinal Structure**     | Classes represent ordered severity; consider ordinal regression or monotonic constraints                                            |
| **🧪 Split Strategy**        | Prefer Variant 1 (WSI-level split) for patient-independent evaluation; Variant 2 may inflate performance due to patch-level leakage |
| **🎨 Stain Variability**     | Apply additional stain normalization (e.g., Macenko) if integrating external cohorts                                                |
| **🔐 Ethical Compliance**    | Dataset contains de-identified human tissue; adhere to institutional review requirements                                            |
| **🧭 Domain Generalization** | Single-region sourcing (Malaysia); validate on geographically diverse cohorts before clinical deployment                            |

#### 💡 Suggested Preprocessing Pipeline

1. **Select variant**: Choose Variant 1 (`her2-ihc-40x-patch.zip`) for rigorous evaluation; Variant 2 for maximum patch
   availability.
2. **Organize directory structure**: Arrange patches into class-labeled subfolders within `Train/` and `Test/`
   directories.
3. **Standardize input**: Confirm uniform 1024×1024 dimensions; resize if model architecture requires smaller inputs (
   e.g., 512×512).
4. **Color normalization**: Apply stain normalization (e.g., Macenko or Vahadane) to mitigate inter-slide IHC staining
   variability.
5. **Ordinal-aware augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering;
   preserve membrane staining integrity.
6. **Stratified mini-batching**: Ensure each training batch contains samples from all four HER2 classes to stabilize
   ordinal learning.
7. **Evaluation metrics**: Report per-class precision/recall, weighted kappa for ordinal agreement, and macro-averaged
   F1-score; include confusion matrices to assess 2+ misclassification patterns.

#### 🔗 Associated Resources

- **Zenodo Repository**: https://doi.org/10.5281/zenodo.15179608
- **Preprocessing Code**: https://github.com/seraju77/HER2-IHC-40x-data-preprocessing
- **Related Publications**:
    - Nabi et al. (2025). "Explainable deep learning models for HER2 IHC scoring in breast cancer diagnosis."
      *Informatics in Medicine Unlocked*, 101700.
    - Wolff et al. (2018). "Human Epidermal Growth Factor Receptor 2 Testing in Breast Cancer: ASCO/CAP Guideline
      Update." *Journal of Clinical Oncology*.
- **Related Datasets**:
    - [BACH](https://bach.grand-challenge.org/) (Breast cancer histology classification)
    - [BreakHis](https://web.inf.ufpr.br/vri/databases/breast-cancer-histological-images/) (Breast tumor microscopy
      images)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{nabi2025her2,
    title = {HER2-IHC-40x: A High-Resolution Histopathology Dataset for HER2 IHC Scoring in Breast Cancer},
    author = {Nabi, Md Serajun and Fauzi, Mohammad Faizal Ahmad and Rehman, Zaka Ur and Karim, Hezerul Bin Abdul and Cheah, Phaik Leng and Chiew, Seow Fan and Looi, Lai Meng},
    journal = {Data in Brief},
    pages = {111922},
    year = {2025},
    publisher = {Elsevier},
    doi = {10.1016/j.dib.2025.111922}
}

@dataset{nabi2025her2zenodo,
    author = {Nabi, Md Serajun and Fauzi, Mohammad Faizal Ahmad and Karim, Hezerul Bin Abdul and Cheah, Phaik Leng and Chiew, Seow Fan and Looi, Lai Meng and Multimedia University},
    title = {HER2-IHC-40x: High-Resolution Histopathology Image Dataset for HER2 Scoring in Breast Cancer},
    year = {2025},
    publisher = {Zenodo},
    version = {v1},
    doi = {10.5281/zenodo.15179608},
    url = {https://doi.org/10.5281/zenodo.15179608}
}
```

---

### 🔬 MSI-MSS Strong Patches: Microsatellite Status Classification

**Study**: Shen, Y. (2020). Strong histopathological relevance patches for MSI vs. MSS classification (Version

1) [Data set]. Zenodo.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                            |
|-------------------------|------------------------------------------------------------------------------------|
| **📛 Title**            | Strong histopathological relevance patches for MSI vs. MSS classification          |
| **🔗 Source**           | https://doi.org/10.5281/zenodo.3692380                                             |
| **🦴 Target Organ**     | Colorectal / Gastrointestinal                                                      |
| **📅 Last Accessed**    | May 08, 2026                                                                       |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification (Microsatellite Instability Detection)                   |
| **📐 Image Size**       | Variable (histopathological patches; standardization recommended)                  |
| **📁 Data Format**      | Image patches extracted from H&E-stained FFPE tissue sections (format unspecified) |
| **👥 Demographics**     | ❌ Not included (de-identified archival samples)                                    |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                             |

#### 📊 Dataset Composition

| Category                 | Details                                                                            |
|--------------------------|------------------------------------------------------------------------------------|
| **🖼️ Total Patches**    | 55,453 histopathological image patches                                             |
| **🔬 Imaging Modality**  | Brightfield histopathology (Hematoxylin & Eosin stain, FFPE tissue sections)       |
| **🎯 Selection Method**  | Neural network-based fused distillation + expert pathologist morphology validation |
| **📦 File Structure**    | Two ZIP archives: `MSIMUT_strong.zip` (~3.2 GB), `MSS_strong.zip` (~3.1 GB)        |
| **🏥 Source**            | Subset of CRC_DX dataset (Zenodo: 10.5281/zenodo.2530835)                          |
| **📅 Collection Period** | Archival FFPE samples; published February 2020                                     |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification of microsatellite status in colorectal/gastrointestinal cancer
- **Number of Classes**: 2️⃣

| Class Label      | Description                                                                   | Clinical Significance                                                          |
|------------------|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| 🔵 MSIMUT_strong | Patches with strong histopathological relevance to microsatellite instability | Associated with defective DNA mismatch repair; predicts immunotherapy response |
| 🔴 MSS_strong    | Patches with strong histopathological relevance to microsatellite stability   | Intact mismatch repair; standard chemotherapy indications                      |

**📊 Patch Distribution**:

| Class            | Patch Count | % of Dataset |
|------------------|-------------|--------------|
| 🔵 MSIMUT_strong | 28,307      | ~51.0%       |
| 🔴 MSS_strong    | 27,146      | ~49.0%       |
| **Total**        | **55,453**  | **100%**     |

> **ℹ️ Note**: This dataset represents a curated subset of the parent CRC_DX collection, filtered via neural network
> distillation and pathologist expert review to retain only patches with strong morphological relevance to MSI/MSS
> classification. This enhances signal-to-noise ratio for model training but may limit generalizability to unfiltered
> histological regions.

#### 🔧 Curation & Quality Control Protocol

1. **Parent Dataset**: Derived from "Histological images for MSI vs. MSS classification in gastrointestinal cancer, FFPE
   samples" (CRC_DX).
2. **Neural Network Filtering**: Fused distillation framework votes on candidate patches for histopathological
   relevance.
3. **Expert Validation**: Board-certified pathologists incorporate morphology knowledge to select most representative
   samples.
4. **Label Assignment**: Patches tagged as MSIMUT_strong or MSS_strong based on consensus molecular status and visual
   relevance.
5. **Quality Assurance**: Final subset optimized for high-confidence model training on MSI prediction tasks.

#### 💡 Usage Notes

- ✅ Suitable for benchmarking deep learning models for microsatellite instability prediction from histopathology
- ✅ Curated "strong relevance" patches reduce background noise, enabling focused feature learning on discriminative
  morphological patterns
- ✅ Near-balanced class distribution (~51/49) supports stable binary classification training without aggressive
  resampling
- ✅ Serves as a high-quality subset for transfer learning or fine-tuning from the broader CRC_DX dataset
- 📚 Required to cite both this Zenodo repository and the parent CRC_DX dataset (DOI: 10.5281/zenodo.2530835) in
  derivative works
- 🔐 Distributed under CC BY 4.0; attribution required for redistribution or adaptation

#### ⚠️ Usage Considerations

| Aspect                      | Recommendation                                                                                                              |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **🔍 Subset Limitation**    | Curated for "strong relevance"; models trained here may not generalize to unfiltered WSIs without domain adaptation         |
| **🧪 Split Strategy**       | No predefined split; implement patient-aware or slide-aware partitioning to prevent data leakage                            |
| **🎨 Stain Variability**    | Apply stain normalization (e.g., Macenko method) if integrating with external cohorts                                       |
| **🔐 Ethical Compliance**   | Dataset contains de-identified human tissue; adhere to institutional review requirements                                    |
| **🧭 Clinical Translation** | MSI status prediction from H&E alone remains investigational; validate against molecular ground truth in clinical pipelines |
| **📦 Patch-Level Focus**    | Patches are extracted regions; whole-slide inference requires aggregation or multiple-instance learning strategies          |

#### 💡 Suggested Preprocessing Pipeline

1. **Extract archives**: Unzip `MSIMUT_strong.zip` and `MSS_strong.zip` into class-labeled directories.
2. **Standardize geometry**: Resize patches to uniform dimensions (e.g., 224×224 or 512×512) while preserving aspect
   ratio.
3. **Color normalization**: Apply stain normalization to mitigate inter-slide H&E staining variability.
4. **Stratified splitting**: Partition data by source slide or patient ID (if metadata available) to ensure no leakage
   between train/test sets.
5. **Augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering; preserve
   morphological integrity of glandular and stromal features.
6. **Class-balanced batching**: Leverage near-balanced distribution for stable training; monitor per-class metrics
   during validation.
7. **Evaluation metrics**: Report accuracy, sensitivity, specificity, AUC-ROC, and F1-score; include confusion matrices
   to assess MSI/MSS discrimination patterns.

#### 🔗 Associated Resources

- **Zenodo Repository**: https://doi.org/10.5281/zenodo.3692380
- **Parent Dataset **(CRC_DX): https://doi.org/10.5281/zenodo.2530835
- **Related Publications**:
    - Shen, Y. et al. (2020). "Histological images for MSI vs. MSS classification in gastrointestinal cancer, FFPE
      samples." Zenodo.
    - Relevant literature on MSI prediction from histopathology: e.g., Kather et al., *Nature Medicine* (2019); Echle et
      al., *Cancer Cell* (2021).
- **Related Datasets**:
    - [NCT-CRC-HE-100K](#-nct-crc-he-100k-100000-histological-images-of-human-colorectal-cancer-and-healthy-tissue) (
      tissue-type classification)
    - [CRC-HGD-v1](#-crc-hgd-v1-colorectal-cancer-histopathological-grading-dataset) (grading-focused)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{shen2020msimss,
    author = {Shen, Yiqing},
    title = {Strong histopathological relevance patches for MSI vs. MSS classification},
    year = {2020},
    publisher = {Zenodo},
    version = {1},
    doi = {10.5281/zenodo.3692380},
    url = {https://doi.org/10.5281/zenodo.3692380}
}

@dataset{shen2020crcdx,
    author = {Shen, Yiqing},
    title = {Histological images for MSI vs. MSS classification in gastrointestinal cancer, FFPE samples},
    year = {2020},
    publisher = {Zenodo},
    doi = {10.5281/zenodo.2530835},
    url = {https://doi.org/10.5281/zenodo.2530835}
}
```

---

### 🔬 CRC_DX: MSI vs. MSS Classification in Gastrointestinal Cancer

**Study**: Kather, J. N. (2019). Histological images for MSI vs. MSS classification in gastrointestinal cancer, FFPE
samples [Data set]. Zenodo.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                                     |
|-------------------------|---------------------------------------------------------------------------------------------|
| **📛 Title**            | Histological images for MSI vs. MSS classification in gastrointestinal cancer, FFPE samples |
| **🔗 Source**           | https://doi.org/10.5281/zenodo.2530835                                                      |
| **🦴 Target Organ**     | Colorectal / Gastric (Gastrointestinal)                                                     |
| **📅 Last Accessed**    | May 08, 2026                                                                                |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification (Microsatellite Status Prediction)                                |
| **📐 Image Size**       | 224 × 224 pixels @ 0.5 µm/pixel (fixed, color-normalized)                                   |
| **📁 Data Format**      | Image patches (format unspecified; typical: JPG/PNG), Macenko-normalized                    |
| **👥 Demographics**     | ❌ Not included (TCGA cohort; de-identified archival FFPE samples)                           |
| **🔄 Train/Test Split** | ✅ Yes (patient-wise ~70/30 split; training sets equilibrated by undersampling)              |

#### 📊 Dataset Composition

| Category                 | Details                                                                                          |
|--------------------------|--------------------------------------------------------------------------------------------------|
| **🖼️ Total Patches**    | 411,890 unique histopathological image patches                                                   |
| **🔬 Imaging Modality**  | Brightfield histopathology (H&E-stained FFPE tissue sections)                                    |
| **🌐 Source Cohort**     | The Cancer Genome Atlas (TCGA): Colorectal adenocarcinoma (COAD) + Stomach adenocarcinoma (STAD) |
| **🎨 Preprocessing**     | Tumor detection → 224×224 px @ 0.5 µm/px → Macenko color normalization                           |
| **📦 File Structure**    | 8 ZIP archives (~47.1 GB total); separated by cancer type, split, and class                      |
| **📅 Collection Period** | Archival TCGA samples; published February 2019                                                   |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification of microsatellite status in gastrointestinal cancer
- **Number of Classes**: 2️⃣

| Class Label | Description                                                       | Clinical Significance                                 |
|-------------|-------------------------------------------------------------------|-------------------------------------------------------|
| 🔴 MSS      | Microsatellite Stable: intact DNA mismatch repair system          | Standard chemotherapy indications                     |
| 🔵 MSIMUT   | Microsatellite Instable / Hypermutated: defective mismatch repair | Predicts immunotherapy response (e.g., pembrolizumab) |

**📊 Patch Distribution by Cancer Type and Split**:

**Gastric Cancer **(STAD)
| Split | Class | Patch Count | Notes |
|--------|---------|-------------|------------------------------------|
| Train | MSS | 50,285 | Equilibrated to match MSIMUT count |
| Train | MSIMUT | 50,285 | Equilibrated baseline |
| Test | MSS | 90,104 | Full test distribution |
| Test | MSIMUT | 27,904 | Reflects natural class imbalance |
| **STAD Total** | — | **218,578** | ~53.1% of dataset |

**Colorectal Cancer **(CRC_DX)
| Split | Class | Patch Count | Notes |
|--------|---------|-------------|------------------------------------|
| Train | MSS | 46,704 | Equilibrated to match MSIMUT count |
| Train | MSIMUT | 46,704 | Equilibrated baseline |
| Test | MSS | 70,569 | Full test distribution |
| Test | MSIMUT | 29,335 | Reflects natural class imbalance |
| **CRC_DX Total** | — | **193,312** | ~46.9% of dataset |

**📈 Overall Class Distribution**:
| Class | Total Patches | % of Dataset | Train (Equilibrated) | Test (Natural) |
|---------|---------------|--------------|---------------------|----------------|
| 🔴 MSS | 257,662 | ~62.6% | 96,989 (50%)        | 160,673 |
| 🔵 MSIMUT | 154,228 | ~37.4% | 96,989 (50%)        | 57,239 |
| **Total** | **411,890** | **100%**     | **193,978**         | **217,912**    |

> **ℹ️ Note**: Training sets were equilibrated via random undersampling of the majority MSS class to enable balanced
> model training. Test sets preserve natural class distribution for realistic performance evaluation. Patient-wise
> splitting prevents data leakage across train/test boundaries.

#### 🔧 Preprocessing Protocol (Applied by Authors)

1. **Tumor Region Detection**: Automated algorithm identifies tumor-containing regions in whole-slide images.
2. **Patch Extraction**: Sliding-window extraction of 224×224 pixel patches at 0.5 µm/pixel resolution.
3. **Color Normalization**: Macenko method applied to reduce inter-slide staining variability.
4. **Patient-Level Splitting**: ~70% of patients assigned to training, ~30% to testing (no patient overlap).
5. **Training Set Equilibration**: MSS class undersampled to match MSIMUT count within training sets.
6. **Quality Control**: Patches derived from diagnostic FFPE slides ("DX" at GDC portal); low-quality regions excluded.

#### 💡 Usage Notes

- ✅ Benchmark dataset for MSI status prediction from H&E histopathology in GI cancers
- ✅ Preprocessed, fixed-size, color-normalized patches enable direct integration with standard CNN architectures
- ✅ Patient-wise splitting supports rigorous evaluation of generalization to unseen patients
- ✅ Includes both colorectal and gastric cancer cohorts for cross-cancer generalization studies
- ✅ Parent dataset for the curated "MSI-MSS Strong Patches" subset (Zenodo: 10.5281/zenodo.3692380)
- 📚 Required to cite the original Zenodo repository and associated publications in derivative works
- 🔐 Distributed under CC BY 4.0; attribution required for redistribution or adaptation

#### ⚠️ Usage Considerations

| Aspect                            | Recommendation                                                                                                                |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance **(Test)     | Test sets reflect natural MSI prevalence (~37% MSIMUT); report balanced metrics (AUC, F1) alongside accuracy                  |
| **🧪 Cross-Cancer Analysis**      | STAD (gastric) and CRC_DX (colorectal) have distinct histomorphology; evaluate domain shift explicitly                        |
| **🎨 Stain Normalization**        | Macenko normalization already applied; additional normalization may be redundant unless integrating external data             |
| **🔐 Ethical Compliance**         | Derived from TCGA; adhere to TCGA data use agreements and institutional review requirements                                   |
| **🧭 Clinical Translation**       | MSI prediction from H&E remains investigational; validate against PCR/NGS molecular ground truth                              |
| **📦 Patch-to-Slide Aggregation** | Patches are tile-level; whole-slide or patient-level inference requires aggregation strategies (e.g., MIL, attention pooling) |

#### 💡 Suggested Preprocessing Pipeline

1. **Extract archives**: Unzip the 8 ZIP files into structured directories by cancer type, split, and class.
2. **Verify integrity**: Confirm patch counts match documentation; check for corrupted files.
3. **Standardize loading**: Use framework-native utilities (e.g., `torchvision.datasets.ImageFolder`) for class-labeled
   directories.
4. **Augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering; preserve glandular
   architecture.
5. **Stratified batching**: Leverage equilibrated training sets for stable binary classification; monitor per-class
   metrics.
6. **Cross-validation**: Implement patient-aware folds if re-splitting; maintain no patient overlap between folds.
7. **Evaluation metrics**: Report AUC-ROC, sensitivity, specificity, F1-score, and confusion matrices; include cancer
   type-stratified results.

#### 🔗 Associated Resources

- **Zenodo Repository**: https://doi.org/10.5281/zenodo.2530835
- **TCGA Data Portal**: https://portal.gdc.cancer.gov/ (original SVS whole-slide images)
- **Preprocessing Reference**: Macenko et al. (2009). "A method for normalizing histology slides for quantitative
  analysis." *ISBI*. [DOI](https://doi.org/10.1109/ISBI.2009.5193250)
- **FFPE Download Guide**: http://www.andrewjanowczyk.com/download-tcga-digital-pathology-images-ffpe/
- **Related Publications**:
    - Kather et al. (2019). "Pan-cancer image-based detection of clinically actionable genetic alterations." *Nature
      Cancer*.
    - Echle et al. (2021). "Clinical-grade detection of microsatellite instability in colorectal tumors by deep
      learning." *Gastroenterology*.
- **Related Datasets**:
    - [MSI-MSS Strong Patches](#-msi-mss-strong-patches-microsatellite-status-classification) (curated subset)
    - [NCT-CRC-HE-100K](#-nct-crc-he-100k-100000-histological-images-of-human-colorectal-cancer-and-healthy-tissue) (
      tissue-type classification)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{kather2019msimss,
    author = {Kather, Jakob Nikolas},
    title = {Histological images for MSI vs. MSS classification in gastrointestinal cancer, FFPE samples},
    year = {2019},
    publisher = {Zenodo},
    version = {v1},
    doi = {10.5281/zenodo.2530835},
    url = {https://doi.org/10.5281/zenodo.2530835}
}

@article{kather2019naturecancer,
    title = {Pan-cancer image-based detection of clinically actionable genetic alterations},
    author = {Kather, Jakob Nikolas and Heij, Lara R and Grabsch, Heike I and Loeffler, Clemens and Echle, Alexander and Muti, Halima S and Krause, Jeremias and Niehues, Jakob M and Sommer, Kai A and Bankhead, Peter and others},
    journal = {Nature Cancer},
    volume = {1},
    number = {8},
    pages = {789--799},
    year = {2020},
    publisher = {Nature Publishing Group},
    doi = {10.1038/s43018-020-0087-4}
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

*🕒 Last Updated: May 08, 2026*

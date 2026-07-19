# Medical AI Datasets Repository

<div align="center">

### 🏷️ Tasks

![Classification](https://img.shields.io/badge/🏷️_Classification-4CAF50?style=flat-square)
![Segmentation](https://img.shields.io/badge/🎭_Segmentation-FF9800?style=flat-square)
![Ordinal Classification](https://img.shields.io/badge/📊_Ordinal_Classification-8BC34A?style=flat-square)
![Localization](https://img.shields.io/badge/📍_Localization-00BCD4?style=flat-square)
![Time-Series](https://img.shields.io/badge/📈_Time--Series-009688?style=flat-square)

### 📡 Modalities

![Medical Imaging](https://img.shields.io/badge/🏥_Medical_Imaging-0288D1?style=flat-square)
![X-ray](https://img.shields.io/badge/🩻_X--ray-03A9F4?style=flat-square)
![CT Scan](https://img.shields.io/badge/🧊_CT_Scan-0277BD?style=flat-square)
![MRI](https://img.shields.io/badge/🧲_MRI-5E35B1?style=flat-square)
![OCT](https://img.shields.io/badge/👁️_OCT-8E24AA?style=flat-square)
![Fundus Photography](https://img.shields.io/badge/📸_Fundus-AB47BC?style=flat-square)
![Histopathology](https://img.shields.io/badge/🔬_Histopathology-9C27B0?style=flat-square)
![Microscopy](https://img.shields.io/badge/🧫_Microscopy-673AB7?style=flat-square)
![Clinical Data](https://img.shields.io/badge/📋_Clinical_Data-607D8B?style=flat-square)

### 🫀 Organs & Conditions

![Brain Tumor](https://img.shields.io/badge/🧠_Brain_Tumor-F44336?style=flat-square)
![Retina](https://img.shields.io/badge/👁️_Retina-E91E63?style=flat-square)
![Diabetic Retinopathy](https://img.shields.io/badge/🩸_Diabetic_Retinopathy-D81B60?style=flat-square)
![COVID-19](https://img.shields.io/badge/🦠_COVID--19-D32F2F?style=flat-square)
![Tuberculosis](https://img.shields.io/badge/🫁_Tuberculosis-C62828?style=flat-square)
![Pneumonia](https://img.shields.io/badge/🫁_Pneumonia-E53935?style=flat-square)
![Knee / Osteoarthritis](https://img.shields.io/badge/🦴_Knee_/_Osteoarthritis-795548?style=flat-square)
![Bone Tumor](https://img.shields.io/badge/🦴_Bone_Tumor-8D6E63?style=flat-square)
![Skin Lesions](https://img.shields.io/badge/🖼️_Skin_Lesions-FFC107?style=flat-square)
![Heart Disease](https://img.shields.io/badge/🫀_Heart_Disease-E91E63?style=flat-square)
![Kidney Cancer](https://img.shields.io/badge/🫘_Kidney_Cancer-FF5722?style=flat-square)
![Colorectal Cancer](https://img.shields.io/badge/🦴_Colorectal-FF7043?style=flat-square)
![Oral Cancer](https://img.shields.io/badge/🗣️_Oral_Cancer-E64A19?style=flat-square)
![Gastrointestinal](https://img.shields.io/badge/🩺_Gastrointestinal-BF360C?style=flat-square)
![Breast Cancer](https://img.shields.io/badge/🎀_Breast_Cancer-AD1457?style=flat-square)
![Urine / UTI](https://img.shields.io/badge/🧪_Urine_/_UTI-FFEB3B?style=flat-square)
![Diabetes](https://img.shields.io/badge/🩸_Diabetes-FF9800?style=flat-square)
![Veterinary](https://img.shields.io/badge/🐄_Veterinary-558B2F?style=flat-square)

</div>

## 📋 Dataset Summary

| Dataset                                                                                                                                               | Organ                     | Tasks                                                        | Classes                                                                                                                  | Split                                      | Last Accessed   | Quick Link                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|-----------------|-------------------------------------------------------------------------------------------------------|
| [🧠 BRISC 2025: Brain Tumor Segmentation & Classification](#-brisc-2025-annotated-dataset-for-brain-tumor-image-segmentation-and-classification)      | 🧠 Brain                  | 🏷️ Classification, 🎭 Segmentation                          | 4️⃣ Multiclass (Classification) / ⚪⚫ Binary (Segmentation)                                                               | ✅ Train/Test                               | 📅 Mar 28, 2026 | [🔗 Source](https://www.kaggle.com/datasets/briscdataset/brisc2025/)                                  |
| [🧠 Brain Tumor MRI Dataset](#-brain-tumor-mri-dataset-glioma-meningioma-pituitary-no-tumor)                                                          | 🧠 Brain                  | 🏷️ Classification                                           | 4️⃣ Multiclass (Glioma, Meningioma, Pituitary, No Tumor)                                                                 | ✅ Train/Test                               | 📅 Mar 28, 2026 | [🔗 Source](https://data.mendeley.com/datasets/zwr4ntf94j/4)                                          |
| [🦴 BTXRD: Bone Tumor X-ray Radiograph Dataset](#-btxrd-bone-tumor-x-ray-radiograph-dataset)                                                          | 🦴 Bone                   | 🏷️ Classification, 🎭 Segmentation, 📍 Localization         | Multiple (see details)                                                                                                   | ❌ No split                                 | 📅 Mar 28, 2026 | [🔗 Source](https://doi.org/10.6084/m9.figshare.27865398)                                             |
| [🔬 Dartmouth Kidney Cancer Histology Dataset](#-dartmouth-kidney-cancer-histology-dataset)                                                           | 🫘 Kidney                 | 🏷️ Classification                                           | 4️⃣ Multiclass (Renal Oncocytoma, Chromophobe RCC, Clear cell RCC, Papillary RCC)                                        | ✅ Train/Val/Test                           | 📅 Apr 11, 2026 | [🔗 Source](https://bmirds.github.io/KidneyCancer/)                                                   |
| [🔬 CRC-HGD-v1: Colorectal Cancer Histopathological Grading Dataset](#-crc-hgd-v1-colorectal-cancer-histopathological-grading-dataset)                | 🦴 Colorectal             | 🏷️ Classification (Grading)                                 | 3️⃣ Ordinal Multiclass (Grade I, Grade II, Grade III)                                                                    | ❌ No split                                 | 📅 Apr 11, 2026 | [🔗 Source](https://data.mendeley.com/datasets/yfp5sfj47m/2)                                          |
| [🔬 NCT-CRC-HE-100K: Colorectal Cancer Histology Patches](#-nct-crc-he-100k-100000-histological-images-of-human-colorectal-cancer-and-healthy-tissue) | 🦴 Colorectal             | 🏷️ Multiclass Classification                                | 9️⃣ Multiclass (ADI, BACK, DEB, LYM, MUC, MUS, NORM, STR, TUM)                                                           | ✅ Train/Val                                | 📅 Apr 12, 2026 | [🔗 Source](https://doi.org/10.5281/zenodo.1214456)                                                   |
| [🔬 Histopathological Imaging Database for Oral Cancer Analysis](#-histopathological-imaging-database-for-oral-cancer-analysis)                       | 🗣️ Oral Cavity           | 🏷️ Binary Classification                                    | 2️⃣ Binary (Normal Epithelium, OSCC)                                                                                     | ❌ No split                                 | 📅 Apr 11, 2026 | [🔗 Source](https://data.mendeley.com/datasets/ftmp4cvtmb/2)                                          |
| [🔬 DeepHisto: Glioma Subtype Classification from WSIs](#-deephisto-dataset-for-glioma-subtype-classification-from-whole-slide-images)                | 🧠 Brain                  | 🏷️ Classification                                           | 5️⃣ Multiclass (IDH-mutant oligodendroglioma, IDH-mutant astrocytoma, IDH-wildtype glioblastoma, Normal brain, Necrosis) | ✅ Train/Test (patient-wise)                | 📅 May 08, 2026 | [🔗 Source](https://doi.org/10.5281/zenodo.7941080)                                                   |
| [🔬 GastroVision: Gastrointestinal Disease Detection](#-gastrovision-gastrointestinal-disease-detection)                                              | 🩺 Gastrointestinal Tract | 🏷️ Classification                                           | 2️⃣7️⃣ Multiclass (Landmarks, abnormalities, polyps, cancer, normal findings)                                            | ❌ No split (user-defined)                  | 📅 May 08, 2026 | [🔗 Source](https://www.kaggle.com/datasets/orvile/gastrovision-gastrointestinal-disease-detection)   |
| [🔬 HER2-IHC-40x: HER2 Scoring in Breast Cancer](#-her2-ihc-40x-high-resolution-histopathology-image-dataset-for-her2-scoring-in-breast-cancer)       | 🫀 Breast                 | 🏷️ Classification                                           | 4️⃣ Ordinal Multiclass (HER2: 0, 1+, 2+, 3+)                                                                             | ✅ Train/Test (80/20, two split strategies) | 📅 May 08, 2026 | [🔗 Source](https://doi.org/10.5281/zenodo.15179608)                                                  |
| [🔬 MSI-MSS Strong Patches: Microsatellite Status Classification](#-msi-mss-strong-patches-microsatellite-status-classification)                      | 🦴 Colorectal             | 🏷️ Binary Classification                                    | 2️⃣ Binary (MSIMUT_strong, MSS_strong)                                                                                   | ❌ No split (user-defined)                  | 📅 May 08, 2026 | [🔗 Source](https://doi.org/10.5281/zenodo.3692380)                                                   |
| [🔬 CRC_DX: MSI vs. MSS Classification in GI Cancer](#-crc_dx-msi-vs-mss-classification-in-gastrointestinal-cancer)                                   | 🦴 Colorectal / Gastric   | 🏷️ Binary Classification                                    | 2️⃣ Binary (MSS, MSIMUT)                                                                                                 | ✅ Train/Test (patient-wise, ~70/30)        | 📅 May 08, 2026 | [🔗 Source](https://doi.org/10.5281/zenodo.2530835)                                                   |
| [🦴 Digital Knee X-ray Images: Knee Osteoarthritis Grading](#-digital-knee-x-ray-images-knee-osteoarthritis-grading)                                  | 🦴 Knee                   | 🏷️ Classification (Ordinal Grading)                         | 5️⃣ Ordinal Multiclass (K&L Grades 0–4: Normal, Doubtful, Mild, Moderate, Severe)                                        | ❌ No split (user-defined)                  | 📅 May 24, 2026 | [🔗 Source](https://www.kaggle.com/datasets/orvile/digital-knee-x-ray-images)                         |
| [👁️ Eyepacs, Aptos, Messidor Diabetic Retinopathy](#-eyepacs-aptos-messidor-diabetic-retinopathy-unified-dataset)                                    | 👁️ Retina                | 🏷️ Ordinal Classification (DR Grading)                      | 5️⃣ Ordinal Multiclass (DR Grades 0–4: None, Mild, Moderate, Severe, Proliferative)                                      | ✅ Train/Val/Test (80/10/10)                | 📅 May 24, 2026 | [🔗 Source](https://www.kaggle.com/datasets/ascanipek/eyepacs-aptos-messidor-diabetic-retinopathyy)   |
| [👁️ IDRiD: Diabetic Retinopathy – Grading](#-idrid-diabetic-retinopathy-grading-indian-dataset)                                                      | 👁️ Retina                | 🏷️ Ordinal Classification, 🎭 Segmentation, 📍 Localization | 5️⃣ DR Severity + 3️⃣ DME Severity (Ordinal Multiclass)                                                                  | ✅ Train/Test (413/103 for grading)         | 📅 May 24, 2026 | [🔗 Source](https://ieee-dataport.org/open-access/indian-diabetic-retinopathy-image-dataset-idrid)    |
| [🦠 Paratuberculosis Histopathology Images](#-paratuberculosis-histopathology-images-dataset)                                                         | 🐄 Intestine (Veterinary) | 🏷️ Binary Classification                                    | 2️⃣ Binary (Normal, Paratuberculosis-Positive)                                                                           | ❌ No split (user-defined)                  | 📅 May 24, 2026 | [🔗 Source](https://data.mendeley.com/datasets/zjhymwjtxv/3)                                          |
| [🫁 COVIDx CT: Large-Scale Chest CT for COVID-19](#-covidx-ct-a-large-scale-chest-ct-dataset-for-covid-19-detection)                                  | 🫁 Lungs / Chest          | 🏷️ Classification, 📍 Localization                          | 3️⃣ Multiclass (Normal, Pneumonia, COVID-19)                                                                             | ✅ Train/Val/Test                           | 📅 Jun 20, 2026 | [🔗 Source](https://www.kaggle.com/datasets/haydengunraj/covidx-ct)                                   |
| [🧠 Brain Tumor Dataset (Jun Cheng)](#-brain-tumor-dataset-jun-cheng)                                                                                 | 🧠 Brain                  | 🏷️ Classification                                           | 3️⃣ Multiclass (Meningioma, Glioma, Pituitary)                                                                           | ✅ Cross-validation (cvind.mat)             | 📅 Jun 20, 2026 | [🔗 Source](https://doi.org/10.6084/m9.figshare.1512427)                                              |
| [🫁 Sakha-TB](#-sakha-tb)                                                                                                                             | 🫁 Lungs / Chest          | 🏷️ Binary Classification                                    | 2️⃣ Binary (Normal, Tuberculosis)                                                                                        | ❌ No split                                 | 📅 Jun 24, 2026 | [🔗 Source](#)                                                                                        |
| [🫁 Tuberculosis (TB) Chest X-ray Database](#-tuberculosis-tb-chest-x-ray-database)                                                                   | 🫁 Lungs / Chest          | 🏷️ Binary Classification                                    | 2️⃣ Binary (Normal, Tuberculosis)                                                                                        | ❌ No split                                 | 📅 Jun 24, 2026 | [🔗 Source](https://www.kaggle.com/datasets/tawsifurrahman/tuberculosis-tb-chest-xray-database)       |
| [👁️🫁 Labeled OCT and Chest X-Ray Images](#-labeled-optical-coherence-tomography-oct-and-chest-x-ray-images-for-classification)                      | 👁️ Eye / 🫁 Lungs        | 🏷️ Multiclass Classification                                | 4️⃣ Multiclass (CNV, DME, DRUSEN, NORMAL)                                                                                | ✅ Train/Test                               | 📅 Jun 24, 2026 | [🔗 Source](https://data.mendeley.com/datasets/rscbjbr9sj/2)                                          |
| [🫁 CheXpert: A Large Chest Radiograph Dataset](#-chexpert-a-large-chest-radiograph-dataset-with-uncertainty-labels-and-expert-comparison)            | 🫁 Lungs / Chest          | 🏷️ Multiclass / Multi-label Classification                  | 14️⃣ Multi-label (14 Observations)                                                                                       | ✅ Train/Val/Test                           | 📅 Jun 26, 2026 | [🔗 Source](https://stanfordmlgroup.github.io/competitions/chexpert/)                                 |
| [🫁 COVID-19 Radiography Database](#-covid-19-radiography-database)                                                                                   | 🫁 Lungs / Chest          | 🏷️ Multiclass Classification, 🎭 Segmentation               | 4️⃣ Multiclass (COVID-19, Lung Opacity, Normal, Viral Pneumonia)                                                         | ❌ No split                                 | 📅 Jun 26, 2026 | [🔗 Source](https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database)              |
| [👁️ Ocular Disease Recognition (ODIR-5K)](#-ocular-disease-recognition-odir-5k)                                                                      | 👁️ Eye (Retina)          | 🏷️ Multiclass / Multi-label Classification                  | 8️⃣ Multi-label (Normal, Diabetes, Glaucoma, Cataract, AMD, Hypertension, Myopia, Other)                                 | ❌ No split                                 | 📅 Jun 30, 2026 | [🔗 Source](https://www.kaggle.com/datasets/andrewmvd/ocular-disease-recognition-odir5k)              |
| [🖼️ ISIC 2019: Skin Lesion Analysis](#-isic-2019-skin-lesion-analysis-toward-melanoma-detection)                                                     | 🖼️ Skin                  | 🏷️ Multiclass Classification                                | 8️⃣ Multiclass (MEL, NV, BCC, AK, BKL, DF, VASC, SCC)                                                                    | ✅ Train/Test                               | 📅 Jun 30, 2026 | [🔗 Source](https://challenge.isic-archive.com/data/#2019)                                            |
| [🧪 Clinical Urine Microscopy](#-clinical-urine-microscopy-for-urinary-tract-infections)                                                              | 🧪 Urine / Cellular       | 🎭 Semantic Segmentation (Binary & Multi-class)              | 7️⃣ Multi-class (Rod, RBC/WBC, Yeast, Miscellaneous, Single EPC, Small/Large EPC sheet)                                  | ❌ No split                                 | 📅 Jun 30, 2026 | [🔗 Source](https://rodare.hzdr.de/record/2473)                                                       |
| [❤️ Heart Failure Prediction Dataset](#-heart-failure-prediction-dataset)                                                                             | ❤️ Heart / Cardiovascular | 🏷️ Binary Classification                                    | 2️⃣ Binary (Heart Disease, Normal)                                                                                       | ❌ No split                                 | 📅 Jun 30, 2026 | [🔗 Source](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)                     |
| [❤️ Heart Attack Analysis & Prediction](#-heart-attack-analysis--prediction-dataset)                                                                  | ❤️ Heart / Cardiovascular | 🏷️ Binary Classification                                    | 2️⃣ Binary (Heart Attack, Normal)                                                                                        | ❌ No split                                 | 📅 Jun 30, 2026 | [🔗 Source](https://www.kaggle.com/datasets/sonialikhan/heart-attack-analysis-and-prediction-dataset) |
| [🖼️ PAD-UFES-20: Skin Lesion Dataset](#-pad-ufes-20-skin-lesion-dataset)                                                                             | 🖼️ Skin                  | 🏷️ Multiclass Classification                                | 6️⃣ Multiclass (BCC, SCC, ACK, SEK, MEL, NEV)                                                                            | ❌ No split                                 | 📅 Jun 30, 2026 | [🔗 Source](https://data.mendeley.com/datasets/zr7vgbcyr2/1)                                          |
| [🩸 Diabetes Dataset (AIM '94)](#-diabetes-dataset-aim-94)                                                                                            | 🩸 Blood / Metabolic      | 📊 Time-Series Analysis                                      | N/A (Time-series of glucose/insulin)                                                                                     | ❌ No split                                 | 📅 Jun 30, 2026 | [🔗 Source](https://archive.ics.uci.edu/dataset/34/diabetes)                                          |
| [🫀 Digital Pathology Dataset for Breast Cancer Diagnosis](#-digital-pathology-dataset-for-breast-cancer-diagnosis)                                   | 🫀 Breast                 | 🎭 Segmentation (Tissue Region)                              | N/A (WSI Tissue Segmentation)                                                                                            | ❌ No split                                 | 📅 Jul 03, 2026 | [🔗 Source](https://zenodo.org/records/14131968)                                                      |
| [🫀 2M Breast Cancer Tumors with HER2 Labels](#-2-million-histological-images-of-breast-cancer-tumors-with-her2-labels)                               | 🫀 Breast                 | 🏷️ Multiclass Classification (HER2 Status)                  | 3️⃣ Multiclass (HER2-negative, HER2-low, HER2-high)                                                                      | ❌ No split                                 | 📅 Jul 03, 2026 | [🔗 Source](https://zenodo.org/records/8383580)                                                       |
| [🫀 Breast Carcinoma Histological Images (Agios Pavlos)](#-breast-carcinoma-histological-images-agios-pavlos-hospital)                                | 🫀 Breast                 | 🏷️ Ordinal Classification (Tumor Grading)                   | 3️⃣ Ordinal Multiclass (Grade 1, Grade 2, Grade 3)                                                                       | ❌ No split                                 | 📅 Jul 03, 2026 | [🔗 Source](https://zenodo.org/records/834910)                                                        |
| [🧠 Brain Tumor Multimodal Image (CT & MRI)](#-brain-tumor-multimodal-image-ct--mri)                                                                  | 🧠 Brain                  | 🏷️ Classification, 🎭 Segmentation                          | Multiple (Glioma, Meningioma, etc.)                                                                                      | ❌ No split (user-defined)                  | 📅 Jul 19, 2026 | [🔗 Source](https://www.kaggle.com/datasets/golammurtoza/brain-tumor-multimodal-image-ct-mri)         |
| [🧠 Brain Tumor MRI Dataset (Nickparvar)](#-brain-tumor-mri-dataset-nickparvar)                                                                       | 🧠 Brain                  | 🏷️ Classification                                           | 4️⃣ Multiclass (Glioma, Meningioma, Pituitary, No Tumor)                                                                 | ✅ Train/Test (5,600 / 1,600)               | 📅 Jul 19, 2026 | [🔗 Source](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset)                 |

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

@article{kather2020pan,
    title = {Pan-cancer image-based detection of clinically actionable genetic alterations},
    author = {Kather, Jakob Nikolas and Heij, Lara R and Grabsch, Heike I and Loeffler, Chiara and Echle, Amelie and Muti, Hannah Sophie and Krause, Jeremias and Niehues, Jan M and Sommer, Kai AJ and Bankhead, Peter and others},
    journal = {Nature cancer},
    volume = {1},
    number = {8},
    pages = {789--799},
    year = {2020},
    publisher = {Nature Publishing Group US New York},
    doi = {10.1038/s43018-020-0087-4}
}
```

---

### 🦴 Digital Knee X-ray Images: Knee Osteoarthritis Grading

**Study**: Gornale, S., & Patravali, P. (2020). Digital Knee X-ray Images. Mendeley Data, V1.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                           |
|-------------------------|-----------------------------------------------------------------------------------|
| **📛 Title**            | Digital Knee X-ray Images: Knee Osteoarthritis Grading                            |
| **🔗 Source**           | https://www.kaggle.com/datasets/orvile/digital-knee-x-ray-images                  |
| **🦴 Target Organ**     | Knee Joint                                                                        |
| **📅 Last Accessed**    | May 24, 2026                                                                      |
| **🎯 Supported Tasks**  | 🏷️ Ordinal Classification (Kellgren–Lawrence Grading)                            |
| **📐 Image Size**       | Variable (8-bit grayscale; original acquisition via PROTEC PRS 500E)              |
| **📁 Data Format**      | JPEG/PNG (.jpg/.png); annotations in filenames or `Digital Knee X-ray Images.csv` |
| **👥 Demographics**     | ❌ Not included (de-identified clinical images)                                    |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                            |

#### 📊 Dataset Composition

| Category                  | Details                                                           |
|---------------------------|-------------------------------------------------------------------|
| **🖼️ Total Images**      | 1,650 digital knee X-ray images                                   |
| **🏥 Imaging Modality**   | Radiographic X-ray (anteroposterior knee views)                   |
| **🎨 Color Format**       | Grayscale, 8-bit depth                                            |
| **📦 Total Size**         | ~121.67 MB (compressed)                                           |
| **🏫 Source Institution** | Rani Channamma University, India                                  |
| **👨‍⚕️ Annotation**      | Dual-expert labeling using Kellgren–Lawrence (K&L) grading system |

#### 🏷️ Classification Task Details

- **Task Type**: Ordinal multiclass classification of knee osteoarthritis severity
- **Number of Classes**: 5️⃣ (ordered severity scale per Kellgren–Lawrence criteria) [[9]]

| K&L Grade | Label    | Description                                                                  | Image Count (MedicalExpert-I) |
|-----------|----------|------------------------------------------------------------------------------|-------------------------------|
| 🔘 0      | Normal   | No radiographic features of OA                                               | 514                           |
| 🟡 1      | Doubtful | Doubtful joint space narrowing, possible osteophytes                         | 477                           |
| 🟠 2      | Mild     | Definite osteophytes, possible joint space narrowing                         | 232                           |
| 🔴 3      | Moderate | Multiple osteophytes, definite joint space narrowing, sclerosis              | 221                           |
| ⚫ 4       | Severe   | Large osteophytes, marked joint space narrowing, severe sclerosis, deformity | 206                           |

**📊 Annotation Protocol**:

- Each image manually labeled by **two independent medical experts** using the Kellgren–Lawrence grading system [[2]]
- Annotations stored either in image filenames or in the companion metadata file `Digital Knee X-ray Images.csv`
- Dataset includes two expert annotation directories: `MedicalExpert-I` and `MedicalExpert-II` for inter-rater
  reliability studies

#### 💡 Usage Notes

- ✅ Suitable for benchmarking ordinal classification models for automated OA severity grading
- ✅ Dual-expert annotations enable research on annotation uncertainty and consensus modeling
- ✅ Includes cartilage region-of-interest (ROI) extraction methodology based on pixel density analysis [[5]]
- ✅ Organized directory structure enables direct integration with standard deep learning data loaders
- 📚 Required to cite the original Mendeley Data repository (DOI: 10.17632/t9ndx37v5h.1) in publications [[14]]
- 🔐 Distributed under CC BY 4.0; attribution required for redistribution or adaptation

#### ⚠️ Usage Considerations

| Aspect                       | Recommendation                                                                             |
|------------------------------|--------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**       | Grades 0–1 dominate (~60%); consider stratified sampling or class-weighted loss            |
| **🧪 Ordinal Structure**     | Grades represent ordered severity; consider ordinal regression or monotonic constraints    |
| **📐 Resolution Handling**   | Images vary in dimensions; apply uniform resizing prior to model ingestion                 |
| **🔐 Ethical Compliance**    | Dataset contains de-identified patient images; adhere to institutional review requirements |
| **🧭 Domain Generalization** | Single-region sourcing (India); validate on external cohorts for clinical deployment       |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Utilize framework-native utilities (e.g., `torchvision.datasets.ImageFolder`) to ingest
   grade-labeled subfolders.
2. **Standardize input format**: Convert all images to fixed resolution (e.g., 224×224 or 512×512) while preserving
   aspect ratio.
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide statistics.
4. **Augmentation **(training only): Incorporate rotation, flipping, and mild intensity jittering; avoid transformations
   that distort anatomical landmarks.
5. **Ordinal encoding**: Encode K&L grades as ordered integers (0–4) or use one-hot vectors with ordinal constraints.
6. **Stratified evaluation**: Report per-grade precision, recall, F1-score, and ordinal-aware metrics (e.g., weighted
   kappa, mean absolute error).

#### 🔗 Associated Resources

- **Kaggle Repository**: https://www.kaggle.com/datasets/orvile/digital-knee-x-ray-images
- **Mendeley Data **(Primary Source): https://data.mendeley.com/datasets/t9ndx37v5h/1 [[5]]
- **Related Publications**:
    - Gornale, S. S., Patravali, P. U., & Hiremath, P. S. (2020). A Comprehensive Digital Knee X-ray Image Dataset for
      the Assessment of Osteoarthritis. *JSM Biomedical Imaging Data Papers*.
    - Kellgren, J. H., & Lawrence, J. S. (1957). Radiological assessment of osteo-arthrosis. *Annals of the Rheumatic
      Diseases*.
- **Related Datasets**:
    - [Knee Osteoarthritis Dataset with KL Grading - 2018](https://www.kaggle.com/datasets/tommyngx/knee-osteoarthritis-dataset-with-kl-grading-2018)
    - [Multi-Class Knee Osteoporosis X-Ray Dataset](https://www.kaggle.com/datasets/mohamedgobara/multi-class-knee-osteoporosis-x-ray-dataset)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{gornale2020digitalknee,
    author = {Gornale, Shivanand and Patravali, Pooja},
    title = {Digital Knee X-ray Images},
    year = {2020},
    publisher = {Mendeley Data},
    version = {1},
    doi = {10.17632/t9ndx37v5h.1},
    url = {https://doi.org/10.17632/t9ndx37v5h.1}
}
```

---

### 👁️ Eyepacs, Aptos, Messidor Diabetic Retinopathy: Unified Dataset

**Study**: Canipek, A. S., et al. (2024). Eyepacs, Aptos, Messidor Diabetic Retinopathy. Kaggle.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                                |
|-------------------------|----------------------------------------------------------------------------------------|
| **📛 Title**            | Eyepacs, Aptos, Messidor Diabetic Retinopathy: Unified Dataset                         |
| **🔗 Source**           | https://www.kaggle.com/datasets/ascanipek/eyepacs-aptos-messidor-diabetic-retinopathyy |
| **👁️ Target Organ**    | Retina / Fundus                                                                        |
| **📅 Last Accessed**    | May 24, 2026                                                                           |
| **🎯 Supported Tasks**  | 🏷️ Ordinal Classification (Diabetic Retinopathy Grading)                              |
| **📐 Image Size**       | 600 × 600 pixels (uniformly resized; original sources variable)                        |
| **📁 Data Format**      | JPEG (.jpg); labels encoded in directory structure                                     |
| **👥 Demographics**     | ❌ Not included (de-identified clinical fundus images)                                  |
| **🔄 Train/Test Split** | ✅ Yes (80% Train / 10% Validation / 10% Test; random stratified split)                 |

#### 📊 Dataset Composition

| Category                   | Details                                                            |
|----------------------------|--------------------------------------------------------------------|
| **🖼️ Total Images**       | 143,669 fundus photographs (after Jan 2024 augmentation)           |
| **🔬 Imaging Modality**    | Color fundus photography (retinal imaging)                         |
| **🎨 Color Format**        | RGB, 8-bit per channel                                             |
| **📦 Total Size**          | ~3.8 GB (compressed; reduced from 18.5 GB via resizing)            |
| **🏥 Source Institutions** | Multi-source: EyePACS, APTOS 2019, Messidor consortium             |
| **👨‍⚕️ Annotation**       | Expert ophthalmologist-graded diabetic retinopathy severity labels |

#### 🏷️ Classification Task Details

- **Task Type**: Ordinal multiclass classification of diabetic retinopathy (DR) severity
- **Number of Classes**: 5️⃣ (ordered severity scale per clinical DR grading standards)

| DR Grade | Label            | Description                                        | Clinical Interpretation             |
|----------|------------------|----------------------------------------------------|-------------------------------------|
| 🔘 0     | No DR            | No visible signs of diabetic retinopathy           | Normal retinal appearance           |
| 🟡 1     | Mild DR          | Microaneurysms only                                | Early non-proliferative changes     |
| 🟠 2     | Moderate DR      | Microaneurysms + hemorrhages/exudates              | Moderate non-proliferative DR       |
| 🔴 3     | Severe DR        | Extensive hemorrhages, venous beading, IRMA        | Severe non-proliferative DR         |
| ⚫ 4      | Proliferative DR | Neovascularization, vitreous/preretinal hemorrhage | Vision-threatening proliferative DR |

**📊 Dataset Distribution **(Post-Augmentation)

| Split         | Percentage | Approx. Image Count | Purpose                               |
|---------------|------------|---------------------|---------------------------------------|
| 🟢 Train      | 80%        | ~114,935            | Model training and development        |
| 🟡 Validation | 10%        | ~14,367             | Hyperparameter tuning, early stopping |
| 🔴 Test       | 10%        | ~14,367             | Final performance evaluation          |
| **Total**     | **100%**   | **143,669**         | —                                     |

> **ℹ️ Note**: Class distribution reflects real-world clinical prevalence (No DR and Mild DR typically dominate).
> Stratified sampling or class-weighted loss functions are recommended during training.

#### 🔧 Preprocessing & Augmentation Protocol (Jan 2024 Update)

1. **Source Integration**: Images aggregated from EyePACS, APTOS 2019, APTOS Gaussian Filtered, and Messidor databases.
2. **Uniform Resizing**: All images resized to 600×600 pixels to standardize input dimensions and reduce storage
   footprint.
3. **Manual Data Augmentation**: Applied geometric and photometric transformations to increase dataset size by ~55%.
4. **Stratified Splitting**: Random 80:10:10 train/val/test split preserved post-augmentation to maintain class balance.
5. **Directory Organization**: Images organized into class-labeled subdirectories within `train/`, `val/`, and `test/`
   folders.

#### 💡 Usage Notes

- ✅ Suitable for benchmarking deep learning models for automated diabetic retinopathy screening
- ✅ Large-scale, multi-source composition supports research on domain generalization across imaging protocols
- ✅ Pre-resized and augmented format reduces preprocessing overhead during model development
- ✅ Predefined stratified splits enable reproducible benchmarking and fair model comparison
- 📚 Required to cite both this Kaggle repository **and** all original source datasets in publications
- ⚠️ **Critical**: Users must review and comply with the licenses and terms of use of each original dataset (EyePACS,
  APTOS, Messidor) before commercial or clinical deployment

#### ⚠️ Usage Considerations

| Aspect                        | Recommendation                                                                                                                |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**        | No DR and Mild DR classes typically dominate; apply class-weighted loss or focal loss                                         |
| **🎨 Source Heterogeneity**   | Images originate from multiple devices/protocols; consider domain adaptation techniques                                       |
| **🧪 Ordinal Structure**      | DR grades represent ordered severity; consider ordinal regression or monotonic constraints                                    |
| **🔐 Licensing Compliance**   | Messidor database has specific usage restrictions; verify terms at official source before redistribution                      |
| **🧭 Clinical Translation**   | Model performance on this curated dataset may not directly translate to real-world screening; validate on prospective cohorts |
| **📦 Augmentation Awareness** | Augmented samples are derived from original images; ensure train/test splits prevent leakage of augmented variants            |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Utilize framework-native utilities (e.g., `torchvision.datasets.ImageFolder`) to ingest
   class-labeled subfolders.
2. **Standardize input format**: Confirm uniform 600×600 dimensions; resize if model architecture requires different
   input sizes.
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using ImageNet statistics if using
   pretrained backbones.
4. **Augmentation **(training only): Incorporate additional rotation, flipping, color jittering, and CutMix/MixUp to
   further improve generalization.
5. **Ordinal encoding**: Encode DR grades as ordered integers (0–4) or use one-hot vectors with ordinal constraints.
6. **Stratified evaluation**: Report per-class precision, recall, F1-score, and ordinal-aware metrics (e.g., weighted
   kappa, quadratic weighted kappa).
7. **Source-aware validation **(optional): If source metadata is available, evaluate cross-source generalization by
   holding out one source for testing.

#### 🔗 Associated Resources

- **Kaggle Repository**: https://www.kaggle.com/datasets/ascanipek/eyepacs-aptos-messidor-diabetic-retinopathyy
- **Original Data Sources**:
    - EyePACS / Kaggle Diabetic Retinopathy
      Detection: https://www.kaggle.com/competitions/diabetic-retinopathy-detection
    - APTOS 2019 Blindness Detection: https://www.kaggle.com/competitions/aptos2019-blindness-detection
    - Messidor Database: https://www.adcis.net/en/third-party/messidor/
- **Related Publications**:
    - Decencière, E., et al. (2014). Feedback on a publicly distributed database: the Messidor database. *Image
      Analysis & Stereology*, 33(3), 231–234.
    - Gulshan, V., et al. (2016). Development and Validation of a Deep Learning Algorithm for Detection of Diabetic
      Retinopathy in Retinal Fundus Photographs. *JAMA*.
- **Related Datasets**:
    - [IDRiD: Diabetic Retinopathy – Grading](https://www.kaggle.com/datasets/sovitrath/idrid-diabetic-retinopathy-grading)
    - [APTOS 2019 Blindness Detection](https://www.kaggle.com/competitions/aptos2019-blindness-detection)
    - [DR_MASTER: Multi-Source DR Grading Dataset](https://www.kaggle.com/datasets/harshitkulkarni07/dr-master-multi-source-dr-grading-dataset)

#### 📚 Citation

If you use this dataset, please cite **both** this unified repository **and** all original source datasets:

```bibtex
@dataset{canipek2024eyepacsaptosmessidor,
    author = {Çakan, Metehan and Aktuğ, Aleyna},
    title = {Eyepacs, Aptos, Messidor Diabetic Retinopathy},
    year = {2024},
    publisher = {Kaggle},
    url = {https://www.kaggle.com/datasets/ascanipek/eyepacs-aptos-messidor-diabetic-retinopathyy},
    note = {Accessed: May 24, 2026}
}

@article{decenciere2014feedback,
    title = {Feedback on a publicly distributed image database: the Messidor database},
    author = {Decenci{\`e}re, Etienne and Zhang, Xiwei and Cazuguel, Guy and Lay, Bruno and Cochener, B{\'e}atrice and Trone, Caroline and Gain, Philippe and Ord{\'o}{\~n}ez-Varela, John-Richard and Massin, Pascale and Erginay, Ali and others},
    journal = {Image Analysis \& Stereology},
    pages = {231--234},
    year = {2014}
}

@misc{eyepacs2015,
    title = {EyePACS: A Platform for Diabetic Retinopathy Screening},
    author = {EyePACS},
    year = {2015},
    url = {https://www.eyepacs.com/},
    note = {Accessed: May 24, 2026}
}

@misc{aptos2019,
    title = {APTOS 2019 Blindness Detection},
    author = {Asia Pacific Tele-Ophthalmology Society},
    year = {2019},
    publisher = {Kaggle},
    url = {https://www.kaggle.com/competitions/aptos2019-blindness-detection},
    note = {Accessed: May 24, 2026}
}
```

---

### 👁️ IDRiD: Diabetic Retinopathy – Grading (Indian Dataset)

**Study**: Porwal, P., Pachade, S., Kamble, R., Kokare, M., Deshmukh, G., Sahasrabuddhe, V., & Meriaudeau, F. (2018).
Indian Diabetic Retinopathy Image Dataset (IDRiD). IEEE DataPort.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                               |
|-------------------------|---------------------------------------------------------------------------------------|
| **📛 Title**            | IDRiD: Diabetic Retinopathy – Grading (Indian Dataset)                                |
| **🔗 Source**           | https://ieee-dataport.org/open-access/indian-diabetic-retinopathy-image-dataset-idrid |
| **👁️ Target Organ**    | Retina / Fundus                                                                       |
| **📅 Last Accessed**    | May 24, 2026                                                                          |
| **🎯 Supported Tasks**  | 🏷️ Ordinal Classification, 🎭 Segmentation, 📍 Localization                          |
| **📐 Image Size**       | 4288 × 2848 pixels (native); 50º field of view                                        |
| **📁 Data Format**      | JPG (fundus images), TIFF (segmentation masks), CSV (labels)                          |
| **👥 Demographics**     | ❌ Not included (de-identified clinical images from Indian population)                 |
| **🔄 Train/Test Split** | ✅ Yes (Grading: 413 Train / 103 Test; Segmentation: variable split)                   |

#### 📊 Dataset Composition

| Category                  | Details                                                                             |
|---------------------------|-------------------------------------------------------------------------------------|
| **🖼️ Total Images**      | 516 color fundus photographs (Disease Grading task)                                 |
| **🔬 Imaging Modality**   | Color fundus photography (retinal imaging)                                          |
| **🎨 Color Format**       | RGB, high-resolution (4288 × 2848 pixels)                                           |
| **📦 Total Size**         | ~962 MB compressed (three ZIP archives: Segmentation, Grading, Localization)        |
| **🏥 Source Institution** | Medical research centers in India                                                   |
| **👨‍⚕️ Annotation**      | Expert ophthalmologist-annotated lesions, severity grades, and anatomical landmarks |

#### 🏷️ Classification Task Details (Disease Grading)

- **Task Type**: Ordinal multiclass classification of diabetic retinopathy (DR) and diabetic macular edema (DME)
  severity
- **Number of Classes**:
    - **DR Severity**: 5️⃣ ordinal grades (0–4)
    - **DME Severity**: 3️⃣ ordinal grades (0–2)

**📊 Diabetic Retinopathy (DR) Severity Grades**:

| Grade | Label            | Description                                        |
|-------|------------------|----------------------------------------------------|
| 🔘 0  | No DR            | No visible signs of diabetic retinopathy           |
| 🟡 1  | Mild DR          | Microaneurysms only                                |
| 🟠 2  | Moderate DR      | Microaneurysms + hemorrhages/exudates              |
| 🔴 3  | Severe DR        | Extensive hemorrhages, venous beading, IRMA        |
| ⚫ 4   | Proliferative DR | Neovascularization, vitreous/preretinal hemorrhage |

**📊 Diabetic Macular Edema (DME) Severity Grades**:

| Grade | Label    | Description                 |
|-------|----------|-----------------------------|
| 🔘 0  | No DME   | No macular edema present    |
| 🟡 1  | Presence | Macular edema present       |
| 🟠 2  | Scarring | Macular edema with scarring |

**📊 Dataset Distribution **(Grading Task)

| Split     | Image Count | Purpose                        |
|-----------|-------------|--------------------------------|
| 🟢 Train  | 413         | Model training and development |
| 🔴 Test   | 103         | Final performance evaluation   |
| **Total** | **516**     | —                              |

#### 🎭 Segmentation Task Details

- **Task Type**: Binary semantic segmentation of retinal lesions and anatomical structures
- **Annotation Targets**:
    - 🩸 Microaneurysms (MA)
    - 🔴 Haemorrhages (HE)
    - 💎 Hard Exudates (EX)
    - ☁️ Soft Exudates / Cotton Wool Spots (SE)
    - ⚪ Optic Disc (OD)

**📊 Segmentation Dataset Distribution**:

| Component        | Image Count | Format | Description                  |
|------------------|-------------|--------|------------------------------|
| Fundus Images    | 81          | JPG    | High-resolution color images |
| Lesion Masks     | 81          | TIFF   | Pixel-level binary masks     |
| Optic Disc Masks | 81          | TIFF   | Pixel-level binary masks     |

> **ℹ️ Note**: Segmentation masks are provided as single-channel TIFF files with white foreground (lesion/structure) on
> black background.

#### 📍 Localization Task Details

- **Task Type**: Keypoint detection / coordinate regression for anatomical landmarks
- **Annotation Targets**:
    - 🎯 Optic Disc Center (x, y coordinates)
    - 🎯 Fovea Center (x, y coordinates)

**📊 Localization Dataset Distribution**:

| Component            | Image Count | Format | Description                    |
|----------------------|-------------|--------|--------------------------------|
| Fundus Images        | 516         | JPG    | High-resolution color images   |
| Landmark Coordinates | 516         | CSV    | Pixel coordinates for OD/Fovea |

#### 💡 Usage Notes

- ✅ First publicly available retinal dataset representative of Indian population demographics
- ✅ Only dataset providing pixel-level annotations for both DR lesions **and** normal retinal structures
- ✅ Multi-task design supports joint learning of classification, segmentation, and localization
- ✅ High-resolution native images (4288×2848) enable research on fine-grained lesion detection
- ✅ Official train/test splits enable reproducible benchmarking across research groups
- 📚 Required to cite the original IEEE DataPort repository and associated publications
- 🔐 Distributed under IEEE DataPort Open Access terms; verify usage rights before commercial deployment

#### ⚠️ Usage Considerations

| Aspect                       | Recommendation                                                                                      |
|------------------------------|-----------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**       | DR grades 0–2 typically dominate; apply stratified sampling or class-weighted loss                  |
| **📐 Resolution Handling**   | Native 4288×2848 images require substantial memory; consider patch-based processing or downsampling |
| **🧪 Multi-Task Learning**   | Tasks share input images but have independent labels; design architectures accordingly              |
| **🔐 Licensing Compliance**  | Verify IEEE DataPort terms; original challenge data may have specific usage restrictions            |
| **🧭 Domain Generalization** | Indian population representation is valuable but may require validation on other ethnic cohorts     |
| **🎨 Annotation Format**     | Segmentation masks use TIFF format; ensure proper library support for loading multi-channel masks   |

#### 💡 Suggested Preprocessing Pipeline

1. **Download and extract**: Obtain all three ZIP archives (Segmentation, Grading, Localization) from IEEE DataPort.
2. **Parse metadata**: Load CSV label files to map image filenames to DR grade, DME grade, and landmark coordinates.
3. **Standardize resolution**: Resize high-resolution images to model-compatible dimensions (e.g., 512×512 or 1024×1024)
   while preserving aspect ratio.
4. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide statistics;
   consider CLAHE for contrast enhancement.
5. **Load segmentation masks**: Use libraries supporting TIFF format (e.g., `tifffile`, `Pillow`) to read binary
   annotation masks.
6. **Coordinate normalization**: Convert landmark coordinates from pixel space to normalized [0, 1] range if required by
   model architecture.
7. **Stratified evaluation**: Report per-class metrics for DR/DME grading; compute Dice/IoU for segmentation; measure
   Euclidean error for localization.

#### 🔗 Associated Resources

- **IEEE DataPort Repository**: https://ieee-dataport.org/open-access/indian-diabetic-retinopathy-image-dataset-idrid
- **Kaggle Mirror**: https://www.kaggle.com/datasets/mariaherrerot/idrid-dataset
- **Grand Challenge Website**: https://idrid.grand-challenge.org/
- **ISBI 2018 Challenge**: https://biomedicalimaging.org/2018/challenges/
- **Data Descriptor Publication**: Porwal, P., et al. (2018). "IDRiD: Diabetic Retinopathy Segmentation and Grading
  Challenge." *Medical Image Analysis*.
- **Related Datasets**:
    - [Messidor-2](https://www.adcis.net/en/third-party/messidor/) (French cohort, DR grading)
    - [RFMiD](https://ieee-dataport.org/documents/retinal-fundus-multi-disease-image-dataset-rfmid) (Multi-disease
      retinal dataset)
    - [APTOS 2019](https://www.kaggle.com/competitions/aptos2019-blindness-detection) (Blindness detection challenge)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{porwal2018idrid,
    author = {Porwal, Prasanna and Pachade, Samiksha and Kamble, Ravi and Kokare, Manesh and Deshmukh, Girish and Sahasrabuddhe, Vivek and Meriaudeau, Fabrice},
    title = {Indian Diabetic Retinopathy Image Dataset (IDRiD)},
    year = {2018},
    publisher = {IEEE DataPort},
    doi = {10.21227/H25W98},
    url = {https://ieee-dataport.org/open-access/indian-diabetic-retinopathy-image-dataset-idrid}
}

@article{porwal2020idrid,
    title = {Idrid: Diabetic retinopathy--segmentation and grading challenge},
    author = {Porwal, Prasanna and Pachade, Samiksha and Kokare, Manesh and Deshmukh, Girish and Son, Jaemin and Bae, Woong and Liu, Lihong and Wang, Jianzong and Liu, Xinhui and Gao, Liangxin and others},
    journal = {Medical image analysis},
    volume = {59},
    pages = {101561},
    year = {2020},
    publisher = {Elsevier},
    doi = {10.1016/j.media.2019.101561}
}
```

---

### 🦠 Paratuberculosis Histopathology Images Dataset

**Study**: Hananeh, W., & Fraiwan, M. (2025). A dataset of histopathology images of paratuberculosis disease. Mendeley
Data, V3.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                                       |
|-------------------------|-----------------------------------------------------------------------------------------------|
| **📛 Title**            | Paratuberculosis Histopathology Images Dataset                                                |
| **🔗 Source**           | https://data.mendeley.com/datasets/zjhymwjtxv/3                                               |
| **🐄 Target Organ**     | Intestinal Tissue (Veterinary Pathology)                                                      |
| **📅 Last Accessed**    | May 24, 2026                                                                                  |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification (Normal vs. Infected)                                               |
| **📐 Image Size**       | Variable (histopathology slides; standardization recommended)                                 |
| **📁 Data Format**      | Image files (format unspecified; typical: JPG/PNG); optional scale-bar variants in `ImagesS/` |
| **👥 Demographics**     | ❌ Not included (veterinary tissue samples; de-identified)                                     |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                                        |

#### 📊 Dataset Composition

| Category                  | Details                                                                     |
|---------------------------|-----------------------------------------------------------------------------|
| **🖼️ Total Images**      | 366 histopathology images of intestinal tissue                              |
| **🔬 Imaging Modality**   | Brightfield histopathology (H&E-stained tissue sections)                    |
| **🎨 Color Format**       | RGB (typical for histopathology)                                            |
| **📦 Total Size**         | ~28.6 MB (compressed)                                                       |
| **🏫 Source Institution** | Jordan University of Science and Technology, Faculty of Veterinary Medicine |
| **👨‍⚕️ Annotation**      | Expert veterinary pathologist-labeled binary classes                        |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification of paratuberculosis infection status in intestinal tissue
- **Number of Classes**: 2️⃣

| Class Label | Description                                                          | Image Count | Clinical Interpretation                    |
|-------------|----------------------------------------------------------------------|-------------|--------------------------------------------|
| ✅ Negative  | Normal intestinal tissue                                             | 157         | No evidence of paratuberculosis            |
| ⚠️ Positive | Tissue infected with *Mycobacterium avium* subsp. *paratuberculosis* | 209         | Histopathological signs of Johne's disease |

**📊 Dataset Distribution**:

| Class     | Image Count | Percentage |
|-----------|-------------|------------|
| Negative  | 157         | ~42.9%     |
| Positive  | 209         | ~57.1%     |
| **Total** | **366**     | **100%**   |

**🔬 Additional Resource: Scale-Bar Variants**

- The `ImagesS/` subdirectory contains identical images with an overlaid scale bar to clarify magnification level
- Useful for research requiring explicit spatial calibration or multi-scale analysis

#### 💡 Usage Notes

- ✅ First publicly available histopathology dataset dedicated to paratuberculosis (Johne's disease) detection
- ✅ Binary classification task suitable for benchmarking veterinary diagnostic AI models
- ✅ Near-balanced class distribution (~43/57) supports stable training without aggressive resampling
- ✅ Scale-bar variant images enable research on resolution-aware feature extraction
- ✅ Small dataset size (~366 images) ideal for few-shot learning, transfer learning, or data augmentation studies
- 📚 Required to cite the original Mendeley Data repository (DOI: 10.17632/zjhymwjtxv.3) in publications
- 🔐 Verify licensing terms on Mendeley Data; attribution typically required under CC BY 4.0

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                  |
|----------------------------|-------------------------------------------------------------------------------------------------|
| **🔍 Limited Sample Size** | Small dataset (n=366); employ strong regularization, augmentation, or transfer learning         |
| **🧪 Class Balance**       | Mild imbalance (~57% positive); consider stratified sampling or class-weighted loss             |
| **📐 Resolution Variance** | Images may vary in magnification; standardize input dimensions prior to training                |
| **🔐 Ethical Compliance**  | Veterinary tissue samples; adhere to institutional animal research guidelines                   |
| **🧭 Domain Specificity**  | Focused on paratuberculosis in ruminants; generalizability to other species requires validation |
| **🎨 Stain Variability**   | Apply stain normalization (e.g., Macenko method) if integrating external cohorts                |

#### 💡 Suggested Preprocessing Pipeline

1. **Download and extract**: Obtain dataset from Mendeley Data; choose between standard images or `ImagesS/` scale-bar
   variants based on research needs.
2. **Organize directory structure**: Arrange images into class-labeled subfolders (e.g., `Negative/`, `Positive/`) for
   framework-native data loading.
3. **Standardize geometry**: Resize images to uniform dimensions (e.g., 224×224 or 512×512) while preserving aspect
   ratio.
4. **Color normalization**: Apply stain normalization to mitigate inter-slide H&E staining variability.
5. **Augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering; preserve
   histological feature integrity.
6. **Stratified splitting**: Partition data with stratification to maintain class balance across train/validation/test
   sets.
7. **Evaluation metrics**: Report sensitivity, specificity, AUC-ROC, and F1-score; include confusion matrices to assess
   diagnostic performance.

#### 🔗 Associated Resources

- **Mendeley Data Repository**: https://data.mendeley.com/datasets/zjhymwjtxv/3
- **Institutional Affiliation**: Jordan University of Science and Technology, Faculty of Veterinary Medicine
- **Related Publications**:
    - Hananeh, W., & Fraiwan, M. (2025). "A dataset of histopathology images of paratuberculosis disease." *Mendeley
      Data*, V3.
    - Relevant veterinary pathology literature on Johne's disease diagnosis and histopathological features.
- **Related Datasets**:
    - [Dartmouth Kidney Cancer Histology Dataset](#-dartmouth-kidney-cancer-histology-dataset) (human histopathology
      classification)
    - [CRC-HGD-v1](#-crc-hgd-v1-colorectal-cancer-histopathological-grading-dataset) (colorectal grading)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{hananeh2025paratuberculosis,
    author = {Hananeh, Wael and Fraiwan, Mohammad},
    title = {A dataset of histopathology images of paratuberculosis disease},
    year = {2025},
    publisher = {Mendeley Data},
    version = {3},
    doi = {10.17632/zjhymwjtxv.3},
    url = {https://data.mendeley.com/datasets/zjhymwjtxv/3}
}
```

---

### 🫁 COVIDx CT: A Large-Scale Chest CT Dataset for COVID-19 Detection

**Study**: Gunraj, H., Wang, L., & Wong, A. (2020). COVIDNet-CT: A Tailored Deep Convolutional Neural Network Design for
Detection of COVID-19 Cases From Chest CT Images. *Frontiers in Medicine*, 7, 1025. & Gunraj, H., Sabri, A., Koff, D., &
Wong, A. (2022). COVID-Net CT-2: Enhanced Deep Neural Networks for Detection of COVID-19 From Chest CT Images Through
Bigger, More Diverse Learning. *Frontiers in Medicine*, 8, 729287.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                  |
|-------------------------|----------------------------------------------------------|
| **📛 Title**            | COVIDx CT (COVIDx CT-3A / CT-3B)                         |
| **🔗 Source**           | https://www.kaggle.com/datasets/hgunraj/covidxct         |
| **🫁 Target Organ**     | Lungs / Chest                                            |
| **📅 Last Accessed**    | June 20, 2026                                            |
| **🎯 Supported Tasks**  | 🏷️ Classification, 📍 Localization                      |
| **📐 Image Size**       | Variable (CT slices)                                     |
| **📁 Data Format**      | Images (PNG/JPG) and TXT label files with bounding boxes |
| **👥 Demographics**     | ❌ Not included (de-identified)                           |
| **🔄 Train/Test Split** | ✅ Yes (Train/Val/Test)                                   |

#### 📊 Dataset Composition

| Category                   | Details                                                                            |
|----------------------------|------------------------------------------------------------------------------------|
| **🖼️ Total Images**       | 425,024 CT slices (CT-3A) / 431,205 CT slices (CT-3B) from 5,312 / 6,068 patients  |
| **🔬 Imaging Modality**    | Computed Tomography (CT)                                                           |
| **🎨 Color Format**        | Grayscale                                                                          |
| **📦 Variants**            | "A" (confirmed diagnoses) and "B" (includes weakly verified cases, train set only) |
| **🏥 Source Institutions** | Multi-source (CNCB, TCIA, LIDC-IDRI, Radiopaedia, MosMedData, STOIC, etc.)         |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification
- **Number of Classes**: 3️⃣
- ✅ Normal
- 🫁 Pneumonia
- 🦠 COVID-19

#### 📍 Localization Task Details

- **Task Type**: Bounding box localization for the body region
- **Annotation Format**: `filename class xmin ymin xmax ymax` in TXT files (classes are zero-indexed: Normal=0,
  Pneumonia=1, COVID-19=2)

**📊 Dataset Distribution (CT-3A Image Count)**:
| Split | Normal | Pneumonia | COVID-19 | Total |
|-------|--------|-----------|----------|---------|
| Train | 35,996 | 26,970 | 294,552 | 357,518 |
| Val | 17,570 | 8,008 | 8,147 | 33,725 |
| Test | 17,922 | 7,965 | 7,894 | 33,781 |

> **ℹ️ Note**: The "B" variant adds weakly verified cases exclusively to the training set (300,733 COVID-19 images).
> Validation and testing sets remain identical to the "A" variant.

#### 💡 Usage Notes

- ✅ Suitable for benchmarking deep learning models for COVID-19 detection and localization from chest CT
- ✅ Large-scale, multi-source composition supports research on domain generalization across diverse CT protocols
- ✅ Bounding box annotations enable joint classification and localization (object detection) tasks
- ✅ Predefined train/val/test splits enable reproducible benchmarking
- 📚 Required to cite the original *Frontiers in Medicine* publications when using this dataset
- 🔐 Distributed under CC BY-NC-SA 4.0; verify constituent dataset licenses for commercial use

#### ⚠️ Usage Considerations

| Aspect                        | Recommendation                                                                                                       |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------|
| **🔍 Severe Class Imbalance** | COVID-19 class heavily dominates the training set; apply class-weighted loss, focal loss, or undersampling           |
| **📦 Variant Selection**      | Use "A" variant for strictly confirmed diagnoses; use "B" variant to maximize training data diversity                |
| **🎨 Source Heterogeneity**   | Images originate from multiple global institutions; consider domain adaptation or stain/intensity normalization      |
| **📐 Resolution Variance**    | CT slices vary in dimensions and slice thickness; standardize input dimensions (e.g., 224x224 or 512x512)            |
| **🔐 Licensing Compliance**   | Aggregated from multiple sources (e.g., MosMedData is CC BY-NC-ND 3.0); ensure downstream use respects all licenses  |
| **🧭 Clinical Translation**   | Model performance on this curated dataset may not directly translate to real-world screening; validate prospectively |

#### 💡 Suggested Preprocessing Pipeline

1. **Parse metadata**: Read `{train,val,test}_COVIDx_CT-3A.txt` to map image filenames to classes and bounding box
   coordinates.
2. **Standardize geometry**: Resize CT slices to uniform dimensions while preserving aspect ratio; consider windowing (
   e.g., Hounsfield units) if raw DICOM/HU data is reconstructed.
3. **Handle bounding boxes**: Scale bounding box coordinates proportionally to match the resized image dimensions.
4. **Intensity normalization**: Apply standard CT windowing (e.g., lung window or mediastinal window) and scale pixel
   values to [0, 1] or [-1, 1].
5. **Class-aware augmentation **(training only): Incorporate rotation, flipping, and elastic deformations; apply
   stronger augmentation to minority classes (Normal, Pneumonia).
6. **Stratified evaluation**: Report per-class precision, recall, F1-score, and mAP (mean Average Precision) for
   bounding box localization.

#### 🔗 Associated Resources

- **Kaggle Repository**: https://www.kaggle.com/datasets/haydengunraj/covidx-ct
- **GitHub Repository**: https://github.com/haydengunraj/COVIDNet-CT (for dataset generation scripts and models)
- **Related Datasets**:
    - [COVID-19 Lung CT Scans](https://www.kaggle.com/datasets/luisblanche/covid19-lung-ct-scans)
    - [MosMedData](https://www.kaggle.com/datasets/mikhailma/covid19-ct-scans)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{gunraj2020covidnet,
    title = {Covidnet-ct: A tailored deep convolutional neural network design for detection of covid-19 cases from chest ct images},
    author = {Gunraj, Hayden and Wang, Linda and Wong, Alexander},
    journal = {Frontiers in medicine},
    volume = {7},
    pages = {608525},
    year = {2020},
    publisher = {Frontiers}
}

@article{gunraj2022covid,
    title = {Covid-net ct-2: Enhanced deep neural networks for detection of covid-19 from chest ct images through bigger, more diverse learning},
    author = {Gunraj, Hayden and Sabri, Ali and Koff, David and Wong, Alexander},
    journal = {Frontiers in Medicine},
    volume = {8},
    pages = {729287},
    year = {2022},
    publisher = {Frontiers Media SA}
}
```

---

### 🧠 Brain Tumor Dataset (Jun Cheng)

**Study**: Cheng, J. (2024). brain tumor dataset. Figshare.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                       |
|-------------------------|---------------------------------------------------------------|
| **📛 Title**            | Brain Tumor Dataset                                           |
| **🔗 Source**           | https://doi.org/10.6084/m9.figshare.1512427                   |
| **🧠 Target Organ**     | Brain                                                         |
| **📅 Last Accessed**    | June 20, 2026                                                 |
| **🎯 Supported Tasks**  | 🏷️ Classification                                            |
| **📐 Image Size**       | Variable (original .mat files; standardization recommended)   |
| **📁 Data Format**      | .mat files (MATLAB), convertible to JPG/PNG via provided code |
| **👥 Demographics**     | ❌ Not included (de-identified)                                |
| **🔄 Train/Test Split** | ✅ Yes (Cross-validation indices provided in `cvind.mat`)      |

#### 📊 Dataset Composition

| Category                | Details                                                        |
|-------------------------|----------------------------------------------------------------|
| **🖼️ Total Images**    | 3,064 T1-weighted contrast-enhanced MRI scans                  |
| **🏥 Imaging Modality** | T1-weighted contrast-enhanced Magnetic Resonance Imaging (MRI) |
| **🎨 Color Format**     | Grayscale                                                      |
| **📦 Total Size**       | ~838.77 MB (compressed across 4 ZIP archives)                  |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification
- **Number of Classes**: 3️⃣
- 🧠 Meningioma
- 🧠 Glioma
- 🧠 Pituitary tumor

#### 💡 Usage Notes

- ✅ Suitable for benchmarking convolutional neural networks (CNNs) and transfer learning architectures
- ✅ Cross-validation indices (`cvind.mat`) enable reproducible k-fold cross-validation
- ✅ Images are stored in .mat format; requires MATLAB or Python (e.g., `scipy.io.loadmat`) to load
- ✅ Provided MATLAB code can convert .mat files to standard image formats (e.g., JPG)
- 📚 Required to cite the original Figshare repository when using this dataset in publications
- 🔐 Distributed under CC BY 4.0; attribution required for redistribution or adaptation

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                      |
|----------------------------|-------------------------------------------------------------------------------------|
| **📦 Data Format**         | Images are stored as .mat files; ensure appropriate libraries are installed to load |
| **🔍 Class Distribution**  | Verify class balance across the 3 tumor types; consider class-weighted loss         |
| **📐 Resolution Variance** | Original scans may vary in dimensions; apply uniform resizing prior to training     |
| **🧪 Validation Strategy** | Utilize the provided `cvind.mat` for standardized cross-validation benchmarking     |

#### 💡 Suggested Preprocessing Pipeline

1. **Load .mat files**: Use `scipy.io.loadmat` in Python or native MATLAB functions to extract image data.
2. **Convert formats **(optional): Use the provided MATLAB script or a Python equivalent to save images as JPG/PNG.
3. **Standardize input format**: Convert all images to a consistent color space (single-channel grayscale) and fixed
   resolution (e.g., 224x224 or 256x256).
4. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
5. **Cross-validation splitting**: Load `cvind.mat` to assign images to specific folds for training and validation.
6. **Augmentation **(training only): Incorporate rotation, flipping, and intensity jittering to improve model
   generalization.
7. **Stratified evaluation**: Report per-class metrics (precision, recall, F1-score) to assess performance across tumor
   subtypes.

#### 🔗 Associated Resources

- **Figshare Repository**: https://doi.org/10.6084/m9.figshare.1512427
- **Related Datasets**:
    - [Brain Tumor MRI Dataset (Glioma, Meningioma, Pituitary, No Tumor)](#-brain-tumor-mri-dataset-glioma-meningioma-pituitary-no-tumor)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{cheng2024braintumor,
    author = {Cheng, Jun},
    title = {brain tumor dataset},
    year = {2024},
    publisher = {Figshare},
    doi = {10.6084/m9.figshare.1512427},
    url = {https://doi.org/10.6084/m9.figshare.1512427}
}
```

---

### 🫁 Sakha-TB

**Study**: Pchelintsev, Ya, Khvostikov, A, Buchatskaia, O, Nikiforova, N, Shepeleva, L, Prokopev, E, Parolina, L, &
Krylov, A. (2022). Robustness Analysis of Chest X-Ray Computer Tuberculosis Diagnosis. *Computational Mathematics and
Modeling*, 33(4), 472-486.
[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                   |
|-------------------------|---------------------------------------------------------------------------|
| **📛 Title**            | Sakha-TB                                                                  |
| **🔗 Source**           | https://imaging.cs.msu.ru/en/research/TB/Sakha-TB                         |
| **🫁 Target Organ**     | Lungs / Chest                                                             |
| **📅 Last Accessed**    | June 24, 2026                                                             |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification                                                 |
| **📐 Image Size**       | Variable (16-bit and 8-bit PNG)                                           |
| **📁 Data Format**      | PNG (Full: DICOM converted; Compressed: cropped, downsampled, normalized) |
| **👥 Demographics**     | ✅ Balanced by age and gender (to some extent)                             |
| **🔄 Train/Test Split** | ❌ Not provided (400 Normal, 400 TB)                                       |

#### 📊 Dataset Composition

| Category                | Details                                                                                                                                              |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| **🖼️ Total Images**    | 800 frontal chest X-rays                                                                                                                             |
| **🏥 Imaging Modality** | Radiographic X-ray (Frontal)                                                                                                                         |
| **🎨 Color Format**     | Grayscale (16-bit and 8-bit)                                                                                                                         |
| **📦 Variants**         | • Full version (8.73 GB): DICOM converted to PNG with bit depth preserved<br>• Compressed version (0.27 GB): Cropped, downsampled, normalized, 8-bit |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification (Tuberculosis vs. Normal)
- **Number of Classes**: 2️⃣
- 🫁 Tuberculosis
- ✅ Normal

**📊 Dataset Distribution**:
| Class | Image Count |
|---|---|
| ✅ Normal | 400 |
| 🫁 Tuberculosis | 400 |
| **Total** | **800** |

#### 💡 Usage Notes

- ✅ Suitable for benchmarking deep learning models for TB screening from chest X-rays
- ✅ Includes both full-resolution (16-bit) and compressed (8-bit) variants for different computational constraints
- ✅ Balanced class distribution supports stable training without aggressive resampling
- 📚 Required to cite the original *Computational Mathematics and Modeling* publication when using this dataset
- 🔐 Distributed under Creative Commons Attribution 4.0 International license

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                            |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| **📦 Data Format**         | Full version requires handling 16-bit PNGs; ensure libraries support high bit-depth                       |
| **🔍 Class Balance**       | Perfectly balanced (1:1 ratio); standard cross-entropy is sufficient                                      |
| **📐 Resolution Variance** | Compressed version is downsampled; verify if resolution is sufficient for fine-grained feature extraction |
| **🔐 Licensing**           | CC BY 4.0; attribution required for redistribution or adaptation                                          |

#### 💡 Suggested Preprocessing Pipeline

1. **Select variant**: Choose the full version (16-bit) for maximum detail or the compressed version (8-bit) for faster
   iteration.
2. **Standardize input format**: Convert all images to a consistent color space (single-channel grayscale) and fixed
   resolution (e.g., 224x224 or 512x512).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
4. **Augmentation **(training only): Incorporate rotation, flipping, and intensity jittering to improve model
   generalization.
5. **Stratified evaluation**: Report per-class metrics (precision, recall, F1-score, AUC-ROC) to assess diagnostic
   performance.

#### 🔗 Associated Resources

- **Full Version Download**: OneDrive | Yandex Disk (8.73 GB)
- **Compressed Version Download**: OneDrive | Yandex Disk (0.27 GB)
- **Institutional Affiliation**: Laboratory of Mathematical Methods of Image Processing, Lomonosov Moscow State
  University

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{pchelintsev2022robustness,
  title={Robustness Analysis of Chest X-Ray Computer Tuberculosis Diagnosis},
  author={Pchelintsev, Ya and Khvostikov, A and Buchatskaia, O and Nikiforova, N and Shepeleva, L and Prokopev, E and Parolina, L and Krylov, A},
  journal={Computational Mathematics and Modeling},
  volume={33},
  number={4},
  pages={472--486},
  year={2022},
  publisher={Springer}
}
```

---

### 🫁 Tuberculosis (TB) Chest X-ray Database

**Study**: Rahman, T., Khandakar, A., Kadir, M. A., Islam, K. R., Islam, K. F., Mahbub, Z. B., Ayari, M. A., &
Chowdhury, M. E. H. (2020). Reliable Tuberculosis Detection using Chest X-ray with Deep Learning, Segmentation and
Visualization. *IEEE Access*, 8, 191586-191601.
[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                           |
|-------------------------|-----------------------------------------------------------------------------------|
| **📛 Title**            | Tuberculosis (TB) Chest X-ray Database                                            |
| **🔗 Source**           | https://www.kaggle.com/datasets/tawsifurrahman/tuberculosis-tb-chest-xray-dataset |
| **🫁 Target Organ**     | Lungs / Chest                                                                     |
| **📅 Last Accessed**    | June 24, 2026                                                                     |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification                                                         |
| **📐 Image Size**       | Variable (Chest X-rays)                                                           |
| **📁 Data Format**      | Images (folders), metadata.xlsx                                                   |
| **👥 Demographics**     | ❌ Not included                                                                    |
| **🔄 Train/Test Split** | ❌ Not provided (700 public TB, 2800 NIAID TB, 3500 Normal)                        |

#### 📊 Dataset Composition

| Category                | Details                                                                            |
|-------------------------|------------------------------------------------------------------------------------|
| **🖼️ Total Images**    | 4,200 publicly accessible chest X-rays                                             |
| **🏥 Imaging Modality** | Radiographic X-ray (Frontal)                                                       |
| **🎨 Color Format**     | Grayscale / RGB (scan-dependent)                                                   |
| **📦 Sources**          | NLM (Montgomery, Shenzhen), Belarus Set, NIAID TB Portal, RSNA Pneumonia Challenge |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification (Tuberculosis vs. Normal)
- **Number of Classes**: 2️⃣
- 🫁 Tuberculosis
- ✅ Normal

**📊 Dataset Distribution**:

| Class           | Image Count | Notes                                                         |
|-----------------|-------------|---------------------------------------------------------------|
| ✅ Normal        | 3,500       | Aggregated from multiple sources                              |
| 🫁 Tuberculosis | 700         | Publicly accessible; 2,800 more available via NIAID agreement |
| **Total**       | **4,200**   | —                                                             |

#### 💡 Usage Notes

- ✅ Largest publicly available TB Chest X-ray database for benchmarking deep learning models
- ✅ Aggregated from multiple global institutions (NLM, Belarus, NIAID, RSNA) supports domain generalization studies
- ✅ Includes metadata files for image references and provenance tracking
- 📚 Required to cite the original *IEEE Access* publication when using this dataset
- 🔐 Data files © Original Authors; verify specific terms for each constituent source

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**     | Severe imbalance (3500 Normal vs. 700 TB); apply class-weighted loss or oversampling                       |
| **📦 Data Heterogeneity**  | Sourced from multiple databases with varying resolutions and protocols; consider domain adaptation         |
| **🔐 Licensing**           | Aggregated dataset; ensure compliance with individual source licenses (e.g., NIAID data-sharing agreement) |
| **🧪 Validation Strategy** | No predefined split; implement patient-aware or source-aware partitioning to prevent data leakage          |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Utilize framework-native utilities to ingest the `Normal` and `Tuberculosis`
   subfolders.
2. **Standardize input format**: Convert all images to a consistent color space (single-channel grayscale) and fixed
   resolution (e.g., 224x224 or 256x256).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
4. **Augmentation **(training only): Incorporate rotation, flipping, and intensity jittering to improve model
   generalization.
5. **Stratified evaluation**: Report per-class metrics (precision, recall, F1-score, AUC-ROC) to assess performance
   given the class imbalance.

#### 🔗 Associated Resources

- **Kaggle Repository**: https://www.kaggle.com/datasets/tawsifurrahman/tuberculosis-tb-chest-xray-dataset
- **NIAID TB Portal**: https://tbportals.niaid.nih.gov/download-data (for additional 2,800 TB images)
- **Related Publications**: Rahman et al., "Reliable Tuberculosis Detection using Chest X-ray with Deep Learning,
  Segmentation and Visualization," *IEEE Access*, 2020.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{rahman2020reliable,
  title={Reliable tuberculosis detection using chest X-ray with deep learning, segmentation and visualization},
  author={Rahman, Tawsifur and Khandakar, Amith and Kadir, Muhammad Abdul and Islam, Khandaker Rejaul and Islam, Khandakar F and Mazhar, Rashid and Hamid, Tahir and Islam, Mohammad Tariqul and Kashem, Saad and Mahbub, Zaid Bin and others},
  journal={Ieee Access},
  volume={8},
  pages={191586--191601},
  year={2020},
  publisher={IEEE}
}
```

---

### 👁️🫁 Labeled Optical Coherence Tomography (OCT) and Chest X-Ray Images for Classification

**Study**: Kermany, D. S., Goldbaum, M., Cai, W., Cordeiro, N. M., Baxter, J. S., et al. (2018). Identifying Medical
Diagnoses and Treatable Diseases by Image-Based Deep Learning. *Cell*, 172(5), 1122-1131.e9.
[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                              |
|-------------------------|--------------------------------------------------------------------------------------|
| **📛 Title**            | Labeled Optical Coherence Tomography (OCT) and Chest X-Ray Images for Classification |
| **🔗 Source**           | https://data.mendeley.com/datasets/rscbjbr9sj/2                                      |
| **👁️🫁 Target Organ**  | Eye (Retina) / Lungs (Chest)                                                         |
| **📅 Last Accessed**    | June 24, 2026                                                                        |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                                                        |
| **📐 Image Size**       | Variable (OCT and Chest X-rays)                                                      |
| **📁 Data Format**      | Images in directories                                                                |
| **👥 Demographics**     | ❌ Not included (independent patients)                                                |
| **🔄 Train/Test Split** | ✅ Yes (Training and testing sets of independent patients)                            |

#### 📊 Dataset Composition

| Category                  | Details                                                                  |
|---------------------------|--------------------------------------------------------------------------|
| **🖼️ Total Images**      | ~108,000 OCT images + Chest X-rays (exact X-ray count varies by version) |
| **🏥 Imaging Modality**   | Optical Coherence Tomography (OCT) / Radiographic X-ray                  |
| **🎨 Color Format**       | Grayscale / RGB (scan-dependent)                                         |
| **🏥 Source Institution** | University of California San Diego                                       |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of retinal diseases (OCT) and chest conditions (X-ray)
- **Number of Classes **(OCT): 4️⃣
- 🩸 CNV (Choroidal Neovascularization)
- 💧 DME (Diabetic Macular Edema)
- 🟡 DRUSEN
- ✅ NORMAL
- **Number of Classes **(X-Ray): 2️⃣ (Normal vs. Pneumonia)

**📊 Dataset Distribution **(OCT)

| Split       | Image Count  | Purpose                                             |
|-------------|--------------|-----------------------------------------------------|
| 🟢 Training | ~100,000     | Model training and development                      |
| 🔴 Testing  | ~8,000       | Final performance evaluation (independent patients) |
| **Total**   | **~108,000** | —                                                   |

#### 💡 Usage Notes

- ✅ Benchmark dataset for multi-disease image-based deep learning classification
- ✅ Patient-independent train/test splits ensure rigorous evaluation without data leakage
- ✅ Supports research on multi-modal or multi-organ diagnostic AI systems
- 📚 Required to cite the original *Cell* publication and Mendeley Data repository when using this dataset
- 🔐 Distributed via Mendeley Data; verify usage terms for clinical deployment

#### ⚠️ Usage Considerations

| Aspect                    | Recommendation                                                                                                    |
|---------------------------|-------------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**    | Verify per-class distribution; apply class-weighted loss or stratified sampling if needed                         |
| **📦 Data Organization**  | Images are organized by disease label; ensure proper directory parsing for framework-native loaders               |
| **🧪 Multi-Organ Focus**  | Dataset contains both OCT and X-ray images; separate preprocessing pipelines may be required for each modality    |
| **🔐 Ethical Compliance** | Dataset contains de-identified clinical imagery; adhere to institutional review requirements for derivative works |

#### 💡 Suggested Preprocessing Pipeline

1. **Separate modalities**: Isolate OCT and Chest X-ray directories to apply modality-specific preprocessing.
2. **Standardize input format**: Convert all images to a consistent color space and fixed resolution (e.g., 224x224 or
   256x256).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
4. **Augmentation **(training only): Incorporate rotation, flipping, and intensity jittering to improve model
   generalization.
5. **Stratified evaluation**: Report per-class metrics (precision, recall, F1-score) to assess performance across
   different disease categories.

#### 🔗 Associated Resources

- **Mendeley Data Repository**: https://data.mendeley.com/datasets/rscbjbr9sj/2
- **Related Publications**: Kermany et al., "Identifying Medical Diagnoses and Treatable Diseases by Image-Based Deep
  Learning," *Cell*, 2018.
- **Institutional Affiliation**: University of California San Diego

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{kermany2018labeled,
  author={Kermany, Daniel and Zhang, Kang and Goldbaum, Michael},
  title={Labeled Optical Coherence Tomography {(OCT)} and Chest {X-Ray} Images for Classification},
  year={2018},
  publisher={Mendeley Data},
  version={2},
  doi={10.17632/rscbjbr9sj.2}
}
```

---

### 🫁 CheXpert: A Large Chest Radiograph Dataset with Uncertainty Labels and Expert Comparison

**Study**: Irvin, J., Rajpurkar, P., Ko, M., Yu, S. C., Ciurea-Ilcus, S., Chute, C., ... & Ng, A. Y. (2019). CheXpert: A
Large Chest Radiograph Dataset with Uncertainty Labels and Expert Comparison. *Proceedings of the AAAI Conference on
Artificial Intelligence*, 33(01), 590-597.
[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                                  |
|-------------------------|------------------------------------------------------------------------------------------|
| **📛 Title**            | CheXpert: A Large Chest Radiograph Dataset with Uncertainty Labels and Expert Comparison |
| **🔗 Source**           | https://stanfordmlgroup.github.io/competitions/chexpert/                                 |
| **🫁 Target Organ**     | Lungs / Chest                                                                            |
| **📅 Last Accessed**    | June 26, 2026                                                                            |
| **🎯 Supported Tasks**  | 🏷️ Multiclass / Multi-label Classification                                              |
| **📐 Image Size**       | Variable (Chest X-rays)                                                                  |
| **📁 Data Format**      | JPEG (.jpg) / DICOM                                                                      |
| **👥 Demographics**     | ❌ Not included (de-identified)                                                           |
| **🔄 Train/Test Split** | ✅ Yes (Train / Validation / Test)                                                        |

#### 📊 Dataset Composition

| Category                  | Details                                        |
|---------------------------|------------------------------------------------|
| **🖼️ Total Images**      | 224,316 chest radiographs from 65,240 patients |
| **🏥 Imaging Modality**   | Radiographic X-ray (Frontal and Lateral views) |
| **🎨 Color Format**       | Grayscale                                      |
| **🏥 Source Institution** | Stanford Hospital                              |
| **📅 Collection Period**  | October 2002 – July 2017                       |

#### 🏷️ Classification Task Details

- **Task Type**: Multi-label classification of 14 radiological observations
- **Number of Classes**: 14️⃣ (No Finding, Enlarged Cardiomediastinum, Cardiomegaly, Lung Opacity, Lung Lesion, Edema,
  Consolidation, Pneumonia, Atelectasis, Pneumothorax, Pleural Effusion, Pleural Other, Fracture, Support Devices)
- **Label Types**: Positive (1), Negative (0), Uncertain (-1), or Blank (unmentioned)
- **Competition Tasks**: 5️⃣ (Atelectasis, Cardiomegaly, Consolidation, Edema, Pleural Effusion)

**📊 Dataset Distribution**:

| Split     | Image Count | Purpose                               |
|-----------|-------------|---------------------------------------|
| 🟢 Train  | 223,816     | Model training and development        |
| 🟡 Valid  | 200         | Hyperparameter tuning                 |
| 🔴 Test   | 500         | Final performance evaluation (Expert) |
| **Total** | **224,316** | —                                     |

> **ℹ️ Note**: The training set features uncertainty labels extracted via an automated rule-based labeler from free-text
> radiology reports. The test set contains strong ground truth from a majority vote of 8 board-certified radiologists.

#### 💡 Usage Notes

- ✅ Suitable for benchmarking deep learning models for automated chest X-ray interpretation
- ✅ Features uncertainty labels to handle ambiguous radiology report statements
- ✅ Includes a radiologist-labeled reference standard evaluation set for rigorous benchmarking
- ✅ Supports research on multi-label classification and uncertainty modeling in medical imaging
- 📚 Required to cite the original AAAI publication and Stanford ML Group when using this dataset

#### ⚠️ Usage Considerations

| Aspect                       | Recommendation                                                                                              |
|------------------------------|-------------------------------------------------------------------------------------------------------------|
| **🔍 Label Uncertainty**     | Training labels contain uncertainty; explore approaches like U-Ignore, U-Zeroes, U-Ones, or U-MultiClass    |
| **🧪 Multi-Label Nature**    | Images can have multiple concurrent pathologies; use appropriate loss functions (e.g., BCE with logits)     |
| **📐 View Handling**         | Dataset contains both frontal and lateral views; consider view-agnostic or multi-view architectures         |
| **🔐 Licensing**             | Verify usage terms on the Stanford AIMI website; typically restricted to non-commercial research use        |
| **🧭 Domain Generalization** | Sourced from a single institution (Stanford Hospital); validate on external cohorts for clinical deployment |

#### 💡 Suggested Preprocessing Pipeline

1. **Parse metadata**: Load the provided CSV files to map image paths to the 14 observation labels and uncertainty
   flags.
2. **Standardize input format**: Convert all images to a consistent color space (single-channel grayscale) and fixed
   resolution (e.g., 320x320 or 512x512).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
4. **Handle uncertainty**: Decide on a strategy for uncertain labels (e.g., U-MultiClass treats uncertainty as a
   separate class).
5. **Augmentation **(training only): Incorporate rotation, flipping, and intensity jittering to improve model
   generalization.
6. **Stratified evaluation**: Report per-class AUC-ROC, sensitivity, and specificity, especially for the 5 competition
   tasks.

#### 🔗 Associated Resources

- **Stanford ML Group Competition Page**: https://stanfordmlgroup.github.io/competitions/chexpert/
- **Stanford AIMI Dataset**: https://stanford.redivis.com/datasets/5yyj-1a9f6ap0x
- **Test Set Labels & Links**: https://github.com/rajpurkarlab/cheXpert-test-set-labels
- **CheXpert Labeler**: https://github.com/stanfordmlgroup/chexpert-labeler

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@inproceedings{irvin2019chexpert,
  title={Chexpert: A large chest radiograph dataset with uncertainty labels and expert comparison},
  author={Irvin, Jeremy and Rajpurkar, Pranav and Ko, Michael and Yu, Yifan and Ciurea-Ilcus, Silviana and Chute, Chris and Marklund, Henrik and Haghgoo, Behzad and Ball, Robyn and Shpanskaya, Katie and others},
  booktitle={Proceedings of the AAAI conference on artificial intelligence},
  volume={33},
  number={01},
  pages={590--597},
  year={2019}
}
```

---

### 🫁 COVID-19 Radiography Database

**Study**: Chowdhury, M. E. H., Rahman, T., Khandakar, A., Mazhar, R., Kadir, M. A., Mahbub, Z. B., ... & Islam, M. T. (
2020). Can AI help in screening Viral and COVID-19 pneumonia?. *IEEE Access*, 8, 132665-132676.
[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                     |
|-------------------------|-----------------------------------------------------------------------------|
| **📛 Title**            | COVID-19 Radiography Database                                               |
| **🔗 Source**           | https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database |
| **🫁 Target Organ**     | Lungs / Chest                                                               |
| **📅 Last Accessed**    | June 26, 2026                                                               |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification, 🎭 Segmentation                              |
| **📐 Image Size**       | 299 × 299 pixels (fixed)                                                    |
| **📁 Data Format**      | PNG (.png) for images and masks, XLSX (.xlsx) for metadata                  |
| **👥 Demographics**     | ❌ Not included (de-identified)                                              |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                      |

#### 📊 Dataset Composition

| Category                   | Details                                                  |
|----------------------------|----------------------------------------------------------|
| **🖼️ Total Images**       | 21,165 chest X-ray images                                |
| **🏥 Imaging Modality**    | Radiographic X-ray                                       |
| **🎨 Color Format**        | PNG (Grayscale / RGB)                                    |
| **🏥 Source Institutions** | Qatar University, University of Dhaka, and collaborators |
| **📦 Total Size**          | ~806.84 MB                                               |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of lung conditions
- **Number of Classes**: 4️⃣
- 🦠 COVID-19
- 🫁 Lung Opacity (Non-COVID lung infection)
- ✅ Normal
- 🦠 Viral Pneumonia

**📊 Dataset Distribution**:

| Class              | Image Count | Description                                 |
|--------------------|-------------|---------------------------------------------|
| 🦠 COVID-19        | 3,616       | Positive cases of SARS-CoV-2 infection      |
| ✅ Normal           | 10,192      | Healthy lung scans                          |
| 🫁 Lung Opacity    | 6,012       | Non-COVID lung infections (e.g., bacterial) |
| 🦠 Viral Pneumonia | 1,345       | Viral pneumonia cases                       |
| **Total**          | **21,165**  | —                                           |

#### 🎭 Segmentation Task Details

- **Task Type**: Binary semantic segmentation of lung regions
- **Annotation Targets**: Ground-truth lung segmentation masks for the entire dataset
- **Format**: PNG masks corresponding to the chest X-ray images

#### 💡 Usage Notes

- ✅ Suitable for benchmarking deep learning models for COVID-19 and pneumonia detection
- ✅ Includes ground-truth lung segmentation masks for joint classification and segmentation tasks
- ✅ Winner of the COVID-19 Dataset Award by the Kaggle Community
- ✅ Fixed 299×299 resolution simplifies preprocessing for standard CNN architectures
- 📚 Required to cite the original *IEEE Access* publications when using this dataset

#### ⚠️ Usage Considerations

| Aspect                       | Recommendation                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**       | Normal class heavily dominates; apply class-weighted loss, focal loss, or undersampling                      |
| **🧪 Multi-Class Nature**    | Distinguishing between COVID-19, Viral Pneumonia, and other Lung Opacities requires careful feature learning |
| **📐 Resolution**            | Images are fixed at 299×299; ensure model input layers match or resize accordingly                           |
| **🔐 Licensing**             | Data files © Original Authors; verify specific terms for commercial or clinical deployment                   |
| **🧭 Domain Generalization** | Aggregated from multiple global sources; validate on external cohorts for clinical deployment                |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Utilize framework-native utilities to ingest the `COVID`, `Lung_Opacity`, `Normal`, and
   `Viral Pneumonia` subfolders.
2. **Standardize input format**: Confirm uniform 299×299 dimensions; convert to single-channel grayscale if desired.
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
4. **Load segmentation masks**: Align lung mask PNGs with their corresponding X-ray images for segmentation tasks.
5. **Augmentation **(training only): Incorporate rotation, flipping, and intensity jittering to improve model
   generalization.
6. **Stratified evaluation**: Report per-class precision, recall, F1-score, and AUC-ROC to assess performance given the
   class imbalance.

#### 🔗 Associated Resources

- **Kaggle Repository**: https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database
- **Related Dataset**: COVID-QU-Ex Dataset (33,920 images with lung masks)
- **Related Publications**:
    - Chowdhury, M. E. H., et al. (2020). "Can AI help in screening Viral and COVID-19 pneumonia?" *IEEE Access*.
    - Rahman, T., et al. (2020). "Exploring the Effect of Image Enhancement Techniques on COVID-19 Detection using Chest
      X-ray Images."

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{chowdhury2020can,
  title={Can AI help in screening viral and COVID-19 pneumonia?},
  author={Chowdhury, Muhammad EH and Rahman, Tawsifur and Khandakar, Amith and Mazhar, Rashid and Kadir, Muhammad Abdul and Mahbub, Zaid Bin and Islam, Khandakar Reajul and Khan, Muhammad Salman and Iqbal, Atif and Al Emadi, Nasser and others},
  journal={Ieee Access},
  volume={8},
  pages={132665--132676},
  year={2020},
  publisher={IEEE}
}
@article{rahman2021exploring,
  title={Exploring the effect of image enhancement techniques on COVID-19 detection using chest X-ray images},
  author={Rahman, Tawsifur and Khandakar, Amith and Qiblawey, Yazan and Tahir, Anas and Kiranyaz, Serkan and Kashem, Saad Bin Abul and Islam, Mohammad Tariqul and Al Maadeed, Somaya and Zughaier, Susu M and Khan, Muhammad Salman and others},
  journal={Computers in biology and medicine},
  volume={132},
  pages={104319},
  year={2021},
  publisher={Elsevier}
}
```

--- 

### 👁️ Ocular Disease Recognition (ODIR-5K)

**Study**: Larxel. (2020). Ocular Disease Recognition. Kaggle.
[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                     |
|-------------------------|-----------------------------------------------------------------------------|
| **📛 Title**            | Ocular Disease Recognition (ODIR-5K)                                        |
| **🔗 Source**           | https://www.kaggle.com/datasets/andrewmvd/ocular-disease-recognition-odir5k |
| **👁️ Target Organ**    | Eye (Retina / Fundus)                                                       |
| **📅 Last Accessed**    | June 30, 2026                                                               |
| **🎯 Supported Tasks**  | 🏷️ Multiclass / Multi-label Classification                                 |
| **📐 Image Size**       | Variable (varied camera resolutions)                                        |
| **📁 Data Format**      | JPEG/PNG (images), CSV (metadata/labels)                                    |
| **👥 Demographics**     | ✅ Age, Sex (Male 54%, Female 46%)                                           |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                      |

#### 📊 Dataset Composition

| Category                  | Details                                                             |
|---------------------------|---------------------------------------------------------------------|
| **🖼️ Total Images**      | 10,000 color fundus photographs (5,000 patients, left & right eyes) |
| **🏥 Imaging Modality**   | Color fundus photography                                            |
| **🎨 Color Format**       | RGB                                                                 |
| **📦 Total Size**         | ~2.03 GB (compressed)                                               |
| **🏥 Source Institution** | Shanggong Medical Technology Co., Ltd. (various hospitals in China) |

#### 🏷️ Classification Task Details

- **Task Type**: Multi-label classification of ocular diseases
- **Number of Classes**: 8️⃣
- ✅ Normal (N)
- 🍬 Diabetes (D)
- 👁️ Glaucoma (G)
- 🌫️ Cataract (C)
- 🟡 Age related Macular Degeneration (A)
- 🩸 Hypertension (H)
- 🔍 Pathological Myopia (M)
- ⚠️ Other diseases/abnormalities (O)

#### 💡 Usage Notes

- ✅ Suitable for benchmarking multi-label classification models for ocular disease screening
- ✅ Includes both left and right eye images for potential bilateral analysis
- ✅ Contains real-world diagnostic keywords from doctors
- 📚 Required to cite the original Kaggle repository when using this dataset
- 🔐 License was not specified on source; verify terms for commercial use

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                    |
|----------------------------|-----------------------------------------------------------------------------------|
| **🔍 Multi-label Nature**  | Patients can have multiple conditions; use appropriate loss functions (e.g., BCE) |
| **📐 Resolution Variance** | Images captured by various cameras (Canon, Zeiss, Kowa); standardize dimensions   |
| **🧪 Data Leakage**        | Split by patient ID, not by image, to prevent leakage between train/test sets     |
| **🔐 Licensing**           | License not explicitly specified; contact authors or assume non-commercial use    |

#### 💡 Suggested Preprocessing Pipeline

1. **Load metadata**: Parse `full_df.csv` to map image paths to the 8 diagnostic labels.
2. **Standardize input format**: Convert all images to a consistent color space and fixed resolution (e.g., 224x224).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide statistics.
4. **Augmentation **(training only): Incorporate rotation, flipping, and color jittering to improve generalization.
5. **Stratified evaluation**: Report per-class AUC-ROC, sensitivity, and specificity to assess multi-label performance.

#### 🔗 Associated Resources

- **Kaggle Repository**: https://www.kaggle.com/datasets/andrewmvd/ocular-disease-recognition-odir5k
- **Related Datasets
  **: [IDRiD](#-idrid-diabetic-retinopathy-grading-indian-dataset), [EyePACS](#-eyepacs-aptos-messidor-diabetic-retinopathy-unified-dataset)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{larxel2020odir,
  title={Ocular Disease Recognition},
  author={Larxel},
  year={2020},
  publisher={Kaggle},
  url={https://www.kaggle.com/datasets/andrewmvd/ocular-disease-recognition-odir5k}
}
```

---

### 🖼️ ISIC 2019: Skin Lesion Analysis Toward Melanoma Detection

**Study**: Tschandl, P., Rosendahl, C., & Kittler, H. (2018). The HAM10000 dataset... / Codella, N., et al. (2017)... /
Hernández-Pérez, C., et al. (2024)...

[🔝 Back to Summary](#-dataset-summary)
| Metadata | Details |
|-------------------------|-------------------------------------------------------------------------|
| **📛 Title**            | ISIC 2019: Skin Lesion Analysis Toward Melanoma Detection |
| **🔗 Source**           | https://challenge.isic-archive.com/data/#2019                           |
| **🖼️ Target Organ**    | Skin |
| **📅 Last Accessed**    | June 30, 2026 |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification |
| **📐 Image Size**       | Variable (dermoscopic and clinical images)                              |
| **📁 Data Format**      | JPEG (images), CSV (metadata/labels)                                    |
| **👥 Demographics**     | ✅ Age, Sex, Anatomical site |
| **🔄 Train/Test Split** | ✅ Yes (25,331 Training / 8,238 Test)                                    |

#### 📊 Dataset Composition

| Category                   | Details                              |
|----------------------------|--------------------------------------|
| **🖼️ Total Images**       | 33,569 skin lesion images            |
| **🏥 Imaging Modality**    | Dermoscopic and clinical photography |
| **🎨 Color Format**        | RGB                                  |
| **📦 Total Size**          | ~12.7 GB (compressed)                |
| **🏥 Source Institutions** | BCN-20000, HAM10000, MSK datasets    |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of skin lesions
- **Number of Classes**: 8️⃣
- ⚫ Melanoma (MEL)
- 🟤 Melanocytic nevus (NV)
- 🟠 Basal cell carcinoma (BCC)
- 🟡 Actinic keratosis (AK)
- 🟢 Benign keratosis (BKL)
- 🔵 Dermatofibroma (DF)
- 🔴 Vascular lesion (VASC)
- ⚪ Squamous cell carcinoma (SCC)

#### 💡 Usage Notes

- ✅ Benchmark dataset for dermoscopic image classification and melanoma detection
- ✅ Includes rich metadata (age, sex, anatomical site) for demographic bias analysis
- ✅ Pre-defined train/test splits enable reproducible benchmarking
- 📚 Required to cite the original ISIC challenge and constituent datasets (HAM10000, BCN-20000, MSK)
- 🔐 Distributed under CC-BY-NC; verify terms for commercial use

#### ⚠️ Usage Considerations

| Aspect                        | Recommendation                                                               |
|-------------------------------|------------------------------------------------------------------------------|
| **🔍 Severe Class Imbalance** | NV and BKL heavily dominate; apply class-weighted loss or focal loss         |
| **📐 Resolution Variance**    | Images vary in dimensions; standardize to fixed dimensions prior to training |
| **🧪 Metadata Integration**   | Leverage age/sex metadata to improve model fairness and generalization       |
| **🔐 Licensing**              | CC-BY-NC-ND; strictly non-commercial use without explicit permission         |

#### 💡 Suggested Preprocessing Pipeline

1. **Load metadata**: Parse CSV files to map image IDs to diagnostic labels and demographic features.
2. **Standardize input format**: Convert all images to a consistent color space and fixed resolution (e.g., 224x224).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using ImageNet statistics.
4. **Augmentation **(training only): Incorporate rotation, flipping, and color jittering; avoid aggressive distortions.
5. **Stratified evaluation**: Report per-class AUC-ROC, sensitivity, and specificity, especially for melanoma.

#### 🔗 Associated Resources

- **ISIC Archive**: https://challenge.isic-archive.com/data/#2019
- **Related Datasets**: [PAD-UFES-20](#-pad-ufes-20-skin-lesion-dataset)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{isic2019skin,
  title={ISIC 2019: Skin Lesion Analysis Toward Melanoma Detection},
  author={Tschandl, P. and Rosendahl, C. and Kittler, H. and Codella, N. and others},
  year={2019},
  publisher={ISIC Archive},
  url={https://challenge.isic-archive.com/data/#2019}
}
```

---

### 🧪 Clinical Urine Microscopy for Urinary Tract Infections

**Study**: Liou, N., De, T., Urbanski, A., Khasriya, R., Yakimovich, A., & Horsley, H. (2023). Clinical urine microscopy
for urinary tract infections. RODARE.

[🔝 Back to Summary](#-dataset-summary)
| Metadata | Details |
|-------------------------|-------------------------------------------------------------------------|
| **📛 Title**            | Clinical Urine Microscopy for Urinary Tract Infections |
| **🔗 Source**           | https://rodare.hzdr.de/record/2473                                      |
| **🧪 Target Organ**    | Urine / Cellular |
| **📅 Last Accessed**    | June 30, 2026 |
| **🎯 Supported Tasks**  | 🎭 Semantic Segmentation (Binary & Multi-class)                         |
| **📐 Image Size**       | 1392 × 1040 pixels (fixed)                                              |
| **📁 Data Format**      | 16-bit TIFF (images and masks)                                          |
| **👥 Demographics**     | ✅ Symptomatic UTI patients |
| **🔄 Train/Test Split** | ❌ Not provided (300 images total)                                       |

#### 📊 Dataset Composition

| Category                  | Details                                   |
|---------------------------|-------------------------------------------|
| **🖼️ Total Images**      | 300 brightfield microscopy images         |
| **🏥 Imaging Modality**   | Brightfield microscopy (x20 objective)    |
| **🎨 Color Format**       | 16-bit RGB                                |
| **📦 Total Size**         | ~2.3 GB (compressed)                      |
| **🏥 Source Institution** | Specialist LUTS outpatient clinic, London |

#### 🎭 Segmentation Task Details

- **Task Type**: Binary and multi-class semantic segmentation of urinary cells
- **Number of Classes**: 7️⃣
- ⚫ Background (0)
- 🦠 Rod (1)
- 🩸 RBC/WBC (2)
- 🍄 Yeast (3)
- 🟤 Miscellaneous (4)
- 🟡 Single EPC (5)
- 🟠 Small EPC sheet (6)
- 🔴 Large EPC sheet (7)

#### 💡 Usage Notes

- ✅ First publicly available dataset for automated UTI diagnosis via urine microscopy
- ✅ Includes both binary (foreground/background) and multi-class segmentation masks
- ✅ High-resolution 16-bit TIFF images preserve fine cellular details
- 📚 Required to cite the original RODARE repository when using this dataset
- 🔐 Distributed under CC BY 4.0; attribution required for redistribution

#### ⚠️ Usage Considerations

| Aspect                        | Recommendation                                                               |
|-------------------------------|------------------------------------------------------------------------------|
| **🔍 Severe Class Imbalance** | Background dominates; EPC sheets are rare; use appropriate loss functions    |
| **📐 High Resolution**        | 1392x1040 images require substantial memory; consider patch-based processing |
| **🎨 16-bit Format**          | Ensure libraries support 16-bit TIFF loading; normalize to 8-bit if needed   |
| **🧪 Clinical Translation**   | Validate on external cohorts before clinical deployment                      |

#### 💡 Suggested Preprocessing Pipeline

1. **Load TIFF files**: Use libraries supporting 16-bit TIFF (e.g., `tifffile`, `Pillow`).
2. **Standardize resolution**: Resize or extract patches to model-compatible dimensions (e.g., 512x512).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide statistics.
4. **Augmentation **(training only): Incorporate rotation, flipping, and elastic deformations; preserve cellular
   integrity.
5. **Stratified evaluation**: Report Dice/IoU for each class, especially for rare classes like EPC sheets.

#### 🔗 Associated Resources

- **RODARE Repository**: https://rodare.hzdr.de/record/2473
- **Related Publications**: Liou, N., et al. (2023). "Clinical urine microscopy for urinary tract infections."

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{liou2023urine,
  title={Clinical urine microscopy for urinary tract infections},
  author={Liou, Natasha and De, Trina and Urbanski, Adrian and Khasriya, Rajvinder and Yakimovich, Artur and Horsley, Harry},
  year={2023},
  publisher={RODARE},
  doi={10.14278/rodare.2473},
  url={https://rodare.hzdr.de/record/2473}
}
```

---

### ❤️ Heart Failure Prediction Dataset

**Study**: fedesoriano. (2021). Heart Failure Prediction Dataset. Kaggle.
[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                              |
|-------------------------|----------------------------------------------------------------------|
| **📛 Title**            | Heart Failure Prediction Dataset                                     |
| **🔗 Source**           | https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction |
| **❤️ Target Organ**     | Heart / Cardiovascular                                               |
| **📅 Last Accessed**    | June 30, 2026                                                        |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification                                            |
| **📐 Image Size**       | N/A (Tabular data)                                                   |
| **📁 Data Format**      | CSV                                                                  |
| **👥 Demographics**     | ✅ Age, Sex                                                           |
| **🔄 Train/Test Split** | ❌ Not provided (918 observations)                                    |

#### 📊 Dataset Composition

| Category                   | Details                                                           |
|----------------------------|-------------------------------------------------------------------|
| **📊 Total Instances**     | 918 observations                                                  |
| **🔢 Features**            | 11 clinical features + 1 target variable                          |
| **📦 Total Size**          | ~35.92 kB                                                         |
| **🏥 Source Institutions** | Cleveland, Hungarian, Switzerland, Long Beach VA, Stalog datasets |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification of heart disease presence
- **Number of Classes**: 2️⃣
- ✅ Normal (0)
- ⚠️ Heart Disease (1)

#### 💡 Usage Notes

- ✅ Largest combined heart disease dataset available for research (5 UCI datasets merged)
- ✅ Includes comprehensive clinical features (ECG, cholesterol, angina, etc.)
- ✅ Suitable for benchmarking tabular machine learning models
- 📚 Required to cite the original Kaggle repository and UCI sources
- 🔐 Database: Open Database, Contents: © Original Authors

#### ⚠️ Usage Considerations

| Aspect                      | Recommendation                                                                  |
|-----------------------------|---------------------------------------------------------------------------------|
| **🔍 Feature Scaling**      | Normalize numerical features (e.g., Age, Cholesterol) for distance-based models |
| **🧪 Categorical Encoding** | One-hot encode categorical variables (e.g., ChestPainType, RestingECG)          |
| **📐 Missing Values**       | Verify handling of missing cholesterol values in original UCI sources           |
| **🔐 Licensing**            | Open Database License; verify terms for commercial use                          |

#### 💡 Suggested Preprocessing Pipeline

1. **Load CSV**: Parse `heart.csv` using pandas or similar libraries.
2. **Handle missing values**: Impute or drop missing cholesterol values if present.
3. **Encode categoricals**: Convert categorical features to numerical representations.
4. **Scale features**: Apply StandardScaler or MinMaxScaler to numerical features.
5. **Stratified splitting**: Implement stratified k-fold cross-validation to maintain class balance.
6. **Evaluation metrics**: Report accuracy, precision, recall, F1-score, and AUC-ROC.

#### 🔗 Associated Resources

- **Kaggle Repository**: https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction
- **UCI Source**: https://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{fedesoriano2021heart,
  title={Heart Failure Prediction Dataset},
  author={fedesoriano},
  year={2021},
  publisher={Kaggle},
  url={https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction}
}
```

---

### ❤️ Heart Attack Analysis & Prediction Dataset

**Study**: Hina Ismail, et al. (2022). Heart Attack Analysis & Prediction Dataset. Kaggle.
[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                                  |
|-------------------------|------------------------------------------------------------------------------------------|
| **📛 Title**            | Heart Attack Analysis & Prediction Dataset                                               |
| **🔗 Source**           | https://www.kaggle.com/datasets/sonialikhan/heart-attack-analysis-and-prediction-dataset |
| **❤️ Target Organ**     | Heart / Cardiovascular                                                                   |
| **📅 Last Accessed**    | June 30, 2026                                                                            |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification                                                                |
| **📐 Image Size**       | N/A (Tabular data)                                                                       |
| **📁 Data Format**      | CSV                                                                                      |
| **👥 Demographics**     | ✅ Age, Sex                                                                               |
| **🔄 Train/Test Split** | ❌ Not provided (303 observations)                                                        |

#### 📊 Dataset Composition

| Category                  | Details                                                  |
|---------------------------|----------------------------------------------------------|
| **📊 Total Instances**    | 303 observations                                         |
| **🔢 Features**           | 14 clinical features + 1 target variable                 |
| **📦 Total Size**         | ~11.32 kB                                                |
| **🏥 Source Institution** | Cleveland Clinic Foundation (UCI Heart Disease Database) |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification of heart attack risk
- **Number of Classes**: 2️⃣
- ✅ Less chance of heart attack (0)
- ⚠️ More chance of heart attack (1)

#### 💡 Usage Notes

- ✅ Classic dataset for benchmarking binary classification algorithms in healthcare
- ✅ Includes key cardiovascular indicators (cholesterol, ECG, thalassemia, etc.)
- ✅ Small dataset size ideal for educational purposes and quick prototyping
- 📚 Required to cite the original Kaggle repository
- 🔐 CC0: Public Domain

#### ⚠️ Usage Considerations

| Aspect                   | Recommendation                                                                       |
|--------------------------|--------------------------------------------------------------------------------------|
| **🔍 Small Sample Size** | 303 instances may lead to overfitting; use strong regularization or cross-validation |
| **🧪 Class Imbalance**   | Verify class distribution; apply class weighting if necessary                        |
| **📐 Feature Selection** | Remove highly correlated features to reduce multicollinearity                        |
| **🔐 Licensing**         | Public Domain; free for any use                                                      |

#### 💡 Suggested Preprocessing Pipeline

1. **Load CSV**: Parse `heart.csv` using pandas.
2. **Encode categoricals**: One-hot encode `cp`, `rest_ecg`, `thal`, etc.
3. **Scale features**: Apply StandardScaler to numerical features.
4. **Cross-validation**: Use stratified k-fold cross-validation due to small dataset size.
5. **Evaluation metrics**: Report accuracy, precision, recall, F1-score, and AUC-ROC.

#### 🔗 Associated Resources

- **Kaggle Repository**: https://www.kaggle.com/datasets/sonialikhan/heart-attack-analysis-and-prediction-dataset
- **Related Datasets**: [Heart Failure Prediction](#-heart-failure-prediction-dataset)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{hinaismail2022heart,
  title={Heart Attack Analysis & Prediction Dataset},
  author={Hina Ismail},
  year={2022},
  publisher={Kaggle},
  url={https://www.kaggle.com/datasets/sonialikhan/heart-attack-analysis-and-prediction-dataset}
}
```

---

### 🖼️ PAD-UFES-20: Skin Lesion Dataset

**Study**: Pacheco, A. G. C., et al. (2020). PAD-UFES-20: a skin lesion dataset composed of patient data and clinical
images collected from smartphones. Mendeley Data.
[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                         |
|-------------------------|-------------------------------------------------|
| **📛 Title**            | PAD-UFES-20: Skin Lesion Dataset                |
| **🔗 Source**           | https://data.mendeley.com/datasets/zr7vgbcyr2/1 |
| **🖼️ Target Organ**    | Skin                                            |
| **📅 Last Accessed**    | June 30, 2026                                   |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                   |
| **📐 Image Size**       | Variable (smartphone cameras)                   |
| **📁 Data Format**      | PNG (images), CSV (metadata)                    |
| **👥 Demographics**     | ✅ Age, Skin type, Location, Diameter            |
| **🔄 Train/Test Split** | ❌ Not provided (2,298 images)                   |

#### 📊 Dataset Composition

| Category                  | Details                                               |
|---------------------------|-------------------------------------------------------|
| **🖼️ Total Images**      | 2,298 skin lesion images                              |
| **🏥 Imaging Modality**   | Smartphone clinical photography                       |
| **🎨 Color Format**       | RGB                                                   |
| **📦 Total Size**         | ~3.35 GB (compressed)                                 |
| **🏥 Source Institution** | Universidade Federal do Espírito Santo (UFES), Brazil |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of skin lesions
- **Number of Classes**: 6️⃣
- ⚫ Basal Cell Carcinoma (BCC)
- 🔴 Squamous Cell Carcinoma (SCC)
- 🟡 Actinic Keratosis (ACK)
- 🟤 Seborrheic Keratosis (SEK)
- 🟠 Melanoma (MEL)
- 🟢 Nevus (NEV)

#### 💡 Usage Notes

- ✅ Unique dataset captured using everyday smartphone devices (real-world conditions)
- ✅ Includes rich clinical metadata (22 features per sample)
- ✅ Biopsy-proven labels for malignant classes (BCC, SCC, MEL)
- 📚 Required to cite the original Mendeley Data repository
- 🔐 Verify usage terms on Mendeley Data; typically CC BY 4.0

#### ⚠️ Usage Considerations

| Aspect                      | Recommendation                                                                  |
|-----------------------------|---------------------------------------------------------------------------------|
| **🔍 Class Imbalance**      | Verify per-class distribution; apply class-weighted loss if needed              |
| **📐 Resolution Variance**  | Smartphone images vary in quality; standardize dimensions and apply enhancement |
| **🧪 Metadata Integration** | Leverage clinical features (age, location) to improve model performance         |
| **🔐 Ethical Compliance**   | Dataset contains patient data; adhere to institutional review requirements      |

#### 💡 Suggested Preprocessing Pipeline

1. **Load metadata**: Parse CSV to map image paths to diagnostic labels and clinical features.
2. **Standardize input format**: Convert all images to a consistent color space and fixed resolution.
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide statistics.
4. **Augmentation **(training only): Incorporate rotation, flipping, and color jittering to simulate varied lighting.
5. **Stratified evaluation**: Report per-class precision, recall, F1-score, and confusion matrices.

#### 🔗 Associated Resources

- **Mendeley Data Repository**: https://data.mendeley.com/datasets/zr7vgbcyr2/1
- **Related Datasets**: [ISIC 2019](#-isic-2019-skin-lesion-analysis-toward-melanoma-detection)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{pacheco2020pad,
  title={PAD-UFES-20: A skin lesion dataset composed of patient data and clinical images collected from smartphones},
  author={Pacheco, Andre GC and Lima, Gustavo R and Salomao, Amanda S and Krohling, Breno and Biral, Igor P and De Angelo, Gabriel G and Alves Jr, F{\'a}bio CR and Esgario, Jos{\'e} GM and Simora, Alana C and Castro, Pedro BC and others},
  journal={Data in brief},
  volume={32},
  pages={106221},
  year={2020},
  publisher={Elsevier}
}
```

---

### 🩸 Diabetes Dataset (AIM '94)

**Study**: Kahn, M. Diabetes [Dataset]. UCI Machine Learning Repository.
[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                         |
|-------------------------|-------------------------------------------------|
| **📛 Title**            | Diabetes Dataset (AIM '94)                      |
| **🔗 Source**           | https://archive.ics.uci.edu/dataset/34/diabetes |
| **🩸 Target Organ**     | Blood / Metabolic                               |
| **📅 Last Accessed**    | June 30, 2026                                   |
| **🎯 Supported Tasks**  | 📊 Time-Series Analysis, 🏷️ Classification     |
| **📐 Image Size**       | N/A (Tabular time-series data)                  |
| **📁 Data Format**      | TXT / CSV                                       |
| **👥 Demographics**     | ❌ Not specified                                 |
| **🔄 Train/Test Split** | ❌ Not provided (Single patient record)          |

#### 📊 Dataset Composition

| Category                  | Details                                              |
|---------------------------|------------------------------------------------------|
| **📊 Total Instances**    | 1 (Patient record with multiple time-series entries) |
| **🔢 Features**           | 4 fields (Date, Time, Code, Value)                   |
| **📦 Total Size**         | ~183.2 KB (compressed)                               |
| **🏥 Source Institution** | UCI Machine Learning Repository                      |

#### 📊 Time-Series Task Details

- **Task Type**: Time-series analysis of blood glucose and insulin doses
- **Event Codes**:
- 💉 33-35: Insulin doses (Regular, NPH, UltraLente)
- 🩸 48-65: Blood glucose measurements (various times)
- 🍽️ 66-68: Meal ingestion events
- 🏃 69-71: Exercise activity events

#### 💡 Usage Notes

- ✅ Classic dataset for time-series forecasting and event detection in healthcare
- ✅ Contains realistic timestamps for electronic records and logical slots for paper records
- ✅ Suitable for research on irregular time-series and missing data imputation
- 📚 Required to cite the original UCI Machine Learning Repository
- 🔐 Licensed under CC BY 4.0; attribution required

#### ⚠️ Usage Considerations

| Aspect                      | Recommendation                                                                   |
|-----------------------------|----------------------------------------------------------------------------------|
| **📐 Irregular Timestamps** | Electronic and paper records have different time resolutions; handle accordingly |
| **🧪 Single Patient**       | Dataset represents a single patient; not suitable for population-level modeling  |
| **🔍 Event Detection**      | Use sequence models (e.g., LSTMs, Transformers) for event prediction             |
| **🔐 Licensing**            | CC BY 4.0; free for any use with attribution                                     |

#### 💡 Suggested Preprocessing Pipeline

1. **Parse TXT/CSV**: Load the tab-separated file into a pandas DataFrame.
2. **Datetime parsing**: Convert Date and Time fields into standard datetime objects.
3. **Handle time slots**: Assign fixed times to paper records (08:00, 12:00, 18:00, 22:00).
4. **Feature engineering**: Extract hour-of-day, day-of-week, and time-since-last-event features.
5. **Sequence modeling**: Format data into sequences for RNNs or Transformers; handle missing values via interpolation.

#### 🔗 Associated Resources

- **UCI Repository**: https://archive.ics.uci.edu/dataset/34/diabetes
- **Related Publications**: Kahn, M. (1994). "Diabetes." UCI Machine Learning Repository.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{kahn1994diabetes,
  title={Diabetes},
  author={Kahn, M.},
  year={1994},
  publisher={UCI Machine Learning Repository},
  doi={10.24432/C5T59G},
  url={https://archive.ics.uci.edu/dataset/34/diabetes}
}
```

---

### 🫀 Digital Pathology Dataset for Breast Cancer Diagnosis

**Study**: Naghshineh Kani, S., Soyak, B. C., Gokce, M., Duyar, Z., Alicikus, H., Yapıcıer, Ö., & Oner, M. U. (2024).
Digital Pathology Dataset for Breast Cancer Diagnosis [Data set]. Zenodo.
[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                               |
|-------------------------|-------------------------------------------------------|
| **📛 Title**            | Digital Pathology Dataset for Breast Cancer Diagnosis |
| **🔗 Source**           | https://zenodo.org/records/14131968                   |
| **🫀 Target Organ**     | Breast                                                |
| **📅 Last Accessed**    | July 03, 2026                                         |
| **🎯 Supported Tasks**  | 🎭 Segmentation (Tissue Region)                       |
| **📐 Image Size**       | Variable (Whole Slide Images)                         |
| **📁 Data Format**      | .svs (Aperio) in ZIP archives                         |
| **👥 Demographics**     | ❌ Not included                                        |
| **🔄 Train/Test Split** | ❌ Not provided                                        |

#### 📊 Dataset Composition

| Category                  | Details                                                              |
|---------------------------|----------------------------------------------------------------------|
| **🖼️ Total Slides**      | 235 Whole Slide Images (WSIs)                                        |
| **🔬 Imaging Modality**   | Brightfield histopathology (H&E and IHC stains)                      |
| **📦 File Structure**     | 36 ZIP files for H&E (72 slides) + 55 ZIP files for IHC (163 slides) |
| **🏥 Source Institution** | Bahçeşehir University Medical School, Turkey                         |

#### 🎭 Segmentation Task Details

- **Task Type**: Binary/Multi-class tissue region segmentation
- **Annotation Targets**: Tissue regions vs. background in H&E and IHC stained slides
- **Associated Code
  **: [Tissue Region Segmentation Code](https://github.com/sepidehnaghshineh/Tissue-region-segmentation-in-HE-and-IHC-stained-pathology-slides)

#### 💡 Usage Notes

- ✅ High-quality IHC and H&E WSIs provided in standard .svs format
- ✅ Suitable for benchmarking tissue region segmentation algorithms across different staining modalities
- ✅ Includes associated Python code for tissue region segmentation using deep learning
- 📚 Required to cite the original Zenodo repository when using this dataset
- 🔐 Distributed under CC BY 4.0; attribution required

#### ⚠️ Usage Considerations

| Aspect                    | Recommendation                                                                            |
|---------------------------|-------------------------------------------------------------------------------------------|
| **📦 Large File Sizes**   | WSIs are massive; ensure adequate storage and use libraries like `OpenSlide` or `libvips` |
| **🎨 Stain Variability**  | Dataset includes both H&E and IHC; models may need to handle stain-specific features      |
| **🔐 Ethical Compliance** | Approved by Bahçeşehir University Clinical Research IRB (Approval No: 2022-10/03)         |

#### 💡 Suggested Preprocessing Pipeline

1. **Extract archives**: Unzip the 91 ZIP files containing the .svs WSIs.
2. **Load WSIs**: Use `OpenSlide` or `tifffile` to read the high-resolution .svs images.
3. **Tissue detection**: Apply thresholding or the provided deep learning model to mask out background/glass regions.
4. **Patch extraction**: Extract overlapping or non-overlapping tiles for training segmentation models.
5. **Evaluation**: Compute Dice/IoU scores for tissue vs. background segmentation.

#### 🔗 Associated Resources

- **Zenodo Repository**: https://zenodo.org/records/14131968
- **Code Repository
  **: https://github.com/sepidehnaghshineh/Tissue-region-segmentation-in-HE-and-IHC-stained-pathology-slides

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{naghshinehkani2024digital,
  author = {Naghshineh Kani, Sepideh and Soyak, Burak Can and Gokce, Melih and Duyar, Zeynep and Alicikus, Hasan and Yapıcıer, Özlem and Oner, Mustafa Umit},
  title = {Digital Pathology Dataset for Breast Cancer Diagnosis},
  year = {2024},
  publisher = {Zenodo},
  doi = {10.5281/zenodo.14131968},
  url = {https://doi.org/10.5281/zenodo.14131968}
}
```

---

### 🫀 2 Million Histological Images of Breast Cancer Tumors with HER2 Labels

**Study**: Valieris, R., Martins, L., Defelicibus, A., Osorio, C. A. B. T., & Bueno, A. P. (2023). 2 million
histological images of breast cancer tumors with her2 labels [Data set]. Zenodo.
[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                |
|-------------------------|------------------------------------------------------------------------|
| **📛 Title**            | 2 Million Histological Images of Breast Cancer Tumors with HER2 Labels |
| **🔗 Source**           | https://zenodo.org/records/8383580                                     |
| **🫀 Target Organ**     | Breast                                                                 |
| **📅 Last Accessed**    | July 03, 2026                                                          |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification (HER2 Status)                            |
| **📐 Image Size**       | 256 × 256 pixels (at 0.5 µm/pixel)                                     |
| **📁 Data Format**      | Image patches (ZIP)                                                    |
| **👥 Demographics**     | ❌ Not included (N = 504 patients)                                      |
| **🔄 Train/Test Split** | ❌ Not provided                                                         |

#### 📊 Dataset Composition

| Category                  | Details                                                     |
|---------------------------|-------------------------------------------------------------|
| **🖼️ Total Patches**     | 2,051,877 image patches                                     |
| **🔬 Imaging Modality**   | Brightfield histopathology (H&E stained, 40x magnification) |
| **🏥 Source Institution** | A. C. Camargo Cancer Center (ACCCC), Brazil                 |
| **📦 Total Size**         | ~35.6 GB (compressed)                                       |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of HER2 status based on H&E morphology
- **Number of Classes**: 3️⃣
- 🔵 HER2-negative (IHC 0)
- 🟡 HER2-low (IHC 1+ or IHC 2+ / ISH-)
- 🔴 HER2-high (IHC 3+ or IHC 2+ / ISH+)

#### 💡 Usage Notes

- ✅ Massive scale (2M+ patches) suitable for training deep learning models from scratch or self-supervised learning
- ✅ Focuses on the clinically relevant "HER2-low" category, which is a newer target for antibody-drug conjugates
- ✅ Patches are pre-filtered to contain only tumor regions and their microenvironment using a ConvNext-tiny model
- 📚 Required to cite the original Zenodo repository and the associated journal article
- 🔐 Distributed under CC BY 4.0; attribution required

#### ⚠️ Usage Considerations

| Aspect                    | Recommendation                                                                                      |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**    | Verify distribution across HER2-negative, low, and high; apply class weighting if needed            |
| **📦 Large Dataset**      | 35.6 GB requires significant storage; consider streaming data or using efficient data loaders       |
| **🧪 Patch-Level Focus**  | Patches are 256x256; whole-slide inference requires Multiple Instance Learning (MIL) or aggregation |
| **🔐 Ethical Compliance** | Approved by the ethics committee of the Fundação Antônio Prudente                                   |

#### 💡 Suggested Preprocessing Pipeline

1. **Extract archive**: Unzip the 35.6 GB `dataset.zip` file.
2. **Organize by label**: Arrange patches into class-labeled subfolders (`HER2-negative`, `HER2-low`, `HER2-high`).
3. **Standardize input**: Confirm 256×256 dimensions; apply intensity normalization.
4. **Augmentation **(training only): Incorporate rotation, flipping, and color jittering; preserve morphological
   integrity.
5. **Stratified splitting**: Implement patient-aware or slide-aware partitioning to prevent data leakage.
6. **Evaluation metrics**: Report macro-averaged F1-score, AUC-ROC, and confusion matrices, especially for the HER2-low
   class.

#### 🔗 Associated Resources

- **Zenodo Repository**: https://zenodo.org/records/8383580
- **Code Repository**: https://github.com/tojallab/wsi-mil
- **Related Publication**: Valieris, R., et al. "2 million histological images of breast cancer tumors with HER2
  labels." *Breast Cancer Research* (2024).

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{valieris2023million,
  author = {Valieris, Renan and Martins, Luan and Defelicibus, Alexandre and Osorio, Cynthia Aparecida Bueno de Toledo and Bueno, Adriana Passos},
  title = {2 million histological images of breast cancer tumors with her2 labels},
  year = {2023},
  publisher = {Zenodo},
  doi = {10.5281/zenodo.8383580},
  url = {https://doi.org/10.5281/zenodo.8383580}
}
```

---

### 🫀 Breast Carcinoma Histological Images (Agios Pavlos Hospital)

**Study**: Zioga, C., Kamas, A., Patsiaoura, K., Dimitropoulos, K., Barmpoutis, P., & Grammalidis, N. (2017). Breast
carcinoma histological images from the Department of Pathology, "Agios Pavlos" General Hospital of Thessaloniki,
Greece [Data set]. Zenodo.
[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                      |
|-------------------------|--------------------------------------------------------------|
| **📛 Title**            | Breast Carcinoma Histological Images (Agios Pavlos Hospital) |
| **🔗 Source**           | https://zenodo.org/records/834910                            |
| **🫀 Target Organ**     | Breast                                                       |
| **📅 Last Accessed**    | July 03, 2026                                                |
| **🎯 Supported Tasks**  | 🏷️ Ordinal Classification (Tumor Grading)                   |
| **📐 Image Size**       | 1280 × 960 pixels                                            |
| **📁 Data Format**      | Image files (ZIP)                                            |
| **👥 Demographics**     | 21 patients                                                  |
| **🔄 Train/Test Split** | ❌ Not provided                                               |

#### 📊 Dataset Composition

| Category                  | Details                                                 |
|---------------------------|---------------------------------------------------------|
| **🖼️ Total Images**      | 300 annotated histological images                       |
| **🔬 Imaging Modality**   | Brightfield histopathology (H&E stained)                |
| **🏥 Source Institution** | "Agios Pavlos" General Hospital of Thessaloniki, Greece |
| **📦 Total Size**         | ~373.8 MB (compressed)                                  |

#### 🏷️ Classification Task Details

- **Task Type**: Ordinal multiclass classification of invasive ductal carcinoma grading
- **Number of Classes**: 3️⃣ (Ordered severity scale)
- 🟢 Grade 1 (Well differentiated)
- 🟡 Grade 2 (Moderately differentiated)
- 🔴 Grade 3 (Poorly differentiated)

#### 💡 Usage Notes

- ✅ Suitable for benchmarking traditional ML and CNN architectures for breast cancer grading
- ✅ Images are grouped into folders corresponding to grades 1-3
- ✅ Relatively small dataset size (300 images) ideal for few-shot learning, transfer learning, or data augmentation
  studies
- 📚 Required to cite the original Zenodo repository and the associated PLOS ONE publication
- 🔐 Distributed under CC BY 4.0; attribution required

#### ⚠️ Usage Considerations

| Aspect                       | Recommendation                                                                                 |
|------------------------------|------------------------------------------------------------------------------------------------|
| **🔍 Small Sample Size**     | 300 images across 21 patients; employ strong regularization, augmentation, or cross-validation |
| **🧪 Ordinal Structure**     | Grades represent ordered severity; consider ordinal regression or monotonic constraints        |
| **📐 Resolution Handling**   | Images are 1280x960; resize to model-compatible dimensions (e.g., 224x224)                     |
| **🧭 Domain Generalization** | Single-center cohort; validate on external datasets for clinical deployment                    |

#### 💡 Suggested Preprocessing Pipeline

1. **Extract archive**: Unzip the `Dataset.zip` file containing the grade-labeled folders.
2. **Standardize resolution**: Resize images to a uniform dimension (e.g., 224×224 or 512×512) while preserving aspect
   ratio.
3. **Color normalization**: Apply stain normalization (e.g., Macenko method) to mitigate inter-slide H&E variability.
4. **Augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering.
5. **Cross-validation**: Use k-fold cross-validation due to the small dataset size.
6. **Evaluation metrics**: Report per-class precision/recall, weighted kappa for ordinal agreement, and macro-averaged
   F1-score.

#### 🔗 Associated Resources

- **Zenodo Repository**: https://zenodo.org/records/834910
- **Related Publication**: Dimitropoulos, K., et al. "Grading of invasive breast carcinoma through Grassmannian VLAD
  encoding." *PLOS ONE* (2017).

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{zioga2017breast,
  author = {Zioga, Christina and Kamas, Athanasios and Patsiaoura, Kalliopi and Dimitropoulos, Kosmas and Barmpoutis, Panagiotis and Grammalidis, Nikos},
  title = {Breast carcinoma histological images from the Department of Pathology, "Agios Pavlos" General Hospital of Thessaloniki, Greece},
  year = {2017},
  publisher = {Zenodo},
  doi = {10.5281/zenodo.834910},
  url = {https://doi.org/10.5281/zenodo.834910}
}
```

---

### 🧠 Brain Tumor Multimodal Image (CT & MRI)

**Author**: Md. Golam Murtoza. Kaggle Dataset.
[🔝 Back to Summary](#-dataset-summary)

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

### 👁️ Eyepacs, Aptos, Messidor Diabetic Retinopathy: Unified Dataset

**Study**: Canipek, A. S., et al. (2024). Eyepacs, Aptos, Messidor Diabetic Retinopathy. Kaggle.

[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

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


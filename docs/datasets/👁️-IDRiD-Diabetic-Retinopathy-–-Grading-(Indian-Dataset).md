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


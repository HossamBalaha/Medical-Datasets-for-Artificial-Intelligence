### 🫁 COVIDx CT: A Large-Scale Chest CT Dataset for COVID-19 Detection

**Study**: Gunraj, H., Wang, L., & Wong, A. (2020). COVIDNet-CT: A Tailored Deep Convolutional Neural Network Design for
Detection of COVID-19 Cases From Chest CT Images. *Frontiers in Medicine*, 7, 1025. & Gunraj, H., Sabri, A., Koff, D., &
Wong, A. (2022). COVID-Net CT-2: Enhanced Deep Neural Networks for Detection of COVID-19 From Chest CT Images Through
Bigger, More Diverse Learning. *Frontiers in Medicine*, 8, 729287.

[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

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


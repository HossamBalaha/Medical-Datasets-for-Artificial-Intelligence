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


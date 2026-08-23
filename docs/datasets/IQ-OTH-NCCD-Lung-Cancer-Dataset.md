### 🫁 IQ-OTH/NCCD Lung Cancer Dataset

**Study**: AL-Huseiny, M., & alyasriy, H. (2021). The IQ-OTHNCCD lung cancer dataset. *Mendeley Data*, V2.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                      |
|-------------------------|------------------------------------------------------------------------------|
| **📛 Title**            | IQ-OTH/NCCD - Lung Cancer Dataset                                            |
| **🔗 Source**           | https://www.kaggle.com/datasets/adityamahimkar/iqothnccd-lung-cancer-dataset |
| **🫁 Target Organ**     | Lungs                                                                        |
| **📅 Last Accessed**    | August 14, 2026                                                              |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                                                |
| **📐 Image Size**       | Variable (extracted slices from DICOM)                                       |
| **📁 Data Format**      | PNG (.png)                                                                   |
| **👥 Demographics**     | ✅ 110 cases (varied gender, age, educational attainment, residence)          |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                       |

#### 📊 Dataset Composition

| Category                | Details                                                               |
|-------------------------|-----------------------------------------------------------------------|
| **🖼️ Total Images**    | 1,190 CT scan slices                                                  |
| **🏥 Imaging Modality** | Computed Tomography (CT)                                              |
| **🔬 Scanner**          | SOMATOM (Siemens); 120 kV, 1 mm slice thickness                       |
| **📦 Total Size**       | ~210.04 MB                                                            |
| **🏥 Source**           | Iraq-Oncology Teaching Hospital / National Center for Cancer Diseases |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of lung cancer stages
- **Number of Classes**: 3️⃣
    - ✅ Normal (55 cases)
    - 🟡 Benign (15 cases)
    - 🔴 Malignant (40 cases)

#### 💡 Usage Notes

- ✅ Valuable dataset for lung cancer detection and staging from CT scan slices.
- ✅ Expertly marked by oncologists and radiologists at two specialist centers.
- ✅ Includes diverse demographic representation from the middle region of Iraq.
- 📚 Required to cite the original Mendeley Data publication when using this dataset.
- 🔐 License: Data files © Original Authors; verify specific terms for commercial use.

#### ⚠️ Usage Considerations

| Aspect                            | Recommendation                                                                                                                  |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Slice-level vs. Case-level** | The dataset contains slices, but labels are per case. Aggregation (e.g., majority voting) is required for case-level diagnosis. |
| **📐 Resolution Variance**        | Slices vary in dimensions; apply uniform resizing and padding prior to training.                                                |
| **🧪 Class Imbalance**            | Benign cases (15) are significantly underrepresented compared to Normal (55) and Malignant (40); apply class weighting.         |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Ingest PNG slices and map them to their respective case IDs.
2. **Standardize input format**: Resize slices to a fixed resolution (e.g., 224x224 or 512x512).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or apply CT-specific windowing if raw HU values are
   reconstructed.
4. **Case-aware splitting**: Partition data by case ID, not by slice, to prevent severe data leakage.
5. **Aggregation strategy**: Design a pipeline that aggregates slice-level predictions into a single case-level
   diagnosis.
6. **Stratified evaluation**: Report case-level accuracy, sensitivity, specificity, and AUC-ROC.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
bibtex
@dataset{alyasriy2021iqothnccd,
  author = {alyasriy, hamdalla and AL-Huseiny, Muayed},
  title = {The IQ-OTHNCCD lung cancer dataset},
  year = {2021},
  publisher = {Mendeley Data},
  version = {2},
  doi = {10.17632/bhmdr45bh2.2},
  url = {https://data.mendeley.com/datasets/bhmdr45bh2/2}

}
```

---

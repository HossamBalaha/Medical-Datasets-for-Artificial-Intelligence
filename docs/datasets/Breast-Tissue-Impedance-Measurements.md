### 🫀 Breast Tissue Impedance Measurements

**Study**: Jossinet, J. (2010). Breast Tissue. UCI Machine Learning Repository.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                            |
|-------------------------|------------------------------------------------------------------------------------|
| **📛 Title**            | Breast Tissue Impedance Measurements                                               |
| **🔗 Source**           | https://www.kaggle.com/datasets/tarktunataalt/breast-tissue-impedance-measurements |
| **🫀 Target Organ**     | Breast                                                                             |
| **📅 Last Accessed**    | October 06, 2026                                                                   |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification, 🔍 Clustering                                       |
| **📐 Image Size**       | N/A (Tabular multivariate data)                                                    |
| **📁 Data Format**      | CSV                                                                                |
| **👥 Demographics**     | ❌ Not included                                                                     |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                             |

#### 📊 Dataset Composition

| Category               | Details                                                    |
|------------------------|------------------------------------------------------------|
| **📊 Total Instances** | 106 freshly excised breast tissue samples                  |
| **🔢 Features**        | 9 real-valued impedance spectrum features + 1 target class |
| **📦 Total Size**      | ~16.36 kB                                                  |
| **🏥 Source**          | UCI Machine Learning Repository                            |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of breast tissue types based on electrical impedance spectra
- **Number of Classes**: 6️⃣
    - 🔴 Carcinoma (car)
    - 🟡 Fibro-adenoma (fad)
    - 🟠 Mastopathy (mas)
    - 🟢 Glandular (gla)
    - 🔵 Connective (con)
    - ⚪ Adipose (adi)
- **Features Included**: I0 (Impedivity at zero frequency), PA500 (Phase angle at 500 KHz), HFS (High-frequency slope),
  DA (Impedance distance), AREA, A/DA, MAX IP, DR, P.

#### 💡 Usage Notes

- ✅ Unique tabular dataset exploring the application of Electrical Impedance Spectroscopy (EIS) for breast tissue
  characterization.
- ✅ Suitable for benchmarking traditional machine learning classifiers (e.g., SVM, Random Forest) and clustering
  algorithms.
- ✅ Classes can be merged into 4 categories (merging fibro-adenoma, mastopathy, and glandular) for simplified
  classification tasks, as noted by the original authors.
- 📚 Required to cite the original UCI Machine Learning Repository in publications.
- 🔐 Distributed under CC BY-SA 4.0.

#### ⚠️ Usage Considerations

| Aspect                   | Recommendation                                                                                                                    |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Small Sample Size** | Only 106 instances; employ strong regularization, leave-one-out cross-validation (LOOCV), or few-shot learning techniques.        |
| **📐 Feature Scaling**   | Features have varying scales; apply StandardScaler or MinMaxScaler prior to modeling.                                             |
| **🧪 Class Imbalance**   | Verify distribution; consider merging the 3 hard-to-discriminate classes (fad, mas, gla) as suggested in the dataset description. |

#### 💡 Suggested Preprocessing Pipeline

1. **Load CSV**: Parse the dataset using pandas.
2. **Handle categorical target**: One-hot encode or label-encode the 'Class' column.
3. **Feature scaling**: Apply StandardScaler to all 9 impedance features to ensure equal weighting in distance-based
   algorithms.
4. **Dimensionality reduction **(optional): Apply PCA to visualize the impedance spectrum clusters in 2D/3D space.
5. **Stratified cross-validation**: Use stratified k-fold (or LOOCV) to maintain class proportions and obtain robust
   performance estimates.
6. **Evaluation metrics**: Report macro-averaged precision, recall, and F1-score due to the multiclass nature and
   potential imbalance.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@misc{jossinet2010breast,
    author = {Jossinet, J.},
    title = {Breast Tissue},
    year = {2010},
    publisher = {UCI Machine Learning Repository},
    doi = {10.24432/C5P31H},
    url = {https://archive.ics.uci.edu/dataset/192/breast+tissue}
}
```

---

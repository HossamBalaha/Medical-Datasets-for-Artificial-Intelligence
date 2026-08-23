### 🫁 Lung Cancer

**Study**: mysar ahmad bhat. (2021). Lung Cancer. Kaggle.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                    |
|-------------------------|------------------------------------------------------------|
| **📛 Title**            | Lung Cancer                                                |
| **🔗 Source**           | https://www.kaggle.com/datasets/mysarahmadbhat/lung-cancer |
| **🫁 Target Organ**     | Lungs                                                      |
| **📅 Last Accessed**    | August 21, 2026                                            |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification                                  |
| **📐 Image Size**       | N/A (Tabular clinical data)                                |
| **📁 Data Format**      | CSV                                                        |
| **👥 Demographics**     | ✅ Gender, Age                                              |
| **🔄 Train/Test Split** | ❌ Not provided (284 instances)                             |

#### 📊 Dataset Composition

| Category               | Details                                              |
|------------------------|------------------------------------------------------|
| **📊 Total Instances** | 284 patient records                                  |
| **🔢 Features**        | 15 clinical/symptomatic features + 1 target variable |
| **📦 Total Size**      | ~11.28 kB                                            |
| **🏥 Source**          | Online lung cancer prediction system survey          |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification of lung cancer risk based on symptoms and lifestyle factors
- **Number of Classes**: 2️⃣
    - ✅ NO (No Lung Cancer)
    - ⚠️ YES (Lung Cancer Present)
- **Key Features**: Gender, Age, Smoking, Yellow fingers, Anxiety, Peer pressure, Chronic Disease, Fatigue, Allergy,
  Wheezing, Alcohol, Coughing, Shortness of Breath, Swallowing Difficulty, Chest pain.

#### 💡 Usage Notes

- ✅ Suitable for benchmarking tabular machine learning models (e.g., Random Forest, XGBoost, Logistic Regression) for
  healthcare risk prediction.
- ✅ Provides a lightweight, accessible dataset for educational purposes and rapid prototyping of symptom-based
  diagnostic tools.
- 📚 Recommended to cite the original Kaggle repository when using this dataset.
- 🔐 License: CC0: Public Domain

#### ⚠️ Usage Considerations

| Aspect                      | Recommendation                                                                                                                           |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Small Sample Size**    | Only 284 instances; employ strong regularization, cross-validation, or synthetic data generation (e.g., SMOTE) to prevent overfitting.   |
| **🧪 Categorical Encoding** | Features like Gender and binary symptoms (YES=2, NO=1) require proper encoding (e.g., one-hot or label encoding) before model ingestion. |
| **📐 Feature Scaling**      | Numerical features (e.g., Age) should be scaled (StandardScaler or MinMaxScaler) for distance-based algorithms.                          |
| **🔐 Clinical Validity**    | Derived from an online survey system; validate findings against clinically verified cohorts before real-world application.               |

#### 💡 Suggested Preprocessing Pipeline

1. **Load CSV**: Parse the dataset using pandas or similar libraries.
2. **Handle Encoding**: Convert categorical variables (e.g., Gender) and binary indicators into appropriate numerical
   formats.
3. **Scale Features**: Apply StandardScaler or MinMaxScaler to numerical features like Age.
4. **Address Imbalance**: Check the target distribution; apply class weighting or resampling techniques if necessary.
5. **Cross-validation**: Use stratified k-fold cross-validation to ensure robust performance estimation given the small
   dataset size.
6. **Evaluation metrics**: Report accuracy, precision, recall, F1-score, and AUC-ROC, prioritizing recall to minimize
   false negatives in a medical context.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{bhat2021lungcancer,
  author = {bhat, mysar ahmad},
  title = {Lung Cancer},
  year = {2021},
  publisher = {Kaggle},
  url = {https://www.kaggle.com/datasets/mysarahmadbhat/lung-cancer}
}
```

---

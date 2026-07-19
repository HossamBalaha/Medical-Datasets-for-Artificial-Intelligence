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


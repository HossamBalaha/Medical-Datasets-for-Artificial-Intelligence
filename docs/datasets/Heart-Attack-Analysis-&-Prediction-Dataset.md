### ❤️ Heart Attack Analysis & Prediction Dataset

**Study**: Hina Ismail, et al. (2022). Heart Attack Analysis & Prediction Dataset. Kaggle.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

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
- **Related Datasets**: [Heart Failure Prediction](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)

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


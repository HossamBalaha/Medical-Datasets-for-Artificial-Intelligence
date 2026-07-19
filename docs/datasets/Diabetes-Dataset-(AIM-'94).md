### 🩸 Diabetes Dataset (AIM '94)

**Study**: Kahn, M. Diabetes [Dataset]. UCI Machine Learning Repository.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

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


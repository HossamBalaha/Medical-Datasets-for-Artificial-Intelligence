### ❤️ Cardiomegaly Disease Prediction Using CNN

**Study**: Verma, H. (2021). Cardiomegaly Disease Prediction Using CNN. Kaggle.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                              |
|-------------------------|--------------------------------------------------------------------------------------|
| **📛 Title**            | Cardiomegaly Disease Prediction Using CNN                                            |
| **🔗 Source**           | https://www.kaggle.com/datasets/rahimanshu/cardiomegaly-disease-prediction-using-cnn |
| **❤️ Target Organ**     | Heart / Cardiovascular                                                               |
| **📅 Last Accessed**    | August 13, 2026                                                                      |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification                                                            |
| **📐 Image Size**       | 128 × 128 pixels (preprocessed)                                                      |
| **📁 Data Format**      | JPEG/PNG (.jpg/.png)                                                                 |
| **👥 Demographics**     | ❌ Not included                                                                       |
| **🔄 Train/Test Split** | ✅ Yes (1:1 ratio between training and testing sets)                                  |

#### 📊 Dataset Composition

| Category                | Details                                                                |
|-------------------------|------------------------------------------------------------------------|
| **🖼️ Total Images**    | 5,552 files                                                            |
| **🏥 Imaging Modality** | Radiographic X-ray (Derived from the original NIH Chest X-ray Dataset) |
| **📦 Total Size**       | ~63.76 MB                                                              |
| **🏥 Source**           | NIH Clinical Center (via Kaggle adaptation)                            |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification of cardiomegaly presence
- **Number of Classes**: 2️⃣
    - ❤️ Cardiomegaly (True)
    - ✅ Normal (False)

#### 💡 Usage Notes

- ✅ Preprocessed with Contrast Limited Adaptive Histogram Equalization (CLAHE) to enhance local contrast.
- ✅ Resized to a uniform 128x128 resolution, making it lightweight and ideal for rapid prototyping or edge-device
  deployment.
- ✅ Balanced 1:1 train/test split simplifies initial model training and evaluation.
- 📚 Recommended to cite the original Kaggle repository and acknowledge the NIH Chest X-ray source.
- 🔐 License: CC0: Public Domain

#### ⚠️ Usage Considerations

| Aspect                 | Recommendation                                                                                                                                                          |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **📐 Low Resolution**  | 128x128 is quite small for medical imaging; fine-grained features may be lost. Consider super-resolution or using the original NIH dataset for high-performance models. |
| **🔍 CTR Calculation** | The original NIH dataset allows for Cardiothoracic Ratio (CTR) calculation. Consider using this as an auxiliary regression task or for label verification.              |
| **🧪 Domain Shift**    | Ensure models trained on this preprocessed subset generalize well to raw, unprocessed clinical X-rays.                                                                  |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Ingest the `train` and `test` folders using standard framework utilities.
2. **Verify dimensions**: Confirm all images are 128x128; resize if your specific architecture requires a different
   input size.
3. **Intensity normalization**: Scale pixel values to [0, 1]. Since CLAHE is already applied, avoid aggressive contrast
   adjustments.
4. **Augmentation**: Incorporate slight rotation, flipping, and translation to improve robustness to patient
   positioning.
5. **Stratified evaluation**: Report accuracy, sensitivity, specificity, and AUC-ROC to comprehensively assess
   diagnostic performance.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{verma2021cardiomegaly,
  author = {Verma, Himanshu},
  title = {Cardiomegaly Disease Prediction Using CNN},
  year = {2021},
  publisher = {Kaggle},
  url = {https://www.kaggle.com/datasets/rahimanshu/cardiomegaly-disease-prediction-using-cnn}
}
```

---

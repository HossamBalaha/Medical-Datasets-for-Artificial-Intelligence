### 🫁 COVID-19 + Pneumonia + Normal Chest X-Ray

**Study**: Kumar, S., Shastri, S., Mahajan, S., et al. (2022). CheXImageNet / LiteCovidNet. Kaggle.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                                         |
|-------------------------|-------------------------------------------------------------------------------------------------|
| **📛 Title**            | COVID19+PNEUMONIA+NORMAL Chest X-Ray Image Dataset                                              |
| **🔗 Source**           | https://www.kaggle.com/datasets/sachinkumar1999/covid19pneumonianormal-chest-xray-image-dataset |
| **🫁 Target Organ**     | Lungs / Chest                                                                                   |
| **📅 Last Accessed**    | August 13, 2026                                                                                 |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                                                                   |
| **📐 Image Size**       | 256 × 256 pixels (preprocessed)                                                                 |
| **📁 Data Format**      | PNG (.png)                                                                                      |
| **👥 Demographics**     | ❌ Not included                                                                                  |
| **🔄 Train/Test Split** | ❌ Not provided (3 subfolders: COVID, NORMAL, PNEUMONIA)                                         |

#### 📊 Dataset Composition

| Category                | Details                                                                           |
|-------------------------|-----------------------------------------------------------------------------------|
| **🖼️ Total Images**    | 5,228 files                                                                       |
| **🏥 Imaging Modality** | Radiographic X-ray (Frontal chest views)                                          |
| **📦 Total Size**       | ~289.93 MB                                                                        |
| **🏥 Source**           | Aggregated from Eurorad, Radiopaedia, Coronacases, and Mooney's Pneumonia dataset |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of pulmonary conditions
- **Number of Classes**: 3️⃣
    - 🦠 COVID-19 (1,626 images)
    - ✅ NORMAL (1,802 images)
    - 🫁 PNEUMONIA (1,800 images)

#### 💡 Usage Notes

- ✅ Preprocessed and uniformly resized to 256x256 resolution, simplifying the preprocessing pipeline for standard CNN
  architectures.
- ✅ Well-balanced class distribution (~1,600–1,800 images per class) supports stable training without aggressive
  resampling.
- ✅ Useful for benchmarking models tasked with differentiating between viral (COVID-19), bacterial/other (Pneumonia),
  and healthy states.
- 📚 Required to cite the original Kaggle repository and the associated CheXImageNet/LiteCovidNet publications.
- 🔐 License: Data files © Original Authors (Verify specific terms for each constituent source).

#### ⚠️ Usage Considerations

| Aspect                      | Recommendation                                                                                                                                   |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| **📦 Data Provenance**      | Aggregated from multiple sources with varying acquisition protocols; consider domain adaptation techniques.                                      |
| **🔐 Licensing Compliance** | Ensure downstream use respects the licenses of all original constituent datasets (e.g., Radiopaedia, Eurorad).                                   |
| **🧪 Clinical Translation** | Model performance on this curated, pre-resized dataset may not directly translate to real-world screening; validate on prospective, raw cohorts. |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Utilize framework-native utilities to ingest the `COVID`, `NORMAL`, and `PNEUMONIA`
   subfolders.
2. **Standardize input format**: Confirm uniform 256×256 dimensions; convert to single-channel grayscale if desired to
   reduce computational load.
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
4. **Augmentation**: Incorporate rotation, flipping, and mild intensity jittering to improve model generalization.
5. **Stratified evaluation**: Report per-class precision, recall, F1-score, and AUC-ROC, alongside a confusion matrix to
   analyze misclassification patterns between Pneumonia and COVID-19.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{shastri2022cheximagenet,
  title = {CheXImageNet: a novel architecture for accurate classification of Covid-19 with chest x-ray digital images using deep convolutional neural networks},
  author = {Shastri, S. and Kansal, I. and Kumar, S. and others},
  journal = {Health and Technology},
  volume = {12},
  pages = {193--204},
  year = {2022},
  doi = {10.1007/s12553-021-00630-x}
}
```

---

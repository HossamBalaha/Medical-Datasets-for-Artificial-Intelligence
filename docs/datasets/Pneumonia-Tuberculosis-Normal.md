### 🫁 Pneumonia Tuberculosis Normal

**Study**: Mahanty, R. (2024). Pneumonia Tuberculosis Normal. Kaggle.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                     |
|-------------------------|-----------------------------------------------------------------------------|
| **📛 Title**            | Pneumonia Tuberculosis Normal                                               |
| **🔗 Source**           | https://www.kaggle.com/datasets/rupeshmahanty/pneumonia-tuberculosis-normal |
| **🫁 Target Organ**     | Lungs / Chest                                                               |
| **📅 Last Accessed**    | August 13, 2026                                                             |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                                               |
| **📐 Image Size**       | Variable                                                                    |
| **📁 Data Format**      | JPEG/PNG (.jpg/.png)                                                        |
| **👥 Demographics**     | ❌ Not included                                                              |
| **🔄 Train/Test Split** | ✅ Yes (Train and Test directories provided)                                 |

#### 📊 Dataset Composition

| Category                | Details                                         |
|-------------------------|-------------------------------------------------|
| **🖼️ Total Images**    | 2,213 files                                     |
| **🏥 Imaging Modality** | Radiographic X-ray (Frontal chest views)        |
| **📦 Total Size**       | ~598.06 MB                                      |
| **🏥 Source**           | Aggregated from public chest X-ray repositories |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of pulmonary conditions
- **Number of Classes**: 3️⃣
    - 🫁 Pneumonia
    - 🦠 Tuberculosis (TB)
    - ✅ Normal

#### 💡 Usage Notes

- ✅ Useful for differential diagnosis between bacterial pneumonia, TB, and healthy lungs.
- ✅ Pre-organized into `Train` and `Test` directories for immediate integration with standard data loaders.
- 📚 Recommended to cite the original Kaggle repository.
- 🔐 License: CC0: Public Domain

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                               |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**     | Verify the exact distribution in the Train/Test folders; apply class weighting if one class dominates.                       |
| **📐 Resolution Variance** | Original scans vary in dimensions; apply uniform resizing (e.g., 224x224) prior to training.                                 |
| **🧪 Validation Strategy** | Use the provided split for reproducible benchmarking, but consider stratified k-fold cross-validation for robust evaluation. |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Utilize framework-native utilities (e.g., `torchvision.datasets.ImageFolder`) to ingest
   labeled subfolders.
2. **Standardize input format**: Convert all images to a consistent color space (single-channel grayscale) and fixed
   resolution.
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
4. **Augmentation**: Incorporate rotation, flipping, and intensity jittering to improve model generalization.
5. **Stratified evaluation**: Report per-class metrics (precision, recall, F1-score, AUC-ROC) to assess performance
   given potential class imbalances.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{mahanty2024pneumoniatb,
  author = {Mahanty, Rupesh},
  title = {Pneumonia Tuberculosis Normal},
  year = {2024},
  publisher = {Kaggle},
  url = {https://www.kaggle.com/datasets/rupeshmahanty/pneumonia-tuberculosis-normal}
}
```

---

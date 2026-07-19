### 🫀 Breast Carcinoma Histological Images (Agios Pavlos Hospital)

**Study**: Zioga, C., Kamas, A., Patsiaoura, K., Dimitropoulos, K., Barmpoutis, P., & Grammalidis, N. (2017). Breast
carcinoma histological images from the Department of Pathology, "Agios Pavlos" General Hospital of Thessaloniki,
Greece [Data set]. Zenodo.
[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                      |
|-------------------------|--------------------------------------------------------------|
| **📛 Title**            | Breast Carcinoma Histological Images (Agios Pavlos Hospital) |
| **🔗 Source**           | https://zenodo.org/records/834910                            |
| **🫀 Target Organ**     | Breast                                                       |
| **📅 Last Accessed**    | July 03, 2026                                                |
| **🎯 Supported Tasks**  | 🏷️ Ordinal Classification (Tumor Grading)                   |
| **📐 Image Size**       | 1280 × 960 pixels                                            |
| **📁 Data Format**      | Image files (ZIP)                                            |
| **👥 Demographics**     | 21 patients                                                  |
| **🔄 Train/Test Split** | ❌ Not provided                                               |

#### 📊 Dataset Composition

| Category                  | Details                                                 |
|---------------------------|---------------------------------------------------------|
| **🖼️ Total Images**      | 300 annotated histological images                       |
| **🔬 Imaging Modality**   | Brightfield histopathology (H&E stained)                |
| **🏥 Source Institution** | "Agios Pavlos" General Hospital of Thessaloniki, Greece |
| **📦 Total Size**         | ~373.8 MB (compressed)                                  |

#### 🏷️ Classification Task Details

- **Task Type**: Ordinal multiclass classification of invasive ductal carcinoma grading
- **Number of Classes**: 3️⃣ (Ordered severity scale)
- 🟢 Grade 1 (Well differentiated)
- 🟡 Grade 2 (Moderately differentiated)
- 🔴 Grade 3 (Poorly differentiated)

#### 💡 Usage Notes

- ✅ Suitable for benchmarking traditional ML and CNN architectures for breast cancer grading
- ✅ Images are grouped into folders corresponding to grades 1-3
- ✅ Relatively small dataset size (300 images) ideal for few-shot learning, transfer learning, or data augmentation
  studies
- 📚 Required to cite the original Zenodo repository and the associated PLOS ONE publication
- 🔐 Distributed under CC BY 4.0; attribution required

#### ⚠️ Usage Considerations

| Aspect                       | Recommendation                                                                                 |
|------------------------------|------------------------------------------------------------------------------------------------|
| **🔍 Small Sample Size**     | 300 images across 21 patients; employ strong regularization, augmentation, or cross-validation |
| **🧪 Ordinal Structure**     | Grades represent ordered severity; consider ordinal regression or monotonic constraints        |
| **📐 Resolution Handling**   | Images are 1280x960; resize to model-compatible dimensions (e.g., 224x224)                     |
| **🧭 Domain Generalization** | Single-center cohort; validate on external datasets for clinical deployment                    |

#### 💡 Suggested Preprocessing Pipeline

1. **Extract archive**: Unzip the `Dataset.zip` file containing the grade-labeled folders.
2. **Standardize resolution**: Resize images to a uniform dimension (e.g., 224×224 or 512×512) while preserving aspect
   ratio.
3. **Color normalization**: Apply stain normalization (e.g., Macenko method) to mitigate inter-slide H&E variability.
4. **Augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering.
5. **Cross-validation**: Use k-fold cross-validation due to the small dataset size.
6. **Evaluation metrics**: Report per-class precision/recall, weighted kappa for ordinal agreement, and macro-averaged
   F1-score.

#### 🔗 Associated Resources

- **Zenodo Repository**: https://zenodo.org/records/834910
- **Related Publication**: Dimitropoulos, K., et al. "Grading of invasive breast carcinoma through Grassmannian VLAD
  encoding." *PLOS ONE* (2017).

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{zioga2017breast,
  author = {Zioga, Christina and Kamas, Athanasios and Patsiaoura, Kalliopi and Dimitropoulos, Kosmas and Barmpoutis, Panagiotis and Grammalidis, Nikos},
  title = {Breast carcinoma histological images from the Department of Pathology, "Agios Pavlos" General Hospital of Thessaloniki, Greece},
  year = {2017},
  publisher = {Zenodo},
  doi = {10.5281/zenodo.834910},
  url = {https://doi.org/10.5281/zenodo.834910}
}
```

---


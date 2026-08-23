### 🫁 Chest X-Ray Images (Pneumonia)

**Study**: Kermany, D. S., Zhang, K., & Goldbaum, M. (2018). Large Scale Dataset of Normal and Pneumonia Chest X-Rays
for Automated Disease Detection. *Cell*, 172(5), 1122-1131.e9.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                |
|-------------------------|------------------------------------------------------------------------|
| **📛 Title**            | Chest X-Ray Images (Pneumonia)                                         |
| **🔗 Source**           | https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia |
| **🫁 Target Organ**     | Lungs / Chest                                                          |
| **📅 Last Accessed**    | August 21, 2026                                                        |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification                                              |
| **📐 Image Size**       | Variable (anterior-posterior pediatric chest X-rays)                   |
| **📁 Data Format**      | JPEG (.jpeg)                                                           |
| **👥 Demographics**     | ✅ Pediatric patients (1 to 5 years old)                                |
| **🔄 Train/Test Split** | ✅ Yes (Train, Test, Val directories provided)                          |

#### 📊 Dataset Composition

| Category                  | Details                                                  |
|---------------------------|----------------------------------------------------------|
| **🖼️ Total Images**      | 5,863 chest X-ray images                                 |
| **🏥 Imaging Modality**   | Radiographic X-ray (Anterior-Posterior)                  |
| **🎨 Color Format**       | Grayscale                                                |
| **📦 Total Size**         | ~1.24 GB                                                 |
| **🏥 Source Institution** | Guangzhou Women and Children’s Medical Center, Guangzhou |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification of pediatric chest X-rays
- **Number of Classes**: 2️⃣
    - 🫁 Pneumonia (Bacterial or Viral)
    - ✅ Normal (Clear lungs without abnormal opacification)

#### 💡 Usage Notes

- ✅ One of the most widely cited benchmark datasets for automated pneumonia detection from chest X-rays.
- ✅ Images were rigorously screened for quality and graded by two expert physicians, with a third expert verifying the
  evaluation set to minimize grading errors.
- ✅ Pre-organized into `train`, `test`, and `val` directories for immediate integration with standard deep learning data
  loaders.
- 📚 Required to cite the original *Cell* publication when using this dataset in publications.
- 🔐 License: CC BY 4.0

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                                             |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Pediatric Focus**     | Dataset consists exclusively of pediatric patients (1-5 years); models may not generalize well to adult anatomy without domain adaptation. |
| **📐 Resolution Variance** | Original scans vary in dimensions; apply uniform resizing (e.g., 224x224 or 256x256) prior to training.                                    |
| **🧪 Validation Strategy** | Utilize the provided `val` set for hyperparameter tuning and the `test` set for final, unbiased performance evaluation.                    |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Utilize framework-native utilities (e.g., `torchvision.datasets.ImageFolder`) to ingest
   the labeled subfolders.
2. **Standardize input format**: Convert all images to a consistent color space (single-channel grayscale) and fixed
   resolution.
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
4. **Augmentation **(training only): Incorporate rotation, flipping, and mild intensity jittering to improve model
   generalization and robustness to patient positioning.
5. **Stratified evaluation**: Report per-class metrics (precision, recall, F1-score, AUC-ROC) to comprehensively assess
   diagnostic performance.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{kermany2018large,
  title={Large scale dataset of normal and pneumonia chest X-rays for automated disease detection},
  author={Kermany, Daniel S and Zhang, Kang and Goldbaum, Michael},
  journal={Cell},
  volume={172},
  number={5},
  pages={1122--1131},
  year={2018},
  publisher={Elsevier},
  doi={10.1016/j.cell.2018.02.010}
}
```

---

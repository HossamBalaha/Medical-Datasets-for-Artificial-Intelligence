### 👁️ Ocular Disease Recognition (ODIR-5K)

**Study**: Larxel. (2020). Ocular Disease Recognition. Kaggle.
[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                     |
|-------------------------|-----------------------------------------------------------------------------|
| **📛 Title**            | Ocular Disease Recognition (ODIR-5K)                                        |
| **🔗 Source**           | https://www.kaggle.com/datasets/andrewmvd/ocular-disease-recognition-odir5k |
| **👁️ Target Organ**    | Eye (Retina / Fundus)                                                       |
| **📅 Last Accessed**    | June 30, 2026                                                               |
| **🎯 Supported Tasks**  | 🏷️ Multiclass / Multi-label Classification                                 |
| **📐 Image Size**       | Variable (varied camera resolutions)                                        |
| **📁 Data Format**      | JPEG/PNG (images), CSV (metadata/labels)                                    |
| **👥 Demographics**     | ✅ Age, Sex (Male 54%, Female 46%)                                           |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                      |

#### 📊 Dataset Composition

| Category                  | Details                                                             |
|---------------------------|---------------------------------------------------------------------|
| **🖼️ Total Images**      | 10,000 color fundus photographs (5,000 patients, left & right eyes) |
| **🏥 Imaging Modality**   | Color fundus photography                                            |
| **🎨 Color Format**       | RGB                                                                 |
| **📦 Total Size**         | ~2.03 GB (compressed)                                               |
| **🏥 Source Institution** | Shanggong Medical Technology Co., Ltd. (various hospitals in China) |

#### 🏷️ Classification Task Details

- **Task Type**: Multi-label classification of ocular diseases
- **Number of Classes**: 8️⃣
- ✅ Normal (N)
- 🍬 Diabetes (D)
- 👁️ Glaucoma (G)
- 🌫️ Cataract (C)
- 🟡 Age related Macular Degeneration (A)
- 🩸 Hypertension (H)
- 🔍 Pathological Myopia (M)
- ⚠️ Other diseases/abnormalities (O)

#### 💡 Usage Notes

- ✅ Suitable for benchmarking multi-label classification models for ocular disease screening
- ✅ Includes both left and right eye images for potential bilateral analysis
- ✅ Contains real-world diagnostic keywords from doctors
- 📚 Required to cite the original Kaggle repository when using this dataset
- 🔐 License was not specified on source; verify terms for commercial use

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                    |
|----------------------------|-----------------------------------------------------------------------------------|
| **🔍 Multi-label Nature**  | Patients can have multiple conditions; use appropriate loss functions (e.g., BCE) |
| **📐 Resolution Variance** | Images captured by various cameras (Canon, Zeiss, Kowa); standardize dimensions   |
| **🧪 Data Leakage**        | Split by patient ID, not by image, to prevent leakage between train/test sets     |
| **🔐 Licensing**           | License not explicitly specified; contact authors or assume non-commercial use    |

#### 💡 Suggested Preprocessing Pipeline

1. **Load metadata**: Parse `full_df.csv` to map image paths to the 8 diagnostic labels.
2. **Standardize input format**: Convert all images to a consistent color space and fixed resolution (e.g., 224x224).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide statistics.
4. **Augmentation **(training only): Incorporate rotation, flipping, and color jittering to improve generalization.
5. **Stratified evaluation**: Report per-class AUC-ROC, sensitivity, and specificity to assess multi-label performance.

#### 🔗 Associated Resources

- **Kaggle Repository**: https://www.kaggle.com/datasets/andrewmvd/ocular-disease-recognition-odir5k
- **Related Datasets
  **: [IDRiD](#-idrid-diabetic-retinopathy-grading-indian-dataset), [EyePACS](#-eyepacs-aptos-messidor-diabetic-retinopathy-unified-dataset)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{larxel2020odir,
  title={Ocular Disease Recognition},
  author={Larxel},
  year={2020},
  publisher={Kaggle},
  url={https://www.kaggle.com/datasets/andrewmvd/ocular-disease-recognition-odir5k}
}
```

---


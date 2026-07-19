### 👁️🫁 Labeled Optical Coherence Tomography (OCT) and Chest X-Ray Images for Classification

**Study**: Kermany, D. S., Goldbaum, M., Cai, W., Cordeiro, N. M., Baxter, J. S., et al. (2018). Identifying Medical
Diagnoses and Treatable Diseases by Image-Based Deep Learning. *Cell*, 172(5), 1122-1131.e9.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                              |
|-------------------------|--------------------------------------------------------------------------------------|
| **📛 Title**            | Labeled Optical Coherence Tomography (OCT) and Chest X-Ray Images for Classification |
| **🔗 Source**           | https://data.mendeley.com/datasets/rscbjbr9sj/2                                      |
| **👁️🫁 Target Organ**  | Eye (Retina) / Lungs (Chest)                                                         |
| **📅 Last Accessed**    | June 24, 2026                                                                        |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                                                        |
| **📐 Image Size**       | Variable (OCT and Chest X-rays)                                                      |
| **📁 Data Format**      | Images in directories                                                                |
| **👥 Demographics**     | ❌ Not included (independent patients)                                                |
| **🔄 Train/Test Split** | ✅ Yes (Training and testing sets of independent patients)                            |

#### 📊 Dataset Composition

| Category                  | Details                                                                  |
|---------------------------|--------------------------------------------------------------------------|
| **🖼️ Total Images**      | ~108,000 OCT images + Chest X-rays (exact X-ray count varies by version) |
| **🏥 Imaging Modality**   | Optical Coherence Tomography (OCT) / Radiographic X-ray                  |
| **🎨 Color Format**       | Grayscale / RGB (scan-dependent)                                         |
| **🏥 Source Institution** | University of California San Diego                                       |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of retinal diseases (OCT) and chest conditions (X-ray)
- **Number of Classes **(OCT): 4️⃣
- 🩸 CNV (Choroidal Neovascularization)
- 💧 DME (Diabetic Macular Edema)
- 🟡 DRUSEN
- ✅ NORMAL
- **Number of Classes **(X-Ray): 2️⃣ (Normal vs. Pneumonia)

**📊 Dataset Distribution **(OCT)

| Split       | Image Count  | Purpose                                             |
|-------------|--------------|-----------------------------------------------------|
| 🟢 Training | ~100,000     | Model training and development                      |
| 🔴 Testing  | ~8,000       | Final performance evaluation (independent patients) |
| **Total**   | **~108,000** | —                                                   |

#### 💡 Usage Notes

- ✅ Benchmark dataset for multi-disease image-based deep learning classification
- ✅ Patient-independent train/test splits ensure rigorous evaluation without data leakage
- ✅ Supports research on multi-modal or multi-organ diagnostic AI systems
- 📚 Required to cite the original *Cell* publication and Mendeley Data repository when using this dataset
- 🔐 Distributed via Mendeley Data; verify usage terms for clinical deployment

#### ⚠️ Usage Considerations

| Aspect                    | Recommendation                                                                                                    |
|---------------------------|-------------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**    | Verify per-class distribution; apply class-weighted loss or stratified sampling if needed                         |
| **📦 Data Organization**  | Images are organized by disease label; ensure proper directory parsing for framework-native loaders               |
| **🧪 Multi-Organ Focus**  | Dataset contains both OCT and X-ray images; separate preprocessing pipelines may be required for each modality    |
| **🔐 Ethical Compliance** | Dataset contains de-identified clinical imagery; adhere to institutional review requirements for derivative works |

#### 💡 Suggested Preprocessing Pipeline

1. **Separate modalities**: Isolate OCT and Chest X-ray directories to apply modality-specific preprocessing.
2. **Standardize input format**: Convert all images to a consistent color space and fixed resolution (e.g., 224x224 or
   256x256).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
4. **Augmentation **(training only): Incorporate rotation, flipping, and intensity jittering to improve model
   generalization.
5. **Stratified evaluation**: Report per-class metrics (precision, recall, F1-score) to assess performance across
   different disease categories.

#### 🔗 Associated Resources

- **Mendeley Data Repository**: https://data.mendeley.com/datasets/rscbjbr9sj/2
- **Related Publications**: Kermany et al., "Identifying Medical Diagnoses and Treatable Diseases by Image-Based Deep
  Learning," *Cell*, 2018.
- **Institutional Affiliation**: University of California San Diego

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{kermany2018labeled,
  author={Kermany, Daniel and Zhang, Kang and Goldbaum, Michael},
  title={Labeled Optical Coherence Tomography {(OCT)} and Chest {X-Ray} Images for Classification},
  year={2018},
  publisher={Mendeley Data},
  version={2},
  doi={10.17632/rscbjbr9sj.2}
}
```

---


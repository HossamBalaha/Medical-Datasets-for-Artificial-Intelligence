### 👁️ OCTDL: Retinal OCT Images Dataset

**Study**: Kulyabin, M., Zhdanov, A., Nikiforova, A., Stepichev, A., Kuznetsova, A., Ronkin, M., Borisov, V., Bogachev,
A., Korotkich, S., Constable, P. A., & Maier, A. (2023). OCTDL: Optical Coherence Tomography Dataset for Image-Based
Deep Learning Methods. *arXiv preprint arXiv:2312.08255*.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                     |
|-------------------------|-----------------------------------------------------------------------------|
| **📛 Title**            | OCTDL: Retinal OCT Images Dataset                                           |
| **🔗 Source**           | https://www.kaggle.com/datasets/shakilrana/octdl-retinal-oct-images-dataset |
| **👁️ Target Organ**    | Eye (Retina)                                                                |
| **📅 Last Accessed**    | October 03, 2026                                                            |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                                               |
| **📐 Image Size**       | Variable (includes width/height metadata)                                   |
| **📁 Data Format**      | Images + CSV metadata file                                                  |
| **👥 Demographics**     | ✅ Patient ID, Eye, Sex, Year included in metadata                           |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                      |

#### 📊 Dataset Composition

| Category                | Details                                       |
|-------------------------|-----------------------------------------------|
| **🖼️ Total Images**    | 2,064 OCT images                              |
| **🔬 Imaging Modality** | Optical Coherence Tomography (OCT)            |
| **📦 Total Size**       | ~407.3 MB                                     |
| **🏥 Source**           | Curated for image-based deep learning methods |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of retinal pathologies
- **Number of Classes**: 7️⃣
    - 🟡 Age-Related Macular Degeneration (AMD) - 1,231 images
    - 💧 Diabetic Macular Edema (DME) - 147 images
    - 🕸️ Epiretinal Membrane (ERM) - 155 images
    - ✅ Normal - 332 images
    - 🩸 Retinal Artery Occlusion (RAO) - 22 images
    - 🩸 Retinal Vein Occlusion (RVO) - 101 images
    - 👁️ Vitreomacular Interface Disease (VMID) - 76 images

#### 💡 Usage Notes

- ✅ Provides a diverse set of labeled OCT images beyond the standard 4-class datasets.
- ✅ Includes rich CSV metadata (patient_id, eye, sex, year, dimensions) for advanced demographic bias analysis.
- ✅ Valuable for developing algorithms for early diagnosis and monitoring of various ocular conditions.
- 📚 Required to cite the original arXiv publication when using this dataset.
- 🔐 License: Verify specific terms on Kaggle; typically for research use.

#### ⚠️ Usage Considerations

| Aspect                        | Recommendation                                                                                |
|-------------------------------|-----------------------------------------------------------------------------------------------|
| **🔍 Severe Class Imbalance** | AMD heavily dominates; apply class-weighted loss, focal loss, or oversampling.                |
| **📐 Resolution Variance**    | Images vary in dimensions; standardize to fixed dimensions (e.g., 224×224) prior to training. |
| **🧪 Data Leakage**           | Split by `patient_id` (not by image) to prevent leakage between train/test sets.              |

#### 💡 Suggested Preprocessing Pipeline

1. **Parse metadata**: Load `OCTDL_labels.csv` to map image filenames to diagnostic labels and patient IDs.
2. **Patient-aware splitting**: Partition data by patient ID to ensure no patient appears in both train and test sets.
3. **Standardize geometry**: Resize images to uniform dimensions while preserving aspect ratio.
4. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide statistics.
5. **Augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering.
6. **Stratified evaluation**: Report per-class precision, recall, F1-score, and macro-averaged metrics to account for
   imbalance.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@misc{kulyabin2023octdl,
    title = {OCTDL: Optical Coherence Tomography Dataset for Image-Based Deep Learning Methods},
    author = {Kulyabin, Mikhail and Zhdanov, Aleksei and Nikiforova, Anastasia and Stepichev, Andrey and Kuznetsova, Anna and Ronkin, Mikhail and Borisov, Vasilii and Bogachev, Alexander and Korotkich, Sergey and Constable, Paul A and Maier, Andreas},
    year = {2023},
    eprint = {2312.08255},
    archivePrefix = {arXiv},
    primaryClass = {eess.IV}
}
```

---

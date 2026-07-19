### 🔬 DeepHisto: Dataset for Glioma Subtype Classification from Whole Slide Images

**Study**: Mittelbronn, M., Hau, A.-C., Kim, S.-Y., Nazarov, P. V., Despotovic, V., Kakoichankava, A., Borgmann, F. B.
K., & Klamminger, G. G. (2023). DeepHisto: Dataset for glioma subtype classification from Whole Slide Images (
0.1) [Data set]. Zenodo.

[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                              |
|-------------------------|--------------------------------------------------------------------------------------|
| **📛 Title**            | DeepHisto: Dataset for glioma subtype classification from Whole Slide Images         |
| **🔗 Source**           | https://doi.org/10.5281/zenodo.7941080                                               |
| **🧠 Target Organ**     | Brain                                                                                |
| **📅 Last Accessed**    | May 08, 2026                                                                         |
| **🎯 Supported Tasks**  | 🏷️ Classification                                                                   |
| **📐 Image Size**       | 512 × 512 pixels (tile patches)                                                      |
| **📁 Data Format**      | Image tiles extracted from Whole Slide Images (format unspecified; typical: JPG/PNG) |
| **👥 Demographics**     | ❌ Not included (de-identified archival samples; N=28 patients)                       |
| **🔄 Train/Test Split** | ✅ Yes (patient-wise partitioning)                                                    |

#### 📊 Dataset Composition

| Category                 | Details                                                                         |
|--------------------------|---------------------------------------------------------------------------------|
| **🖼️ Total Tiles**      | 42,718 tiles extracted from 28 adult-type diffuse glioma cases                  |
| **🔬 Imaging Modality**  | Brightfield histopathology (Hematoxylin & Eosin stain)                          |
| **🔍 Scanner**           | IntelliSite Ultra Fast digital slide scanner (Philips), 20x/0.75 NA Plan Apo    |
| **📏 Resolution**        | 0.25 µm/pixel (average slide resolution)                                        |
| **📦 File Structure**    | train.zip (~19.2 GB), test.zip (~2.1 GB), readme.txt (1.5 kB)                   |
| **🏥 Source**            | National Center of Pathology (NCP), Luxembourg National Health Laboratory (LNS) |
| **📅 Collection Period** | 2017–2021                                                                       |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of diffuse glioma subtypes per WHO CNS5 classification
- **Number of Classes**: 5️⃣ (4 tumor entities + necrosis; normal brain as control)
    - 🟤 IDH-mutant astrocytoma
    - 🔴 IDH-wildtype glioblastoma
    - 🟣 IDH-mutant, 1p/19q codeleted oligodendroglioma
    - ⚪ Normal brain tissue (white and gray matter controls)
    - ⚫ Necrosis (annotated regions)

**📊 Tile Distribution by Class and Split**:

| Class                | Train Tiles | Test Tiles | Total Tiles |
|----------------------|-------------|------------|-------------|
| 🟤 Astrocytoma       | 3,755       | 465        | 4,220       |
| 🔴 Glioblastoma      | 1,633       | 241        | 1,874       |
| 🟣 Oligodendroglioma | 3,384       | 431        | 3,815       |
| ⚪ Normal Brain       | 29,383      | 2,947      | 32,330      |
| ⚫ Necrosis           | 389         | 90         | 479         |
| **Total**            | **38,544**  | **4,174**  | **42,718**  |

> **ℹ️ Note**: Tile counts reflect patient-wise partitioning to prevent data leakage. Normal brain tissue tiles
> constitute the majority class; consider class-weighted loss functions or stratified sampling during training.

**📋 Annotation Protocol**:

- Region annotation performed by board-certified pathologists
- Regions of interest divided into square 512×512 pixel tiles
- Each tile associated with a class label denoting tumor entity, normal tissue, or necrosis
- Patient-wise split into training and test subsets to ensure subject-level independence

#### 💡 Usage Notes

- ✅ Suitable for benchmarking deep learning models for histopathological glioma classification
- ✅ High-resolution WSI tiles (0.25 µm/pixel) enable fine-grained morphological analysis
- ✅ Patient-wise train/test split ensures robust evaluation without subject-level data leakage
- ✅ WHO CNS5-aligned classification supports clinically relevant subtype prediction
- ✅ Explicit necrosis class enables research on tumor microenvironment and tissue viability
- 📚 Required to cite the original Zenodo repository (DOI: 10.5281/zenodo.7941080) in publications
- 🔐 Distributed under CC BY 4.0; attribution required for redistribution or adaptation

#### ⚠️ Usage Considerations

| Aspect                       | Recommendation                                                                                                        |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**       | Normal brain tiles dominate (~75%); apply class-weighted loss or oversampling for minority classes                    |
| **🎨 Stain Variability**     | Apply stain normalization (e.g., Macenko method) to mitigate inter-slide variation                                    |
| **🧪 Patch-Level vs. WSI**   | Tiles are extracted patches; whole-slide inference requires aggregation strategies                                    |
| **🔐 Ethical Compliance**    | Dataset contains anonymized human tissue; adhere to institutional review requirements                                 |
| **🧭 Domain Generalization** | Single-center Luxembourg cohort; validate on external cohorts for clinical deployment                                 |
| **⚠️ Necrosis Handling**     | Necrosis class is sparse (~1%); consider treating as auxiliary task or excluding if not relevant to research question |

#### 💡 Suggested Preprocessing Pipeline

1. **Extract archives**: Unzip `train.zip` and `test.zip` into structured directories by split.
2. **Organize by label**: Arrange tiles into class-labeled subfolders for framework-native data loading.
3. **Standardize resolution**: Confirm uniform 512×512 pixel dimensions; resize if preprocessing pipelines require fixed
   input sizes.
4. **Color normalization**: Apply stain normalization (e.g., Macenko or Vahadane methods) to reduce inter-slide color
   variability.
5. **Class-aware augmentation **(training only): Incorporate rotation, flipping, and mild intensity jittering; apply
   stronger augmentation to minority classes (glioblastoma, necrosis) to improve generalization.
6. **Patient-aware validation**: Maintain patient-wise separation during cross-validation to prevent data leakage.
7. **Evaluation metrics**: Report per-subtype precision, recall, F1-score, and confusion matrices; compute
   macro-averaged metrics to account for class imbalance.

#### 🔗 Associated Resources

- **Zenodo Repository**: https://doi.org/10.5281/zenodo.7941080
- **WHO Classification Reference**: WHO Classification of Tumours Editorial Board. Central Nervous System Tumours. 5th
  ed. Vol 6. Lyon (France): International Agency for Research on Cancer; 2021.
- **Funding Acknowledgment**: This work was supported by the Luxembourg National Research Fund (FNR) grants
  C21/BM/15739125/DIOMEDES and PEARL P16/BM/11192868.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{mittelbronn2023deephisto,
    author = {Mittelbronn, Michel and Hau, Ann-Christin and Kim, Sang-Yoon and Nazarov, Petr V. and Despotovic, Vladimir and Kakoichankava, Aliaksandra and Borgmann, Felix Bruno Kleine and Klamminger, Gilbert Georg},
    title = {DeepHisto: Dataset for glioma subtype classification from Whole Slide Images},
    year = {2023},
    publisher = {Zenodo},
    version = {0.1},
    doi = {10.5281/zenodo.7941080},
    url = {https://doi.org/10.5281/zenodo.7941080}
}
```

---


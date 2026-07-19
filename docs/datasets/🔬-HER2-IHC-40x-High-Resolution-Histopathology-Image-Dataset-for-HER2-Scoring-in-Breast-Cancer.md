### 🔬 HER2-IHC-40x: High-Resolution Histopathology Image Dataset for HER2 Scoring in Breast Cancer

**Study**: Nabi, M. S., Fauzi, M. F. A., Rehman, Z. U., Karim, H. B. A., Cheah, P. L., Chiew, S. F., & Looi, L. M. (
2025). HER2-IHC-40x: A High-Resolution Histopathology Dataset for HER2 IHC Scoring in Breast Cancer. *Data in Brief*,

111922.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                                      |
|-------------------------|----------------------------------------------------------------------------------------------|
| **📛 Title**            | HER2-IHC-40x: High-Resolution Histopathology Image Dataset for HER2 Scoring in Breast Cancer |
| **🔗 Source**           | https://doi.org/10.5281/zenodo.15179608                                                      |
| **🫀 Target Organ**     | Breast                                                                                       |
| **📅 Last Accessed**    | May 08, 2026                                                                                 |
| **🎯 Supported Tasks**  | 🏷️ Ordinal Classification (HER2 IHC Scoring)                                                |
| **📐 Image Size**       | 1024 × 1024 pixels (fixed patch size)                                                        |
| **📁 Data Format**      | PNG/JPEG patches extracted from Whole Slide Images (.svs); ROI masks in PNG                  |
| **👥 Demographics**     | ❌ Not included (de-identified archival samples; N=107 patients)                              |
| **🔄 Train/Test Split** | ✅ Yes (80/20 split; two variants: WSI-level and patch-level partitioning)                    |

#### 📊 Dataset Composition

| Category                  | Details                                                                                |
|---------------------------|----------------------------------------------------------------------------------------|
| **🖼️ Total Patches**     | Variant 1: 9,940 patches; Variant 2: 10,997 patches                                    |
| **🔬 Imaging Modality**   | Brightfield immunohistochemistry (HER2-stained FFPE tissue sections)                   |
| **🔍 Magnification**      | 40× objective (high-resolution)                                                        |
| **📦 File Structure**     | Two ZIP archives: `her2-ihc-40x-patch.zip` (~1.7 GB), `her2-ihc-40x-wsi.zip` (~1.5 GB) |
| **🏥 Source Institution** | Multimedia University, Malaysia; collaborating clinical centers                        |
| **👨‍⚕️ Annotation**      | Expert pathologist-annotated ROIs using Cytomine platform                              |

#### 🏷️ Classification Task Details

- **Task Type**: Ordinal multiclass classification of HER2 immunohistochemistry (IHC) scoring per ASCO/CAP guidelines
- **Number of Classes**: 4️⃣ (ordered severity scale)

| HER2 Score | Description                                              | Clinical Interpretation               |
|------------|----------------------------------------------------------|---------------------------------------|
| 🔘 0       | No observable staining                                   | Negative                              |
| 🟡 1+      | Weak/incomplete membrane staining in ≤10% of tumor cells | Negative                              |
| 🟠 2+      | Moderate circumferential staining in >10% of tumor cells | Equivocal (requires ISH confirmation) |
| 🔴 3+      | Strong circumferential staining in >10% of tumor cells   | Positive                              |

**📊 Dataset Variants & Statistics**:

**Variant 1: HER2-IHC-40x **(WSI-Level Split)
> Whole-slide images partitioned 80/20 *before* patch extraction to prevent patient-level data leakage.

| HER2 Class | WSIs    | ROIs      | Train Patches | Test Patches | Total Patches |
|------------|---------|-----------|---------------|--------------|---------------|
| 🔘 0       | 23      | 429       | 3,031         | 758          | 3,789         |
| 🟡 1+      | 26      | 131       | 1,722         | 431          | 2,153         |
| 🟠 2+      | 27      | 483       | 507           | 127          | 634           |
| 🔴 3+      | 31      | 156       | 2,691         | 673          | 3,364         |
| **Total**  | **107** | **1,199** | **7,951**     | **1,989**    | **9,940**     |

**Variant 2: HER2-IHC-40x-WSI **(Patch-Level Split)
> Patches extracted first, then partitioned 80/20 *after* extraction (higher patch count due to expanded ROI coverage).

| HER2 Class | WSIs    | ROIs      | Train Patches | Test Patches | Total Patches |
|------------|---------|-----------|---------------|--------------|---------------|
| 🔘 0       | 23      | 429       | 3,031         | 758          | 3,789         |
| 🟡 1+      | 26      | 131       | 2,151         | 538          | 2,689         |
| 🟠 2+      | 27      | 483       | 905           | 226          | 1,131         |
| 🔴 3+      | 31      | 156       | 2,710         | 678          | 3,388         |
| **Total**  | **107** | **1,199** | **8,797**     | **2,200**    | **10,997**    |

> **ℹ️ Note**: Class 2+ (Equivocal) is underrepresented (~6–10% of patches). Consider ordinal regression, class-weighted
> loss, or focal loss to address imbalance. Variant 1 (WSI-level split) is recommended for rigorous generalization
> evaluation.

#### 🔧 Preprocessing & Quality Control Protocol

1. **ROI Selection**: Manual tumor region annotation by board-certified pathologists using Cytomine.
2. **Color Histogram Filtering**: HSV-based filtering to exclude non-tumor tissue, background, and low-quality patches.
3. **Intensity Normalization**: Global intensity normalization applied across all patches to reduce staining
   variability.
4. **Patch Extraction**: Adaptive sliding-window extraction of 1024×1024 pixel patches from annotated ROIs.
5. **Quality Assurance**: Expert review of sampled patches to verify label consistency and image quality.

#### 💡 Usage Notes

- ✅ Suitable for benchmarking deep learning models for HER2 IHC scoring automation
- ✅ High-resolution 40× patches (1024×1024) enable fine-grained membrane staining pattern analysis
- ✅ Two split strategies support research on data leakage prevention and generalization robustness
- ✅ Ordinal class structure enables investigation of monotonic loss functions and ordinal regression architectures
- ✅ Includes original WSIs (.svs) and ROI masks for reproducible patch regeneration
- 📚 Required to cite the original *Data in Brief* publication and Zenodo repository in derivative works
- 🔐 Distributed under CC BY-SA 4.0; attribution and share-alike conditions apply for redistribution

#### ⚠️ Usage Considerations

| Aspect                       | Recommendation                                                                                                                      |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**       | Class 2+ is sparse; apply class-weighted cross-entropy, focal loss, or oversampling                                                 |
| **📊 Ordinal Structure**     | Classes represent ordered severity; consider ordinal regression or monotonic constraints                                            |
| **🧪 Split Strategy**        | Prefer Variant 1 (WSI-level split) for patient-independent evaluation; Variant 2 may inflate performance due to patch-level leakage |
| **🎨 Stain Variability**     | Apply additional stain normalization (e.g., Macenko) if integrating external cohorts                                                |
| **🔐 Ethical Compliance**    | Dataset contains de-identified human tissue; adhere to institutional review requirements                                            |
| **🧭 Domain Generalization** | Single-region sourcing (Malaysia); validate on geographically diverse cohorts before clinical deployment                            |

#### 💡 Suggested Preprocessing Pipeline

1. **Select variant**: Choose Variant 1 (`her2-ihc-40x-patch.zip`) for rigorous evaluation; Variant 2 for maximum patch
   availability.
2. **Organize directory structure**: Arrange patches into class-labeled subfolders within `Train/` and `Test/`
   directories.
3. **Standardize input**: Confirm uniform 1024×1024 dimensions; resize if model architecture requires smaller inputs (
   e.g., 512×512).
4. **Color normalization**: Apply stain normalization (e.g., Macenko or Vahadane) to mitigate inter-slide IHC staining
   variability.
5. **Ordinal-aware augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering;
   preserve membrane staining integrity.
6. **Stratified mini-batching**: Ensure each training batch contains samples from all four HER2 classes to stabilize
   ordinal learning.
7. **Evaluation metrics**: Report per-class precision/recall, weighted kappa for ordinal agreement, and macro-averaged
   F1-score; include confusion matrices to assess 2+ misclassification patterns.

#### 🔗 Associated Resources

- **Zenodo Repository**: https://doi.org/10.5281/zenodo.15179608
- **Preprocessing Code**: https://github.com/seraju77/HER2-IHC-40x-data-preprocessing
- **Related Publications**:
    - Nabi et al. (2025). "Explainable deep learning models for HER2 IHC scoring in breast cancer diagnosis."
      *Informatics in Medicine Unlocked*, 101700.
    - Wolff et al. (2018). "Human Epidermal Growth Factor Receptor 2 Testing in Breast Cancer: ASCO/CAP Guideline
      Update." *Journal of Clinical Oncology*.
- **Related Datasets**:
    - [BACH](https://bach.grand-challenge.org/) (Breast cancer histology classification)
    - [BreakHis](https://web.inf.ufpr.br/vri/databases/breast-cancer-histological-images/) (Breast tumor microscopy
      images)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{nabi2025her2,
    title = {HER2-IHC-40x: A High-Resolution Histopathology Dataset for HER2 IHC Scoring in Breast Cancer},
    author = {Nabi, Md Serajun and Fauzi, Mohammad Faizal Ahmad and Rehman, Zaka Ur and Karim, Hezerul Bin Abdul and Cheah, Phaik Leng and Chiew, Seow Fan and Looi, Lai Meng},
    journal = {Data in Brief},
    pages = {111922},
    year = {2025},
    publisher = {Elsevier},
    doi = {10.1016/j.dib.2025.111922}
}

@dataset{nabi2025her2zenodo,
    author = {Nabi, Md Serajun and Fauzi, Mohammad Faizal Ahmad and Karim, Hezerul Bin Abdul and Cheah, Phaik Leng and Chiew, Seow Fan and Looi, Lai Meng and Multimedia University},
    title = {HER2-IHC-40x: High-Resolution Histopathology Image Dataset for HER2 Scoring in Breast Cancer},
    year = {2025},
    publisher = {Zenodo},
    version = {v1},
    doi = {10.5281/zenodo.15179608},
    url = {https://doi.org/10.5281/zenodo.15179608}
}
```

---


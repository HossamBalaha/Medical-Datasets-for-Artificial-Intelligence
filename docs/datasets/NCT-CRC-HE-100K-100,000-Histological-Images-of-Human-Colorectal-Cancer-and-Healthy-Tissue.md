### 🔬 NCT-CRC-HE-100K: 100,000 Histological Images of Human Colorectal Cancer and Healthy Tissue

**Study**: Kather, J. N., Halama, N., & Marx, A. (2024). 100,000 histological images of human colorectal cancer and
healthy tissue, April 2018. URL https://doi.org/10.5281/zenodo.1214456.

[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                            |
|-------------------------|--------------------------------------------------------------------|
| **📛 Title**            | NCT-CRC-HE-100K: Colorectal Cancer Histology Patches               |
| **🔗 Source**           | https://doi.org/10.5281/zenodo.1214456                             |
| **🦴 Target Organ**     | Colorectal / Colon                                                 |
| **📅 Last Accessed**    | April 11, 2026                                                     |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification, 🔍 Content-Based Retrieval          |
| **📐 Image Size**       | 224 × 224 pixels @ 0.5 µm/pixel (fixed)                            |
| **📁 Data Format**      | JPEG (.jpg), color-normalized (Macenko method) or raw              |
| **👥 Demographics**     | ❌ Not included (anonymized archival samples; N=136 patients total) |
| **🔄 Train/Test Split** | ✅ Yes (100K training patches + 7K validation patches)              |

#### 📊 Dataset Composition

| Category                   | Details                                                                                                                                                                       |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **🖼️ Total Images**       | 107,180 histopathological image patches                                                                                                                                       |
| **🔬 Imaging Modality**    | Brightfield histopathology (H&E-stained FFPE tissue sections)                                                                                                                 |
| **📦 Variants**            | • `NCT-CRC-HE-100K.zip`: Color-normalized (11.7 GB)<br>• `NCT-CRC-HE-100K-NONORM.zip`: Raw staining (11.7 GB)<br>• `CRC-VAL-HE-7K.zip`: Independent validation set (800.3 MB) |
| **🏥 Source Institutions** | National Center for Tumor Diseases (NCT), Heidelberg; University Medical Center Mannheim (UMM), Germany                                                                       |
| **📅 Collection Period**   | Archival samples; ethics approval renewed December 2017                                                                                                                       |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass tissue-type classification
- **Number of Classes**: 9️⃣

| Class Code | Full Name                            | Description                                    |
|------------|--------------------------------------|------------------------------------------------|
| ADI        | Adipose tissue                       | Fat cells                                      |
| BACK       | Background                           | Empty / non-tissue regions                     |
| DEB        | Debris                               | Necrotic or fragmented tissue                  |
| LYM        | Lymphocytes                          | Immune cell infiltrates                        |
| MUC        | Mucus                                | Extracellular mucin pools                      |
| MUS        | Smooth muscle                        | Muscularis propria or muscularis mucosae       |
| NORM       | Normal colon mucosa                  | Non-neoplastic glandular epithelium            |
| STR        | Cancer-associated stroma             | Desmoplastic reaction / tumor microenvironment |
| TUM        | Colorectal adenocarcinoma epithelium | Malignant glandular structures                 |

**📊 Dataset Distribution**:

| Split                      | Image Count | Patient Count | Purpose                            |
|----------------------------|-------------|---------------|------------------------------------|
| Training (NCT-CRC-HE-100K) | 100,000     | 86            | Model development                  |
| Validation (CRC-VAL-HE-7K) | 7,180       | 50            | Hyperparameter tuning / evaluation |
| **Total**                  | **107,180** | **136**       | —                                  |

> ⚠️ **Note**: Classes are only roughly balanced. Evaluation based solely on overall accuracy is discouraged; report
> per-class metrics and consider stratified sampling.

#### 💡 Usage Notes

- ✅ Benchmark dataset for tissue-type recognition in computational histopathology
- ✅ Pre-extracted, fixed-size patches enable direct integration with standard CNN architectures
- ✅ Color-normalized and non-normalized variants support research on stain invariance
- ✅ Independent validation set (CRC-VAL-HE-7K) enables reproducible benchmarking without data leakage
- 📚 Cite the Zenodo repository (DOI: 10.5281/zenodo.1214456) and associated publications when using this dataset
- 🔐 Distributed under CC BY 4.0; attribution required for redistribution or adaptation

#### ⚠️ Usage Considerations

| Aspect                             | Recommendation                                                                                             |
|------------------------------------|------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**             | Verify per-class distribution; apply class-weighted loss or stratified sampling if needed                  |
| **🎨 Stain Variability**           | Use color-normalized variant for reduced domain shift; or explicitly model staining as a covariate         |
| **🧪 Patch-Level vs. Slide-Level** | Patches are non-overlapping tiles; whole-slide inference requires aggregation strategies                   |
| **🔐 Ethical Compliance**          | Dataset contains anonymized human tissue; adhere to institutional review requirements for derivative works |
| **🧭 Domain Generalization**       | Sourced from two German centers; validate on external cohorts for clinical deployment                      |

#### 💡 Suggested Preprocessing Pipeline

1. **Select variant**: Choose color-normalized (`NCT-CRC-HE-100K.zip`) for reduced stain variability, or raw (`NONORM`)
   for domain adaptation research.
2. **Organize directory structure**: Arrange images by class label for compatibility with framework-native loaders (
   e.g., `torchvision.datasets.ImageFolder`).
3. **Load validation set separately**: Keep `CRC-VAL-HE-7K.zip` isolated to prevent accidental training contamination.
4. **Apply augmentations **(training only): Incorporate rotation, flipping, and mild intensity jittering; avoid
   geometric distortions that alter tissue architecture.
5. **Normalization**: Scale pixel values to [0, 1] or standardize using ImageNet statistics if using pretrained
   backbones.
6. **Stratified evaluation**: Report per-class precision, recall, F1-score, and confusion matrices; compute
   macro-averaged metrics to account for class imbalance.
7. **Aggregation **(optional): For slide-level prediction, implement majority voting, attention-based pooling, or
   multiple-instance learning over patch predictions.

#### 🔗 Associated Resources

- **Primary Publication**: Kather et al., "Predicting survival from colorectal cancer histology slides using deep
  learning: A retrospective multicenter study," *PLOS Medicine*,
    2019. [DOI](https://doi.org/10.1371/journal.pmed.1002730)
- **Color Normalization Reference**: Macenko et al., "A method for normalizing histology slides for quantitative
  analysis," *ISBI*, 2009. [DOI](https://doi.org/10.1109/ISBI.2009.5193250)
- **GitHub Implementations**: Multiple open-source repositories implement benchmarks on this dataset; search "
  NCT-CRC-HE-100K" on GitHub for reference code.
- **Related Datasets**:
    - [CRC-HGD-v1](https://data.mendeley.com/datasets/yfp5sfj47m/2) (grading-focused)
    - [HunCRC](https://doi.org/10.1038/s41597-022-01450-y) (Hungarian colorectal cancer dataset)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{kather2018nctcrc,
    author = {Kather, Jakob Nikolas and Halama, Niels and Marx, Alexander},
    title = {100,000 histological images of human colorectal cancer and healthy tissue},
    year = {2018},
    publisher = {Zenodo},
    version = {v0.1},
    doi = {10.5281/zenodo.1214456},
    url = {https://doi.org/10.5281/zenodo.1214456}
}

@article{kather2019plosmed,
    title = {Predicting survival from colorectal cancer histology slides using deep learning: A retrospective multicenter study},
    author = {Kather, Jakob Nikolas and Krisam, Johannes and Charoentong, Pornpimol and Luedde, Tom and Herpel, Esther and Weis, Cleo-Aron and Gaiser, Timo and Marx, Alexander and Valous, Nektarios A and Ferber, Dyke and others},
    journal = {PLOS Medicine},
    volume = {16},
    number = {1},
    pages = {e1002730},
    year = {2019},
    publisher = {Public Library of Science San Francisco, CA USA},
    doi = {10.1371/journal.pmed.1002730}
}
```

---


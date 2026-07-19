### 🔬 CRC_DX: MSI vs. MSS Classification in Gastrointestinal Cancer

**Study**: Kather, J. N. (2019). Histological images for MSI vs. MSS classification in gastrointestinal cancer, FFPE
samples [Data set]. Zenodo.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                                     |
|-------------------------|---------------------------------------------------------------------------------------------|
| **📛 Title**            | Histological images for MSI vs. MSS classification in gastrointestinal cancer, FFPE samples |
| **🔗 Source**           | https://doi.org/10.5281/zenodo.2530835                                                      |
| **🦴 Target Organ**     | Colorectal / Gastric (Gastrointestinal)                                                     |
| **📅 Last Accessed**    | May 08, 2026                                                                                |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification (Microsatellite Status Prediction)                                |
| **📐 Image Size**       | 224 × 224 pixels @ 0.5 µm/pixel (fixed, color-normalized)                                   |
| **📁 Data Format**      | Image patches (format unspecified; typical: JPG/PNG), Macenko-normalized                    |
| **👥 Demographics**     | ❌ Not included (TCGA cohort; de-identified archival FFPE samples)                           |
| **🔄 Train/Test Split** | ✅ Yes (patient-wise ~70/30 split; training sets equilibrated by undersampling)              |

#### 📊 Dataset Composition

| Category                 | Details                                                                                          |
|--------------------------|--------------------------------------------------------------------------------------------------|
| **🖼️ Total Patches**    | 411,890 unique histopathological image patches                                                   |
| **🔬 Imaging Modality**  | Brightfield histopathology (H&E-stained FFPE tissue sections)                                    |
| **🌐 Source Cohort**     | The Cancer Genome Atlas (TCGA): Colorectal adenocarcinoma (COAD) + Stomach adenocarcinoma (STAD) |
| **🎨 Preprocessing**     | Tumor detection → 224×224 px @ 0.5 µm/px → Macenko color normalization                           |
| **📦 File Structure**    | 8 ZIP archives (~47.1 GB total); separated by cancer type, split, and class                      |
| **📅 Collection Period** | Archival TCGA samples; published February 2019                                                   |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification of microsatellite status in gastrointestinal cancer
- **Number of Classes**: 2️⃣

| Class Label | Description                                                       | Clinical Significance                                 |
|-------------|-------------------------------------------------------------------|-------------------------------------------------------|
| 🔴 MSS      | Microsatellite Stable: intact DNA mismatch repair system          | Standard chemotherapy indications                     |
| 🔵 MSIMUT   | Microsatellite Instable / Hypermutated: defective mismatch repair | Predicts immunotherapy response (e.g., pembrolizumab) |

**📊 Patch Distribution by Cancer Type and Split**:

**Gastric Cancer **(STAD)
| Split | Class | Patch Count | Notes |
|--------|---------|-------------|------------------------------------|
| Train | MSS | 50,285 | Equilibrated to match MSIMUT count |
| Train | MSIMUT | 50,285 | Equilibrated baseline |
| Test | MSS | 90,104 | Full test distribution |
| Test | MSIMUT | 27,904 | Reflects natural class imbalance |
| **STAD Total** | — | **218,578** | ~53.1% of dataset |

**Colorectal Cancer **(CRC_DX)
| Split | Class | Patch Count | Notes |
|--------|---------|-------------|------------------------------------|
| Train | MSS | 46,704 | Equilibrated to match MSIMUT count |
| Train | MSIMUT | 46,704 | Equilibrated baseline |
| Test | MSS | 70,569 | Full test distribution |
| Test | MSIMUT | 29,335 | Reflects natural class imbalance |
| **CRC_DX Total** | — | **193,312** | ~46.9% of dataset |

**📈 Overall Class Distribution**:
| Class | Total Patches | % of Dataset | Train (Equilibrated) | Test (Natural) |
|---------|---------------|--------------|---------------------|----------------|
| 🔴 MSS | 257,662 | ~62.6% | 96,989 (50%)        | 160,673 |
| 🔵 MSIMUT | 154,228 | ~37.4% | 96,989 (50%)        | 57,239 |
| **Total** | **411,890** | **100%**     | **193,978**         | **217,912**    |

> **ℹ️ Note**: Training sets were equilibrated via random undersampling of the majority MSS class to enable balanced
> model training. Test sets preserve natural class distribution for realistic performance evaluation. Patient-wise
> splitting prevents data leakage across train/test boundaries.

#### 🔧 Preprocessing Protocol (Applied by Authors)

1. **Tumor Region Detection**: Automated algorithm identifies tumor-containing regions in whole-slide images.
2. **Patch Extraction**: Sliding-window extraction of 224×224 pixel patches at 0.5 µm/pixel resolution.
3. **Color Normalization**: Macenko method applied to reduce inter-slide staining variability.
4. **Patient-Level Splitting**: ~70% of patients assigned to training, ~30% to testing (no patient overlap).
5. **Training Set Equilibration**: MSS class undersampled to match MSIMUT count within training sets.
6. **Quality Control**: Patches derived from diagnostic FFPE slides ("DX" at GDC portal); low-quality regions excluded.

#### 💡 Usage Notes

- ✅ Benchmark dataset for MSI status prediction from H&E histopathology in GI cancers
- ✅ Preprocessed, fixed-size, color-normalized patches enable direct integration with standard CNN architectures
- ✅ Patient-wise splitting supports rigorous evaluation of generalization to unseen patients
- ✅ Includes both colorectal and gastric cancer cohorts for cross-cancer generalization studies
- ✅ Parent dataset for the curated "MSI-MSS Strong Patches" subset (Zenodo: 10.5281/zenodo.3692380)
- 📚 Required to cite the original Zenodo repository and associated publications in derivative works
- 🔐 Distributed under CC BY 4.0; attribution required for redistribution or adaptation

#### ⚠️ Usage Considerations

| Aspect                            | Recommendation                                                                                                                |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance **(Test)     | Test sets reflect natural MSI prevalence (~37% MSIMUT); report balanced metrics (AUC, F1) alongside accuracy                  |
| **🧪 Cross-Cancer Analysis**      | STAD (gastric) and CRC_DX (colorectal) have distinct histomorphology; evaluate domain shift explicitly                        |
| **🎨 Stain Normalization**        | Macenko normalization already applied; additional normalization may be redundant unless integrating external data             |
| **🔐 Ethical Compliance**         | Derived from TCGA; adhere to TCGA data use agreements and institutional review requirements                                   |
| **🧭 Clinical Translation**       | MSI prediction from H&E remains investigational; validate against PCR/NGS molecular ground truth                              |
| **📦 Patch-to-Slide Aggregation** | Patches are tile-level; whole-slide or patient-level inference requires aggregation strategies (e.g., MIL, attention pooling) |

#### 💡 Suggested Preprocessing Pipeline

1. **Extract archives**: Unzip the 8 ZIP files into structured directories by cancer type, split, and class.
2. **Verify integrity**: Confirm patch counts match documentation; check for corrupted files.
3. **Standardize loading**: Use framework-native utilities (e.g., `torchvision.datasets.ImageFolder`) for class-labeled
   directories.
4. **Augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering; preserve glandular
   architecture.
5. **Stratified batching**: Leverage equilibrated training sets for stable binary classification; monitor per-class
   metrics.
6. **Cross-validation**: Implement patient-aware folds if re-splitting; maintain no patient overlap between folds.
7. **Evaluation metrics**: Report AUC-ROC, sensitivity, specificity, F1-score, and confusion matrices; include cancer
   type-stratified results.

#### 🔗 Associated Resources

- **Zenodo Repository**: https://doi.org/10.5281/zenodo.2530835
- **TCGA Data Portal**: https://portal.gdc.cancer.gov/ (original SVS whole-slide images)
- **Preprocessing Reference**: Macenko et al. (2009). "A method for normalizing histology slides for quantitative
  analysis." *ISBI*. [DOI](https://doi.org/10.1109/ISBI.2009.5193250)
- **FFPE Download Guide**: http://www.andrewjanowczyk.com/download-tcga-digital-pathology-images-ffpe/
- **Related Publications**:
    - Kather et al. (2019). "Pan-cancer image-based detection of clinically actionable genetic alterations." *Nature
      Cancer*.
    - Echle et al. (2021). "Clinical-grade detection of microsatellite instability in colorectal tumors by deep
      learning." *Gastroenterology*.
- **Related Datasets**:
    - [MSI-MSS Strong Patches](#-msi-mss-strong-patches-microsatellite-status-classification) (curated subset)
    - [NCT-CRC-HE-100K](#-nct-crc-he-100k-100000-histological-images-of-human-colorectal-cancer-and-healthy-tissue) (
      tissue-type classification)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{kather2019msimss,
    author = {Kather, Jakob Nikolas},
    title = {Histological images for MSI vs. MSS classification in gastrointestinal cancer, FFPE samples},
    year = {2019},
    publisher = {Zenodo},
    version = {v1},
    doi = {10.5281/zenodo.2530835},
    url = {https://doi.org/10.5281/zenodo.2530835}
}

@article{kather2020pan,
    title = {Pan-cancer image-based detection of clinically actionable genetic alterations},
    author = {Kather, Jakob Nikolas and Heij, Lara R and Grabsch, Heike I and Loeffler, Chiara and Echle, Amelie and Muti, Hannah Sophie and Krause, Jeremias and Niehues, Jan M and Sommer, Kai AJ and Bankhead, Peter and others},
    journal = {Nature cancer},
    volume = {1},
    number = {8},
    pages = {789--799},
    year = {2020},
    publisher = {Nature Publishing Group US New York},
    doi = {10.1038/s43018-020-0087-4}
}
```

---


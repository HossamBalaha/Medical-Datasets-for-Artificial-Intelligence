### 🔬 MSI-MSS Strong Patches: Microsatellite Status Classification

**Study**: Shen, Y. (2020). Strong histopathological relevance patches for MSI vs. MSS classification (Version

1) [Data set]. Zenodo.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                            |
|-------------------------|------------------------------------------------------------------------------------|
| **📛 Title**            | Strong histopathological relevance patches for MSI vs. MSS classification          |
| **🔗 Source**           | https://doi.org/10.5281/zenodo.3692380                                             |
| **🦴 Target Organ**     | Colorectal / Gastrointestinal                                                      |
| **📅 Last Accessed**    | May 08, 2026                                                                       |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification (Microsatellite Instability Detection)                   |
| **📐 Image Size**       | Variable (histopathological patches; standardization recommended)                  |
| **📁 Data Format**      | Image patches extracted from H&E-stained FFPE tissue sections (format unspecified) |
| **👥 Demographics**     | ❌ Not included (de-identified archival samples)                                    |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                             |

#### 📊 Dataset Composition

| Category                 | Details                                                                            |
|--------------------------|------------------------------------------------------------------------------------|
| **🖼️ Total Patches**    | 55,453 histopathological image patches                                             |
| **🔬 Imaging Modality**  | Brightfield histopathology (Hematoxylin & Eosin stain, FFPE tissue sections)       |
| **🎯 Selection Method**  | Neural network-based fused distillation + expert pathologist morphology validation |
| **📦 File Structure**    | Two ZIP archives: `MSIMUT_strong.zip` (~3.2 GB), `MSS_strong.zip` (~3.1 GB)        |
| **🏥 Source**            | Subset of CRC_DX dataset (Zenodo: 10.5281/zenodo.2530835)                          |
| **📅 Collection Period** | Archival FFPE samples; published February 2020                                     |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification of microsatellite status in colorectal/gastrointestinal cancer
- **Number of Classes**: 2️⃣

| Class Label      | Description                                                                   | Clinical Significance                                                          |
|------------------|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| 🔵 MSIMUT_strong | Patches with strong histopathological relevance to microsatellite instability | Associated with defective DNA mismatch repair; predicts immunotherapy response |
| 🔴 MSS_strong    | Patches with strong histopathological relevance to microsatellite stability   | Intact mismatch repair; standard chemotherapy indications                      |

**📊 Patch Distribution**:

| Class            | Patch Count | % of Dataset |
|------------------|-------------|--------------|
| 🔵 MSIMUT_strong | 28,307      | ~51.0%       |
| 🔴 MSS_strong    | 27,146      | ~49.0%       |
| **Total**        | **55,453**  | **100%**     |

> **ℹ️ Note**: This dataset represents a curated subset of the parent CRC_DX collection, filtered via neural network
> distillation and pathologist expert review to retain only patches with strong morphological relevance to MSI/MSS
> classification. This enhances signal-to-noise ratio for model training but may limit generalizability to unfiltered
> histological regions.

#### 🔧 Curation & Quality Control Protocol

1. **Parent Dataset**: Derived from "Histological images for MSI vs. MSS classification in gastrointestinal cancer, FFPE
   samples" (CRC_DX).
2. **Neural Network Filtering**: Fused distillation framework votes on candidate patches for histopathological
   relevance.
3. **Expert Validation**: Board-certified pathologists incorporate morphology knowledge to select most representative
   samples.
4. **Label Assignment**: Patches tagged as MSIMUT_strong or MSS_strong based on consensus molecular status and visual
   relevance.
5. **Quality Assurance**: Final subset optimized for high-confidence model training on MSI prediction tasks.

#### 💡 Usage Notes

- ✅ Suitable for benchmarking deep learning models for microsatellite instability prediction from histopathology
- ✅ Curated "strong relevance" patches reduce background noise, enabling focused feature learning on discriminative
  morphological patterns
- ✅ Near-balanced class distribution (~51/49) supports stable binary classification training without aggressive
  resampling
- ✅ Serves as a high-quality subset for transfer learning or fine-tuning from the broader CRC_DX dataset
- 📚 Required to cite both this Zenodo repository and the parent CRC_DX dataset (DOI: 10.5281/zenodo.2530835) in
  derivative works
- 🔐 Distributed under CC BY 4.0; attribution required for redistribution or adaptation

#### ⚠️ Usage Considerations

| Aspect                      | Recommendation                                                                                                              |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **🔍 Subset Limitation**    | Curated for "strong relevance"; models trained here may not generalize to unfiltered WSIs without domain adaptation         |
| **🧪 Split Strategy**       | No predefined split; implement patient-aware or slide-aware partitioning to prevent data leakage                            |
| **🎨 Stain Variability**    | Apply stain normalization (e.g., Macenko method) if integrating with external cohorts                                       |
| **🔐 Ethical Compliance**   | Dataset contains de-identified human tissue; adhere to institutional review requirements                                    |
| **🧭 Clinical Translation** | MSI status prediction from H&E alone remains investigational; validate against molecular ground truth in clinical pipelines |
| **📦 Patch-Level Focus**    | Patches are extracted regions; whole-slide inference requires aggregation or multiple-instance learning strategies          |

#### 💡 Suggested Preprocessing Pipeline

1. **Extract archives**: Unzip `MSIMUT_strong.zip` and `MSS_strong.zip` into class-labeled directories.
2. **Standardize geometry**: Resize patches to uniform dimensions (e.g., 224×224 or 512×512) while preserving aspect
   ratio.
3. **Color normalization**: Apply stain normalization to mitigate inter-slide H&E staining variability.
4. **Stratified splitting**: Partition data by source slide or patient ID (if metadata available) to ensure no leakage
   between train/test sets.
5. **Augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering; preserve
   morphological integrity of glandular and stromal features.
6. **Class-balanced batching**: Leverage near-balanced distribution for stable training; monitor per-class metrics
   during validation.
7. **Evaluation metrics**: Report accuracy, sensitivity, specificity, AUC-ROC, and F1-score; include confusion matrices
   to assess MSI/MSS discrimination patterns.

#### 🔗 Associated Resources

- **Zenodo Repository**: https://doi.org/10.5281/zenodo.3692380
- **Parent Dataset **(CRC_DX): https://doi.org/10.5281/zenodo.2530835
- **Related Publications**:
    - Shen, Y. et al. (2020). "Histological images for MSI vs. MSS classification in gastrointestinal cancer, FFPE
      samples." Zenodo.
    - Relevant literature on MSI prediction from histopathology: e.g., Kather et al., *Nature Medicine* (2019); Echle et
      al., *Cancer Cell* (2021).
- **Related Datasets**:
    - [NCT-CRC-HE-100K](#-nct-crc-he-100k-100000-histological-images-of-human-colorectal-cancer-and-healthy-tissue) (
      tissue-type classification)
    - [CRC-HGD-v1](#-crc-hgd-v1-colorectal-cancer-histopathological-grading-dataset) (grading-focused)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{shen2020msimss,
    author = {Shen, Yiqing},
    title = {Strong histopathological relevance patches for MSI vs. MSS classification},
    year = {2020},
    publisher = {Zenodo},
    version = {1},
    doi = {10.5281/zenodo.3692380},
    url = {https://doi.org/10.5281/zenodo.3692380}
}

@dataset{shen2020crcdx,
    author = {Shen, Yiqing},
    title = {Histological images for MSI vs. MSS classification in gastrointestinal cancer, FFPE samples},
    year = {2020},
    publisher = {Zenodo},
    doi = {10.5281/zenodo.2530835},
    url = {https://doi.org/10.5281/zenodo.2530835}
}
```

---


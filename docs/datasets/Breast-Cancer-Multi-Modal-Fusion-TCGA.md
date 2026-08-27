### 🎀 Breast Cancer: Multi-Modal Fusion Dataset (TCGA-BRCA)

**Study**: Eslami, S. (2026). TCGA-BRCA: Multi-Modal Fusion Dataset (MRI, Pathology, Omics & Clinical). Kaggle.  
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                                               |
|-------------------------|-------------------------------------------------------------------------------------------------------|
| **📛 Title**            | TCGA-BRCA: Multi-Modal Fusion Dataset                                                                 |
| **🔗 Source**           | https://www.kaggle.com/datasets/sepehreslamimoghadam/breast-cancer-vision-and-genomic-fusion-ml-ready |
| **🫁 Target Organ**     | Breast                                                                                                |
| **📅 Last Accessed**    | August 27, 2026                                                                                       |
| **🎯 Supported Tasks**  | 🔄 Multimodal Fusion, 📈 Survival Prediction, 🏷️ Molecular Subtyping                                 |
| **📐 Image Size**       | Variable (MRI volumes, High-res SVS pathology patches)                                                |
| **📁 Data Format**      | .csv (Omics/Clinical), .json (Mappings), Processed Image Tiles                                        |
| **👥 Demographics**     | ✅ Included (TNM staging, survival status, treatment matrix)                                           |
| **🔄 Train/Test Split** | ❌ Not provided (patient-level splitting required)                                                     |

#### 📊 Dataset Composition

| Category                | Details                                                               |
|-------------------------|-----------------------------------------------------------------------|
| **🖼️ Total Images**    | 122 strictly aligned patients (MRI + Pathology patches)               |
| **🏥 Imaging Modality** | Multimodal: MRI, Histopathology (SVS patches), RNA-Seq, CNV, Clinical |
| **📦 Total Size**       | ~20.02 GB                                                             |
| **🏥 Source**           | The Cancer Genome Atlas (TCGA-BRCA), preprocessed and aligned         |

#### 🏷️ Task Details

- **Task Type**: Multi-modal representation learning and downstream prediction
- **Target Variables**:
    - 🧬 Molecular Subtypes (e.g., Luminal A, Basal-like, HER2-enriched)
    - ⏱️ Survival Status & Time
    - 💊 Treatment Response (One-hot encoded drug matrix)

#### 💡 Usage Notes

- ✅ Solves the massive boilerplate problem of aligning TCGA WSIs, clinical XMLs, and genomic data. Ready for "
  plug-and-play" fusion networks.
- ✅ Includes a pre-merged `RNA_CNV_ModelReady.csv` for immediate tabular deep learning.
- 🔐 License: Creative Commons Attribution 4.0 International (CC BY 4.0).

#### ⚠️ Usage Considerations

| Aspect                      | Recommendation                                                                                                                                              |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Patient Leakage**      | With only 122 patients, strict patient-level splitting is mandatory. Do not split by image patch, or the model will memorize patient-specific artifacts.    |
| **📐 Modality Missingness** | Not all 122 patients may have every single modality perfectly populated. Implement masking or imputation strategies for missing genomic or clinical fields. |
| **🧪 Validation Strategy**  | Use Leave-One-Out Cross-Validation (LOOCV) or 5-fold patient-stratified CV due to the small cohort size.                                                    |

#### 💡 Suggested Preprocessing Pipeline

1. **Patient Alignment**: Use the provided `MRI_and_SVS_Patches_info.json` to map image tiles to their corresponding
   patient's genomic and clinical rows.
2. **Vision Encoding**: Pass pathology patches through a frozen, pretrained histopathology encoder (e.g., UNI, Phikon,
   or ResNet-50) to generate fixed-size embeddings.
3. **Tabular Processing**: Apply standard scaling to the `RNA_CNV_ModelReady.csv` features.
4. **Fusion Architecture**: Concatenate vision embeddings and tabular vectors, passing them through a multi-layer
   perceptron (MLP) for early/late fusion.
5. **Downstream Head**: Train a classification head for molecular subtyping or a Cox proportional hazards head for
   survival analysis.

#### 📚 Citation

If you use this dataset, please cite the curator and the original TCGA research network:

```bibtex
@dataset{eslami2026tcgabrca,
  author = {Eslami, Sepehr},
  title = {Breast Cancer : Multi-Modal Fusion Dataset (TCGA-BRCA)},
  year = {2026},
  publisher = {Kaggle},
  url = {https://www.kaggle.com/datasets/sepehreslamimoghadam/breast-cancer-vision-and-genomic-fusion-ml-ready}
}

```

---

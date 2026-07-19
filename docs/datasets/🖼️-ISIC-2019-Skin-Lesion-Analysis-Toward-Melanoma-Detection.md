### 🖼️ ISIC 2019: Skin Lesion Analysis Toward Melanoma Detection

**Study**: Tschandl, P., Rosendahl, C., & Kittler, H. (2018). The HAM10000 dataset... / Codella, N., et al. (2017)... /
Hernández-Pérez, C., et al. (2024)...

[🔝 Back to Summary](#-dataset-summary)
| Metadata | Details |
|-------------------------|-------------------------------------------------------------------------|
| **📛 Title**            | ISIC 2019: Skin Lesion Analysis Toward Melanoma Detection |
| **🔗 Source**           | https://challenge.isic-archive.com/data/#2019                           |
| **🖼️ Target Organ**    | Skin |
| **📅 Last Accessed**    | June 30, 2026 |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification |
| **📐 Image Size**       | Variable (dermoscopic and clinical images)                              |
| **📁 Data Format**      | JPEG (images), CSV (metadata/labels)                                    |
| **👥 Demographics**     | ✅ Age, Sex, Anatomical site |
| **🔄 Train/Test Split** | ✅ Yes (25,331 Training / 8,238 Test)                                    |

#### 📊 Dataset Composition

| Category                   | Details                              |
|----------------------------|--------------------------------------|
| **🖼️ Total Images**       | 33,569 skin lesion images            |
| **🏥 Imaging Modality**    | Dermoscopic and clinical photography |
| **🎨 Color Format**        | RGB                                  |
| **📦 Total Size**          | ~12.7 GB (compressed)                |
| **🏥 Source Institutions** | BCN-20000, HAM10000, MSK datasets    |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of skin lesions
- **Number of Classes**: 8️⃣
- ⚫ Melanoma (MEL)
- 🟤 Melanocytic nevus (NV)
- 🟠 Basal cell carcinoma (BCC)
- 🟡 Actinic keratosis (AK)
- 🟢 Benign keratosis (BKL)
- 🔵 Dermatofibroma (DF)
- 🔴 Vascular lesion (VASC)
- ⚪ Squamous cell carcinoma (SCC)

#### 💡 Usage Notes

- ✅ Benchmark dataset for dermoscopic image classification and melanoma detection
- ✅ Includes rich metadata (age, sex, anatomical site) for demographic bias analysis
- ✅ Pre-defined train/test splits enable reproducible benchmarking
- 📚 Required to cite the original ISIC challenge and constituent datasets (HAM10000, BCN-20000, MSK)
- 🔐 Distributed under CC-BY-NC; verify terms for commercial use

#### ⚠️ Usage Considerations

| Aspect                        | Recommendation                                                               |
|-------------------------------|------------------------------------------------------------------------------|
| **🔍 Severe Class Imbalance** | NV and BKL heavily dominate; apply class-weighted loss or focal loss         |
| **📐 Resolution Variance**    | Images vary in dimensions; standardize to fixed dimensions prior to training |
| **🧪 Metadata Integration**   | Leverage age/sex metadata to improve model fairness and generalization       |
| **🔐 Licensing**              | CC-BY-NC-ND; strictly non-commercial use without explicit permission         |

#### 💡 Suggested Preprocessing Pipeline

1. **Load metadata**: Parse CSV files to map image IDs to diagnostic labels and demographic features.
2. **Standardize input format**: Convert all images to a consistent color space and fixed resolution (e.g., 224x224).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using ImageNet statistics.
4. **Augmentation **(training only): Incorporate rotation, flipping, and color jittering; avoid aggressive distortions.
5. **Stratified evaluation**: Report per-class AUC-ROC, sensitivity, and specificity, especially for melanoma.

#### 🔗 Associated Resources

- **ISIC Archive**: https://challenge.isic-archive.com/data/#2019
- **Related Datasets**: [PAD-UFES-20](#-pad-ufes-20-skin-lesion-dataset)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{isic2019skin,
  title={ISIC 2019: Skin Lesion Analysis Toward Melanoma Detection},
  author={Tschandl, P. and Rosendahl, C. and Kittler, H. and Codella, N. and others},
  year={2019},
  publisher={ISIC Archive},
  url={https://challenge.isic-archive.com/data/#2019}
}
```

---


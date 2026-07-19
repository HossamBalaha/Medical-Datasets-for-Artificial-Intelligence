### 🔬 CRC-HGD-v1: Colorectal Cancer Histopathological Grading Dataset

**Study**: Amjadi, E., Bahreini, A., Hakimian, S. M., Emami, M. H., Fahim, A., Rahimi, H., & Bolhasani, H. (2024).
CRC-HGD-v1: A Histopathological Image Dataset for Grading Colorectal Cancer. *Mendeley Data*, V2.

[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                         |
|-------------------------|-----------------------------------------------------------------|
| **📛 Title**            | CRC-HGD-v1: Colorectal Cancer Histopathological Grading Dataset |
| **🔗 Source**           | https://data.mendeley.com/datasets/yfp5sfj47m/2                 |
| **🦴 Target Organ**     | Colorectal / Colon                                              |
| **📅 Last Accessed**    | April 11, 2026                                                  |
| **🎯 Supported Tasks**  | 🏷️ Classification (Ordinal Grading)                            |
| **📐 Image Size**       | Variable (multi-magnification: 4x, 10x, 20x, 40x)               |
| **📁 Data Format**      | Image files (format unspecified; typical: JPG/PNG)              |
| **👥 Demographics**     | ❌ Not included                                                  |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)          |

#### 📊 Dataset Composition

| Category                    | Details                                                  |
|-----------------------------|----------------------------------------------------------|
| **🖼️ Total Images**        | 1,899 histopathological images                           |
| **🔬 Imaging Modality**     | Brightfield histopathology (H&E-stained tissue sections) |
| **🔍 Magnification Levels** | 4x, 10x, 20x, 40x (multi-scale coverage)                 |
| **📦 Total Size**           | ~457 MB (compressed)                                     |
| **🏥 Curation**             | Poursina-Hakim Digestive Disease Research Center (PDDRC) |

#### 🏷️ Classification Task Details

- **Task Type**: Ordinal multiclass classification (tumor grading)
- **Number of Classes**: 3️⃣
    - 🟢 Grade I: Well Differentiated
    - 🟡 Grade II: Moderately Differentiated
    - 🔴 Grade III: Poorly Differentiated

**📊 Specimen-Level Distribution**:

| Grade     | Description               | Specimens | Images (All Magnifications) |
|-----------|---------------------------|-----------|-----------------------------|
| I         | Well Differentiated       | 103       | 860                         |
| II        | Moderately Differentiated | 75        | 712                         |
| III       | Poorly Differentiated     | 32        | 327                         |
| **Total** | —                         | **210**   | **1,899**                   |

**🔬 Multi-Magnification Sampling Protocol**:

- Per specimen: ~10 images total
    - 1 image at 4x magnification
    - 3 images at 10x magnification
    - 3 images at 20x magnification
    - 3 images at 40x magnification

#### 💡 Usage Notes

- ✅ Suitable for benchmarking ordinal classification and multi-scale learning architectures
- ✅ Multi-magnification design supports research on resolution-aware feature extraction
- ✅ Expert-curated labels under pathology supervision enhance annotation reliability
- 📚 Required to cite the original Mendeley Data repository (DOI: 10.17632/yfp5sfj47m.2) in publications
- 🔗 For dataset updates or inquiries, visit: https://databiox.com (as noted by the authors)

#### ⚠️ Usage Considerations

| Aspect                        | Recommendation                                                                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**        | Grade III (Poorly Differentiated) is underrepresented; consider stratified sampling or class-weighted loss |
| **🔬 Magnification Handling** | Images span 4x-40x; either process magnifications separately or normalize resolution prior to training     |
| **🧪 Ordinal Nature**         | Grades represent an ordered severity scale; consider ordinal regression or monotonic loss functions        |
| **🔐 Licensing**              | Verify usage terms on Mendeley Data; attribution required for redistribution                               |
| **🧭 Domain Generalization**  | Single-center curation may limit external validity; validate on independent cohorts when possible          |

#### 💡 Suggested Preprocessing Pipeline

1. **Organize directory structure**: Group images by grade and magnification level for efficient data loading.
2. **Standardize resolution**: Resize images to a uniform dimension (e.g., 224x224 or 512x512) while preserving aspect
   ratio.
3. **Color normalization**: Apply stain normalization (e.g., Macenko method) to reduce inter-slide variability.
4. **Magnification-aware augmentation**: Apply rotation, flipping, and intensity adjustments; avoid operations that
   distort histological features.
5. **Stratified splitting**: Partition data by specimen (not image) to prevent data leakage across train/test sets.
6. **Ordinal encoding**: Encode grades as ordered integers (0, 1, 2) or use one-hot vectors with ordinal constraints.
7. **Evaluation metrics**: Report per-class precision/recall alongside ordinal-aware metrics (e.g., weighted kappa, mean
   absolute error).

#### 🔗 Associated Resources

- **Dataset Homepage**: https://data.mendeley.com/datasets/yfp5sfj47m/2
- **Query Portal**: https://databiox.com (for updates and support)
- **Related Work**: Consider cross-referencing with other colorectal histopathology datasets (e.g., CRC-VAL-HE-7K,
  PatchGastricADC22)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{amjadi2024crchgd,
    author = {Amjadi, Elham and Bahreini, Amin and Hakimian, Sayyed Mohammadreza and Emami, Mohammad Hasan and Fahim, Alireza and Rahimi, Hojjatollah and Bolhasani, Hamidreza},
    title = {CRC-HGD-v1: A Histopathological Image Dataset for Grading Colorectal Cancer},
    year = {2024},
    publisher = {Mendeley Data},
    version = {2},
    doi = {10.17632/yfp5sfj47m.2},
    url = {https://data.mendeley.com/datasets/yfp5sfj47m/2}
}
```

---


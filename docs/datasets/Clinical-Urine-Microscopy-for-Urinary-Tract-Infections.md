### 🧪 Clinical Urine Microscopy for Urinary Tract Infections

**Study**: Liou, N., De, T., Urbanski, A., Khasriya, R., Yakimovich, A., & Horsley, H. (2023). Clinical urine microscopy
for urinary tract infections. RODARE.

[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)
| Metadata | Details |
|-------------------------|-------------------------------------------------------------------------|
| **📛 Title**            | Clinical Urine Microscopy for Urinary Tract Infections |
| **🔗 Source**           | https://rodare.hzdr.de/record/2473                                      |
| **🧪 Target Organ**    | Urine / Cellular |
| **📅 Last Accessed**    | June 30, 2026 |
| **🎯 Supported Tasks**  | 🎭 Semantic Segmentation (Binary & Multi-class)                         |
| **📐 Image Size**       | 1392 × 1040 pixels (fixed)                                              |
| **📁 Data Format**      | 16-bit TIFF (images and masks)                                          |
| **👥 Demographics**     | ✅ Symptomatic UTI patients |
| **🔄 Train/Test Split** | ❌ Not provided (300 images total)                                       |

#### 📊 Dataset Composition

| Category                  | Details                                   |
|---------------------------|-------------------------------------------|
| **🖼️ Total Images**      | 300 brightfield microscopy images         |
| **🏥 Imaging Modality**   | Brightfield microscopy (x20 objective)    |
| **🎨 Color Format**       | 16-bit RGB                                |
| **📦 Total Size**         | ~2.3 GB (compressed)                      |
| **🏥 Source Institution** | Specialist LUTS outpatient clinic, London |

#### 🎭 Segmentation Task Details

- **Task Type**: Binary and multi-class semantic segmentation of urinary cells
- **Number of Classes**: 7️⃣
- ⚫ Background (0)
- 🦠 Rod (1)
- 🩸 RBC/WBC (2)
- 🍄 Yeast (3)
- 🟤 Miscellaneous (4)
- 🟡 Single EPC (5)
- 🟠 Small EPC sheet (6)
- 🔴 Large EPC sheet (7)

#### 💡 Usage Notes

- ✅ First publicly available dataset for automated UTI diagnosis via urine microscopy
- ✅ Includes both binary (foreground/background) and multi-class segmentation masks
- ✅ High-resolution 16-bit TIFF images preserve fine cellular details
- 📚 Required to cite the original RODARE repository when using this dataset
- 🔐 Distributed under CC BY 4.0; attribution required for redistribution

#### ⚠️ Usage Considerations

| Aspect                        | Recommendation                                                               |
|-------------------------------|------------------------------------------------------------------------------|
| **🔍 Severe Class Imbalance** | Background dominates; EPC sheets are rare; use appropriate loss functions    |
| **📐 High Resolution**        | 1392x1040 images require substantial memory; consider patch-based processing |
| **🎨 16-bit Format**          | Ensure libraries support 16-bit TIFF loading; normalize to 8-bit if needed   |
| **🧪 Clinical Translation**   | Validate on external cohorts before clinical deployment                      |

#### 💡 Suggested Preprocessing Pipeline

1. **Load TIFF files**: Use libraries supporting 16-bit TIFF (e.g., `tifffile`, `Pillow`).
2. **Standardize resolution**: Resize or extract patches to model-compatible dimensions (e.g., 512x512).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide statistics.
4. **Augmentation **(training only): Incorporate rotation, flipping, and elastic deformations; preserve cellular
   integrity.
5. **Stratified evaluation**: Report Dice/IoU for each class, especially for rare classes like EPC sheets.

#### 🔗 Associated Resources

- **RODARE Repository**: https://rodare.hzdr.de/record/2473
- **Related Publications**: Liou, N., et al. (2023). "Clinical urine microscopy for urinary tract infections."

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{liou2023urine,
  title={Clinical urine microscopy for urinary tract infections},
  author={Liou, Natasha and De, Trina and Urbanski, Adrian and Khasriya, Rajvinder and Yakimovich, Artur and Horsley, Harry},
  year={2023},
  publisher={RODARE},
  doi={10.14278/rodare.2473},
  url={https://rodare.hzdr.de/record/2473}
}
```

---


### 🫀 CBCT Liver and Liver Tumor Segmentation (CBCTLiTS)

**Study**: Tschuchnig, M. E., Steininger, P., & Gadermayr, M. (2024). CBCTLiTS: A Synthetic, Paired CBCT/CT Dataset For
Segmentation And Style Transfer. *Eurographics Workshop on Visual Computing for Biology and Medicine*.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------|
| **📛 Title**            | CBCT Liver and Liver Tumor Segmentation Train Data (CBCTLiTS)                                           |
| **🔗 Source**           | https://www.kaggle.com/datasets/maximiliantschuchnig/cbct-liver-and-liver-tumor-segmentation-train-data |
| **🫀 Target Organ**     | Liver                                                                                                   |
| **📅 Last Accessed**    | November 10, 2026                                                                                       |
| **🎯 Supported Tasks**  | 🎭 3D Semantic Segmentation, 🔄 Style Transfer                                                          |
| **📐 Image Size**       | Variable 3D volumes (multiple resolution levels)                                                        |
| **📁 Data Format**      | NIfTI (.nii)                                                                                            |
| **👥 Demographics**     | ❌ Not included (derived from LiTS dataset)                                                             |
| **🔄 Train/Test Split** | ✅ Yes (131 Training volumes provided; 70 Test volumes in full benchmark)                               |

#### 📊 Dataset Composition

| Category                | Details                                                                          |
|-------------------------|----------------------------------------------------------------------------------|
| **🖼️ Total Volumes**    | 131 training volumes (with paired masks)                                         |
| **🏥 Imaging Modality** | Cone-Beam CT (CBCT) at 5 quality levels + Paired standard CT                     |
| **📦 Total Size**       | ~99.69 GB                                                                        |
| **🏥 Source**           | Synthetic derivation from the original Liver Tumor Segmentation (LiTS) benchmark |

#### 🎭 Segmentation Task Details

- **Task Type**: 3D multiclass semantic segmentation
- **Number of Classes**: 3️⃣
    - ⚫ Background (0)
    - 🟤 Liver (1)
    - 🔴 Liver Tumor (2)
- **Annotation Targets**: Expert-segmented masks for the entire liver volume and intra-hepatic tumors, aligned to the
  CBCT space.

#### 💡 Usage Notes

- ✅ First large-scale, paired CBCT/CT dataset for liver segmentation, addressing the scarcity of annotated CBCT data.
- ✅ Provides 5 different CBCT simulation quality levels, enabling robust research on domain adaptation and style
  transfer.
- ✅ Builds directly upon the gold-standard LiTS (Liver Tumor Segmentation) benchmark.
- 📚 Required to cite both this CBCTLiTS publication and the original LiTS dataset.
- 🔐 Distributed under CC BY-NC-ND 4.0 (Non-commercial, no derivatives).

#### ⚠️ Usage Considerations

| Aspect                  | Recommendation                                                                                                                   |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| **📦 Large File Sizes** | ~100 GB dataset; ensure adequate storage and use efficient 3D data loaders (e.g., `MONAI`).                                      |
| **🔄 Modality Shift**   | CBCT has lower soft-tissue contrast and higher noise than standard CT; models trained on CT may fail on CBCT without adaptation. |
| **🧪 Quality Levels**   | Leverage the 5 quality levels for curriculum learning or robustness testing.                                                     |

#### 💡 Suggested Preprocessing Pipeline

1. **Load 3D volumes**: Use `nibabel` or `MONAI` to read the paired `.nii` files for images and masks.
2. **Intensity normalization**: Apply CT-specific Hounsfield Unit (HU) windowing (e.g., liver window: -50 to 150 HU) and
   clip to [0, 1].
3. **Resampling**: Resample all volumes to a common isotropic voxel spacing (e.g., 1.5 × 1.5 × 1.5 mm).
4. **Spatial alignment**: Ensure the CBCT, CT, and mask volumes are perfectly spatially aligned (provided in this
   dataset).
5. **Augmentation **(training only): Apply 3D random cropping, flipping, and Gaussian noise injection (especially for
   CBCT branches).
6. **Evaluation metrics**: Report Dice Similarity Coefficient (DSC) and Normalized Surface Distance (NSD) for both liver
   and tumor classes.

#### 📚 Citation

If you use this dataset, please cite:

```
bibtex
@inproceedings{tschuchnig2024cbctlits,
  title={CBCTLiTS: A Synthetic, Paired CBCT/CT Dataset For Segmentation And Style Transfer},
  author={Tschuchnig, Maximilian Ernst and Steininger, Philipp and Gadermayr, Michael},
  booktitle={Eurographics Workshop on Visual Computing for Biology and Medicine},
  year={2024}
}
@article{bilic2023lits,
  title={The Liver Tumor Segmentation Benchmark (LiTS)},
  author={Bilic, Patrick and Christ, Patrick and Li, Hongwei Bran and others},
  journal={Medical Image Analysis},
  volume={84},
  pages={102680},
  year={2023},
  publisher={Elsevier},
  doi={10.1016/j.media.2022.102680}
}
```

---

### 🩺 ETIS-LaribPolypDB

**Study**: Silva, J., Histace, A., Romain, O., Dray, X., & Granado, B. (2014). Toward embedded detection of polyps in
WCE images for early diagnosis of colorectal cancer. *International Journal of Computer Assisted Radiology and Surgery*,
9(2), 283-293.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                             |
|-------------------------|---------------------------------------------------------------------|
| **📛 Title**            | ETIS-LaribPolypDB                                                   |
| **🔗 Source**           | https://www.kaggle.com/datasets/nguyenvoquocduong/etis-laribpolypdb |
| **🩺 Target Organ**     | Gastrointestinal Tract (Colon)                                      |
| **📅 Last Accessed**    | August 31, 2026                                                     |
| **🎯 Supported Tasks**  | 🎭 Semantic Segmentation                                            |
| **📐 Image Size**       | Variable (typically ~1000 × 1000 pixels)                            |
| **📁 Data Format**      | PNG (.png) for both original images and ground truth masks          |
| **👥 Demographics**     | ❌ Not included (de-identified clinical colonoscopy frames)          |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)              |

#### 📊 Dataset Composition

| Category                  | Details                                  |
|---------------------------|------------------------------------------|
| **🖼️ Total Images**      | 196 colonoscopy frames containing polyps |
| **🏥 Imaging Modality**   | White-light endoscopy (WLE)              |
| **📦 Total Size**         | ~185 MB (compressed)                     |
| **🏥 Source Institution** | Hôpital Lariboisière, Paris, France      |

#### 🎭 Segmentation Task Details

- **Task Type**: Binary semantic segmentation of colorectal polyps
- **Annotation Targets**: Pixel-wise mask corresponding to the polyp region.
- **Annotation Protocol**: Manually annotated by medical experts, known for containing particularly challenging polyps (
  e.g., small, flat, or low-contrast lesions).

#### 💡 Usage Notes

- ✅ Highly regarded benchmark dataset for evaluating the robustness of polyp segmentation models on difficult cases.
- ✅ Frequently used in cross-dataset evaluation protocols to test model generalization beyond easier datasets like
  Kvasir-SEG.
- 📚 Required to cite the original *International Journal of Computer Assisted Radiology and Surgery* publication when
  using this dataset.
- 🔐 License: Verify specific terms on the hosting platform; typically restricted to research and educational purposes.

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                           |
|----------------------------|----------------------------------------------------------------------------------------------------------|
| **🔍 High Difficulty**     | Contains many small or flat polyps; models may struggle without advanced attention mechanisms.           |
| **📐 Resolution Variance** | Images vary in dimensions; standardize to fixed dimensions (e.g., 256×256 or 512×512) prior to training. |
| **🧪 Domain Shift**        | Sourced from a single institution; validate on external cohorts for robustness.                          |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Ingest images and corresponding masks from their respective folders.
2. **Standardize geometry**: Resize images and masks to uniform dimensions while preserving aspect ratio.
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide statistics.
4. **Augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering; preserve polyp
   boundary integrity.
5. **Evaluation metrics**: Report Dice coefficient and Intersection over Union (IoU) as the primary segmentation
   metrics.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{silva2014toward,
  title={Toward embedded detection of polyps in WCE images for early diagnosis of colorectal cancer},
  author={Silva, J{\'e}r{\^o}me and Histace, Aymeric and Romain, Olivier and Dray, Xavier and Granado, Bertrand},
  journal={International journal of computer assisted radiology and surgery},
  volume={9},
  number={2},
  pages={283--293},
  year={2014},
  publisher={Springer},
  doi={10.1007/s11548-013-0926-3}
}
```

---

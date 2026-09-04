### 🩺 CVC-ColonDB

**Study**: Vázquez, D., Bernal, J., Sánchez, F. J., Fernández-Esparrach, G., López, A. M., Romero, A., ... & Vilariño,
F. (2017). A benchmark for endoluminal scene segmentation of colonoscopy images. *Journal of Healthcare Engineering*
,2017.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                       |
|-------------------------|---------------------------------------------------------------|
| **📛 Title**            | CVC-ColonDB                                                   |
| **🔗 Source**           | https://www.kaggle.com/datasets/hopmai/cvc-colondb            |
| **🩺 Target Organ**     | Gastrointestinal Tract (Colon)                                |
| **📅 Last Accessed**    | August 31, 2026                                               |
| **🎯 Supported Tasks**  | 🎭 Semantic Segmentation                                      |
| **📐 Image Size**       | 384 × 288 pixels (fixed)                                      |
| **📁 Data Format**      | Images and masks (format varies by mirror; typically PNG/JPG) |
| **👥 Demographics**     | ❌ Not included (de-identified clinical colonoscopy frames)    |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)        |

#### 📊 Dataset Composition

| Category                  | Details                                  |
|---------------------------|------------------------------------------|
| **🖼️ Total Images**      | 380 colonoscopy frames containing polyps |
| **🏥 Imaging Modality**   | White-light endoscopy (WLE)              |
| **📦 Total Size**         | ~191 MB (compressed)                     |
| **🏥 Source Institution** | Hospital Clinic, Barcelona, Spain        |

#### 🎭 Segmentation Task Details

- **Task Type**: Binary semantic segmentation of colorectal polyps
- **Annotation Targets**: Pixel-wise mask corresponding to the polyp region.
- **Annotation Protocol**: Manually annotated to provide a diverse benchmark for endoluminal scene segmentation,
  complementing the CVC-ClinicDB dataset.

#### 💡 Usage Notes

- ✅ Valuable for benchmarking polyp segmentation models on a distinct set of endoscopic frames.
- ✅ Often used in conjunction with CVC-ClinicDB and ETIS-LaribPolypDB for cross-dataset generalization studies.
- 📚 Recommended to cite the original *Journal of Healthcare Engineering* publication when using this dataset.
- 🔐 License: Verify specific terms on the hosting platform; typically restricted to research and educational purposes.

#### ⚠️ Usage Considerations

| Aspect                   | Recommendation                                                                  |
|--------------------------|---------------------------------------------------------------------------------|
| **🔍 Limited Diversity** | Contains only frames with polyps; lacks negative (polyp-free) examples.         |
| **📐 Resolution**        | Fixed at 384×288; modern architectures may require upsampling or padding.       |
| **🧪 Domain Shift**      | Sourced from a single institution; validate on external cohorts for robustness. |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Ingest images and corresponding masks from their respective folders.
2. **Standardize geometry**: Resize images and masks to uniform dimensions (e.g., 256×256 or 512×512) while preserving
   aspect ratio.
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide statistics.
4. **Augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering; preserve polyp
   boundary integrity.
5. **Evaluation metrics**: Report Dice coefficient and Intersection over Union (IoU) as the primary segmentation
   metrics.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{vazquez2017benchmark,
  title={A benchmark for endoluminal scene segmentation of colonoscopy images},
  author={V{\'a}zquez, David and Bernal, Jorge and S{\'a}nchez, Francisco J and Fern{\'a}ndez-Esparrach, Gloria and L{\'o}pez, Antonio M and Romero, Adriana and Drozdzal, Michal and Courville, Aaron},
  journal={Journal of healthcare engineering},
  volume={2017},
  year={2017},
  publisher={Hindawi},
  doi={10.1155/2017/4037190}
}
```

---

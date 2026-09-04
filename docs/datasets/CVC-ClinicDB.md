### 🩺 CVC-ClinicDB

**Study**: Bernal, J., Sánchez, F. J., Fernández-Esparrach, G., Gil, D., Rodríguez, C., & Vilariño, F. (2015). WM-DOVA
maps for accurate polyp highlighting in colonoscopy: Validation vs. saliency maps from physicians. *Computerized Medical
Imaging and Graphics*, 43, 99-111.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                      |
|-------------------------|--------------------------------------------------------------|
| **📛 Title**            | CVC-ClinicDB                                                 |
| **🔗 Source**           | https://polyp.grand-challenge.org/CVCClinicDB/               |
| **🩺 Target Organ**     | Gastrointestinal Tract (Colon)                               |
| **📅 Last Accessed**    | August 31, 2026                                              |
| **🎯 Supported Tasks**  | 🎭 Semantic Segmentation                                     |
| **📐 Image Size**       | 384 × 288 pixels (fixed)                                     |
| **📁 Data Format**      | TIFF (.tiff) for both original images and ground truth masks |
| **👥 Demographics**     | ❌ Not included (de-identified clinical colonoscopy frames)   |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)       |

#### 📊 Dataset Composition

| Category                  | Details                                                                               |
|---------------------------|---------------------------------------------------------------------------------------|
| **🖼️ Total Images**      | 612 colonoscopy frames containing polyps                                              |
| **🏥 Imaging Modality**   | White-light endoscopy (WLE)                                                           |
| **📦 Total Size**         | ~50 MB (compressed)                                                                   |
| **🏥 Source Institution** | Hospital Clinic, Barcelona, Spain (Images); Computer Vision Center, Barcelona (Masks) |

#### 🎭 Segmentation Task Details

- **Task Type**: Binary semantic segmentation of colorectal polyps
- **Annotation Targets**: Pixel-wise mask corresponding to the region covered by the polyp in the image.
- **Annotation Protocol**: Manually annotated and verified by medical experts to serve as the official training database
  for the MICCAI 2015 Sub-Challenge on Automatic Polyp Detection.

#### 💡 Usage Notes

- ✅ Benchmark dataset for endoscopic polyp segmentation and computer-aided diagnosis (CAD) systems.
- ✅ Provides high-quality, expert-verified ground truth masks for rigorous model evaluation.
- ✅ Widely used in academic literature, enabling direct comparison with state-of-the-art segmentation architectures.
- 📚 Required to cite the original *Computerized Medical Imaging and Graphics* publication when using this dataset.
- 🔐 License: Restricted to research and educational purposes; commercial use is forbidden without prior written
  permission.

#### ⚠️ Usage Considerations

| Aspect                   | Recommendation                                                                   |
|--------------------------|----------------------------------------------------------------------------------|
| **🔍 Limited Diversity** | Contains only frames with polyps; does not include negative (polyp-free) frames. |
| **📐 Resolution**        | Fixed at 384×288; modern architectures may require upsampling or padding.        |
| **🔐 Licensing**         | Strictly non-commercial; verify terms before any derivative work or deployment.  |

#### 💡 Suggested Preprocessing Pipeline

1. **Load TIFF files**: Use libraries supporting multi-page or high-bit-depth TIFF (e.g., `tifffile`, `Pillow`).
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
@article{bernal2015wm,
  title={WM-DOVA maps for accurate polyp highlighting in colonoscopy: Validation vs. saliency maps from physicians},
  author={Bernal, Jorge and S{\'a}nchez, Francisco J and Fern{\'a}ndez-Esparrach, Gloria and Gil, Debora and Rodr{\'\i}guez, Cristina and Vilari{\~n}o, Fernando},
  journal={Computerized medical imaging and graphics},
  volume={43},
  pages={99--111},
  year={2015},
  publisher={Elsevier},
  doi={10.1016/j.compmedimag.2015.02.007}
}
```

---

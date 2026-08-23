### 🫁 COVID-19 CT scans

**Study**: Larxel. (2020). COVID-19 CT scans. Kaggle. (Annotations by Ma Jun, et al., 2020).
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                    |
|-------------------------|------------------------------------------------------------|
| **📛 Title**            | COVID-19 CT scans                                          |
| **🔗 Source**           | https://www.kaggle.com/datasets/andrewmvd/covid19-ct-scans |
| **🫁 Target Organ**     | Lungs / Chest                                              |
| **📅 Last Accessed**    | August 21, 2026                                            |
| **🎯 Supported Tasks**  | 🎭 Semantic Segmentation, 🏷️ Classification               |
| **📐 Image Size**       | Variable (3D NIfTI volumes)                                |
| **📁 Data Format**      | NIfTI (.nii) for images and masks, CSV (metadata)          |
| **👥 Demographics**     | ❌ Not included (de-identified)                             |
| **🔄 Train/Test Split** | ❌ Not provided (20 CT scans total)                         |

#### 📊 Dataset Composition

| Category                   | Details                                            |
|----------------------------|----------------------------------------------------|
| **🖼️ Total Scans**        | 20 3D CT scans of patients diagnosed with COVID-19 |
| **🏥 Imaging Modality**    | Computed Tomography (CT)                           |
| **📦 Total Size**          | ~7.91 GB                                           |
| **🏥 Source Institutions** | Coronacases.org & Radiopaedia.org                  |

#### 🎭 Segmentation Task Details

- **Task Type**: Multi-class semantic segmentation of thoracic CT scans
- **Annotation Targets**: Expert-drawn masks for:
    1. **Lung Fields**: The entire anatomical lung region.
    2. **Infections**: Specific regions of COVID-19 manifestations (e.g., ground-glass opacities, consolidations).
    3. **Combined**: Masks containing both lung and infection segmentations.

#### 💡 Usage Notes

- ✅ High-quality, expert-annotated dataset specifically tailored for COVID-19 severity assessment and infection
  localization.
- ✅ Plays a supportive role in optimizing diagnosis and treatment, especially in regions with a shortage of expert
  radiologists.
- ✅ Provided in NIfTI format, preserving the native 3D spatial resolution and Hounsfield Unit (HU) values critical for
  medical analysis.
- 📚 Required to credit the original data sources (Coronacases, Radiopaedia) and the annotation authors (Ma Jun, et al.)
  in publications.
- 🔐 Licenses: Coronacases (CC BY-NC 3.0), Radiopaedia (CC BY-NC-SA 3.0), Annotations (CC BY 4.0).

#### ⚠️ Usage Considerations

| Aspect                      | Recommendation                                                                                                                                |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Small Sample Size**    | Only 20 scans; highly prone to overfitting. Use aggressive cross-validation, transfer learning from larger CT datasets, or data augmentation. |
| **📦 3D Data Handling**     | Requires 3D deep learning frameworks (e.g., 3D U-Net) or slice-by-slice 2D approaches with careful volume reconstruction.                     |
| **🔐 Licensing Compliance** | Strictly non-commercial use due to source licenses; verify terms before any derivative work.                                                  |

#### 💡 Suggested Preprocessing Pipeline

1. **Load NIfTI data**: Use `nibabel` or `SimpleITK` to read the 3D CT volumes and corresponding expert masks.
2. **Apply HU Windowing**: Clip Hounsfield Units to a lung/mediastinal window (e.g., -1000 to 400 HU) and normalize
   to [0, 1].
3. **Resampling**: Resample all volumes to a consistent isotropic voxel spacing (e.g., 1.0 × 1.0 × 1.0 mm) and crop/pad
   to a fixed bounding box (e.g., 128x128x128).
4. **Synchronized 3D Augmentation**: Apply 3D rotations, flips, and elastic deformations identically to the image and
   all mask channels.
5. **Evaluation metrics**: Report per-class 3D Dice coefficient and Volumetric IoU for both lung and infection
   segmentation tasks.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{larxel2020covid19ct,
  author = {Larxel},
  title = {COVID-19 CT scans},
  year = {2020},
  publisher = {Kaggle},
  url = {https://www.kaggle.com/datasets/andrewmvd/covid19-ct-scans}

}
@dataset{ma2020covid19ctseg,
  author = {Ma, Jun and Ge, Cheng and Wang, Yixin and An, Xingle and Gao, Jiantao and Yu, Ziqi and He, Jian},
  title = {COVID-19 CT Lung and Infection Segmentation Dataset},
  year = {2020},
  publisher = {Zenodo},
  doi = {10.5281/zenodo.3757476}
}
```

---

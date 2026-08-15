### 🩺 Pancreas-CT

**Study**: Roth, H., Farag, A., Turkbey, E. B., Lu, L., Liu, J., & Summers, R. M. (2016). Data From Pancreas-CT. The
Cancer Imaging Archive (TCIA).
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                      |
|-------------------------|--------------------------------------------------------------|
| **📛 Title**            | Pancreas-CT                                                  |
| **🔗 Source**           | https://www.cancerimagingarchive.net/collection/pancreas-ct/ |
| **🩺 Target Organ**     | Pancreas                                                     |
| **📅 Last Accessed**    | August 13, 2026                                              |
| **🎯 Supported Tasks**  | 🎭 Semantic Segmentation                                     |
| **📐 Image Size**       | 512 × 512 pixels (varying slice thickness: 1.5 – 2.5 mm)     |
| **📁 Data Format**      | DICOM (images), ZIP and NIfTI (manual annotations)           |
| **👥 Demographics**     | ✅ 53 Male, 27 Female (Ages 18–76, mean 46.8 ± 16.7)          |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)       |

#### 📊 Dataset Composition

| Category                | Details                                                             |
|-------------------------|---------------------------------------------------------------------|
| **🖼️ Total Images**    | 82 abdominal contrast-enhanced 3D CT scans (~18,942 slices)         |
| **🏥 Imaging Modality** | Computed Tomography (CT), portal-venous phase (~70s post-injection) |
| **📦 Total Size**       | ~9.95 GB                                                            |
| **🏥 Source**           | National Institutes of Health (NIH) Clinical Center                 |

#### 🎭 Segmentation Task Details

- **Task Type**: Binary semantic segmentation of the pancreas organ
- **Annotation Targets**: Slice-by-slice manual segmentation of the pancreas, verified and modified by an experienced
  radiologist.
- **Format**: Ground-truth masks provided in NIfTI and ZIP formats, aligned with the DICOM series.

#### 💡 Usage Notes

- ✅ Benchmark dataset for automated pancreas segmentation in abdominal CT.
- ✅ Subjects are healthy controls (kidney donors) or patients without major abdominal pathologies or pancreatic cancer
  lesions.
- ✅ High-quality, expert-verified annotations make it ideal for training robust medical segmentation models.
- 📚 Required to cite the original TCIA collection and the MICCAI 2015 DeepOrgan publication.
- 🔐 License: CC BY 3.0

#### ⚠️ Usage Considerations

| Aspect                    | Recommendation                                                                                        |
|---------------------------|-------------------------------------------------------------------------------------------------------|
| **📦 Data Format**        | Requires DICOM and NIfTI handling libraries (e.g., `pydicom`, `nibabel`, `SimpleITK`).                |
| **🧪 Domain Shift**       | Acquired on Philips and Siemens MDCT scanners; validate on external vendors to ensure generalization. |
| **📐 3D Context**         | Slice-by-slice 2D segmentation may lose volumetric context; consider 3D CNNs or 2.5D approaches.      |
| **🔐 Ethical Compliance** | Dataset contains de-identified human clinical data; adhere to institutional review requirements.      |

#### 💡 Suggested Preprocessing Pipeline

1. **Load DICOM series**: Reconstruct 3D volumes from axial slices using patient metadata and sort by slice location.
2. **Intensity windowing**: Apply abdominal soft-tissue windowing (e.g., -100 to 400 Hounsfield Units) and normalize
   to [0, 1].
3. **Resampling**: Resample volumes to isotropic voxel spacing (e.g., 1.0 × 1.0 × 1.0 mm) for consistent CNN input.
4. **Mask alignment**: Ensure the NIfTI segmentation masks are correctly registered to the resampled DICOM volumes.
5. **Augmentation**: Apply 3D elastic deformations, random cropping, and rotation to handle the small organ size
   relative to the abdomen.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{roth2016pancreasct,
  author = {Roth, H. and Farag, A. and Turkbey, E. B. and Lu, L. and Liu, J. and Summers, R. M.},
  title = {Data From Pancreas-CT (Version 2)},
  year = {2016},
  publisher = {The Cancer Imaging Archive},
  doi = {10.7937/K9/TCIA.2016.tNB1kqBU},
  url = {https://www.cancerimagingarchive.net/collection/pancreas-ct/}
}
```

---

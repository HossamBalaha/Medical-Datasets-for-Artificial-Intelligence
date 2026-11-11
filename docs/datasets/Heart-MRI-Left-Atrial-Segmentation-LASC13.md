### ❤️ Heart MRI: Left Atrial Segmentation (LASC'13)

**Study**: Tobon-Gomez, C., Geers, A. J., Peters, J., et al. (2015). Benchmark for Algorithms Segmenting the Left Atrium
From 3D CT and MRI Datasets. *IEEE Transactions on Medical Imaging*, 34(7), 1460–1473.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                                    |
|-------------------------|--------------------------------------------------------------------------------------------|
| **📛 Title**            | Heart MRI Image DataSet: Left Atrial Segmentation (LASC'13)                                |
| **🔗 Source**           | https://www.kaggle.com/datasets/adarshsng/heart-mri-image-dataset-left-atrial-segmentation |
| **❤️ Target Organ**     | Heart (Left Atrium)                                                                        |
| **📅 Last Accessed**    | November 10, 2026                                                                          |
| **🎯 Supported Tasks**  | 🎭 3D Semantic Segmentation                                                                |
| **📐 Image Size**       | Variable 3D volumes (NIfTI / MHD format)                                                   |
| **📁 Data Format**      | `.mhd` / `.raw` or `.nii` (NIfTI)                                                          |
| **👥 Demographics**     | ❌ Not included (de-identified clinical scans)                                             |
| **🔄 Train/Test Split** | ✅ Yes (10 Training, 20 Testing per modality)                                              |

#### 📊 Dataset Composition

| Category                | Details                                            |
|-------------------------|----------------------------------------------------|
| **🖼️ Total Volumes**    | 30 MRI datasets (10 Training, 20 Testing)          |
| **🏥 Imaging Modality** | Magnetic Resonance Imaging (MRI)                   |
| **📦 Total Size**       | ~1.78 GB (compressed)                              |
| **🏥 Source**           | King’s College London and Philips Technologie GmbH |

#### 🎭 Segmentation Task Details

- **Task Type**: 3D binary semantic segmentation
- **Annotation Targets**: Left Atrium (LA) including a short part of the LA appendage trunk plus the proximal parts of
  the pulmonary veins.
- **Ground Truth**: Expert manual segmentations provided for the training set.

#### 💡 Usage Notes

- ✅ Established benchmark dataset from the MICCAI'13 STACOM workshop (LASC'13).
- ✅ Specifically designed for evaluating algorithms that segment the left atrium for atrial fibrillation ablation
  guidance and cardiac biophysical modeling.
- ✅ Includes both MRI and (historically) CT modalities, though only MRI is publicly available in this Kaggle mirror.
- 📚 Required to cite the original *IEEE Transactions on Medical Imaging* publication.
- 🔐 Distributed under EU ODP Legal Notice / Open Access policy with attribution.

#### ⚠️ Usage Considerations

| Aspect                    | Recommendation                                                                                 |
|---------------------------|------------------------------------------------------------------------------------------------|
| **📦 3D Data Handling**   | Volumes are large; ensure adequate RAM/GPU memory or use patch-based 3D training.              |
| **🧪 Evaluation Metrics** | Use standard challenge metrics: Dice Similarity Coefficient (DSC) and Hausdorff Distance (HD). |
| **🔐 Licensing**          | Verify compliance with the original LASC'13 data use agreement for commercial use.             |

#### 💡 Suggested Preprocessing Pipeline

1. **Load 3D Volumes**: Use libraries like `SimpleITK` or `nibabel` to read `.mhd`/`.raw` or `.nii` files.
2. **Intensity Normalization**: Clip extreme outliers and normalize voxel intensities (e.g., z-score normalization per
   volume).
3. **Resampling**: Resample all volumes to a consistent isotropic voxel spacing (e.g., 1.0 × 1.0 × 1.0 mm).
4. **Cropping**: Crop to the bounding box of the heart/atria to reduce background memory overhead.
5. **3D Augmentation**: Apply random 3D rotations, elastic deformations, and intensity shifts during training.

#### 📚 Citation

If you use this dataset, please cite:

@article{tobon2015benchmark,
    title = {Benchmark for algorithms segmenting the left atrium from 3D CT and MRI datasets},
    author = {Tobon-Gomez, Catalina and Geers, Arjan J and Peters, Jochen and Weese, J{\"u}rgen and Pinto, Karim and Karim, Rashed and Ammar, Mouloud and Daoudi, Ahror and Margeta, Jan and Sandoval, Zuluaga and others},
    journal = {IEEE transactions on medical imaging},
    volume = {34},
    number = {7},
    pages = {1460--1473},
    year = {2015},
    publisher = {IEEE}
}
```

---
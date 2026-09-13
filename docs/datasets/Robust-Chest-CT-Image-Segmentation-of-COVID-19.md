### 🫁 Robust Chest CT Segmentation of COVID-19 Lung Infection
**Study**: Müller, D., Soto Rey, I., & Kramer, F. (2021). Robust Chest CT Image Segmentation of COVID-19 Lung Infection based on limited data. Zenodo.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                 |
|-------------------------|-------------------------------------------------------------------------|
| **📛 Title**            | Robust Chest CT Segmentation of COVID-19 Lung Infection                 |
| **🔗 Source**           | https://zenodo.org/records/4875738                                      |
| **🫁 Target Organ**     | Lungs / Chest                                                           |
| **📅 Last Accessed**    | September 10, 2026                                                      |
| **🎯 Supported Tasks**  | 🎭 Semantic Segmentation                                                |
| **📐 Image Size**       | Variable (3D CT volumes)                                                |
| **📁 Data Format**      | 3D CT scans, segmentation masks, model weights (ZIP archives)           |
| **👥 Demographics**     | ❌ Not included (de-identified clinical CT scans)                        |
| **🔄 Train/Test Split** | ✅ Yes (k-fold CV on 20 scans; separate 100-patient test set)            |

#### 📊 Dataset Composition
| Category                | Details                                                                 |
|-------------------------|-------------------------------------------------------------------------|
| **🖼️ Total Volumes**   | 20 CT scans (training/validation) + 100 CT scans (testing)              |
| **🏥 Imaging Modality** | Computed Tomography (CT)                                                |
| **📦 Total Size**       | ~3.2 GB (includes evaluation data, models, predictions, supplementary)  |
| **🏥 Source**           | MIScnn framework research cohort                                        |

#### 🎭 Segmentation Task Details
- **Task Type**: 3D semantic segmentation of thoracic structures and pathological regions.
- **Number of Classes**: 3️⃣ (Background, Healthy Lung Tissue, COVID-19 Infected Regions)
- **Annotation Protocol**: Expert radiologist annotations for lungs and COVID-19 infection zones.

#### 💡 Usage Notes
- ✅ Specifically designed to address the challenge of training robust models on **limited medical data**.
- ✅ Includes a rigorous evaluation protocol: k-fold cross-validation on a small cohort, plus a completely held-out 100-patient test set to measure true generalizability.
- ✅ Achieved a Dice similarity coefficient of 0.804 (validation) and 0.661 (testing) for COVID-19 infection segmentation using a standard 3D U-Net.
- 📚 Required to cite the original Zenodo repository and the associated MIScnn publication.
- 🔐 License: Creative Commons Attribution 4.0 International (CC BY 4.0)

#### ⚠️ Usage Considerations
| Aspect                     | Recommendation                                                                     |
|----------------------------|------------------------------------------------------------------------------------|
| **🔍 Limited Training Data**| The 20-scan training set is intentionally small to simulate data scarcity; leverage the provided extensive data augmentation pipeline. |
| **📦 3D Processing**       | Requires 3D deep learning frameworks (e.g., 3D U-Net); ensure adequate GPU memory or use patch-based training. |
| **🧪 Generalization**      | The 100-patient test set is the true benchmark; do not tune hyperparameters on this set. |

#### 💡 Suggested Preprocessing Pipeline
1. **Load 3D data**: Use libraries like `nibabel`, `SimpleITK`, or the provided MIScnn framework to read NIfTI/DICOM volumes.
2. **Intensity windowing**: Apply standard lung windowing (e.g., -1000 to 400 Hounsfield Units) and normalize to [0, 1].
3. **Resampling**: Resample all volumes to isotropic voxel spacing (e.g., 1.0 × 1.0 × 1.0 mm) for consistent 3D convolution.
4. **On-the-fly augmentation**: Utilize the provided pipeline for random cropping, rotation, and intensity shifting to prevent overfitting on the small training set.
5. **Evaluation metrics**: Report 3D Dice Similarity Coefficient (DSC) and Intersection over Union (IoU) for both lung and infection classes, especially on the 100-patient test set.

#### 📚 Citation
If you use this dataset, please cite:
```bibtex
@dataset{muller2021robust,
  author = {M{\"u}ller, Dominik and Soto Rey, I{\~n}aki and Kramer, Frank},
  title = {Robust Chest CT Image Segmentation of COVID-19 Lung Infection based on limited data},
  year = {2021},
  publisher = {Zenodo},
  version = {2.0},
  doi = {10.5281/zenodo.4875738},
  url = {https://doi.org/10.5281/zenodo.4875738}
}
```

---

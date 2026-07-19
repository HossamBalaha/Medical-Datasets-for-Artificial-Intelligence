### 🧠 Brain Tumor Dataset (Jun Cheng)

**Study**: Cheng, J. (2024). brain tumor dataset. Figshare.

[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                       |
|-------------------------|---------------------------------------------------------------|
| **📛 Title**            | Brain Tumor Dataset                                           |
| **🔗 Source**           | https://doi.org/10.6084/m9.figshare.1512427                   |
| **🧠 Target Organ**     | Brain                                                         |
| **📅 Last Accessed**    | June 20, 2026                                                 |
| **🎯 Supported Tasks**  | 🏷️ Classification                                            |
| **📐 Image Size**       | Variable (original .mat files; standardization recommended)   |
| **📁 Data Format**      | .mat files (MATLAB), convertible to JPG/PNG via provided code |
| **👥 Demographics**     | ❌ Not included (de-identified)                                |
| **🔄 Train/Test Split** | ✅ Yes (Cross-validation indices provided in `cvind.mat`)      |

#### 📊 Dataset Composition

| Category                | Details                                                        |
|-------------------------|----------------------------------------------------------------|
| **🖼️ Total Images**    | 3,064 T1-weighted contrast-enhanced MRI scans                  |
| **🏥 Imaging Modality** | T1-weighted contrast-enhanced Magnetic Resonance Imaging (MRI) |
| **🎨 Color Format**     | Grayscale                                                      |
| **📦 Total Size**       | ~838.77 MB (compressed across 4 ZIP archives)                  |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification
- **Number of Classes**: 3️⃣
- 🧠 Meningioma
- 🧠 Glioma
- 🧠 Pituitary tumor

#### 💡 Usage Notes

- ✅ Suitable for benchmarking convolutional neural networks (CNNs) and transfer learning architectures
- ✅ Cross-validation indices (`cvind.mat`) enable reproducible k-fold cross-validation
- ✅ Images are stored in .mat format; requires MATLAB or Python (e.g., `scipy.io.loadmat`) to load
- ✅ Provided MATLAB code can convert .mat files to standard image formats (e.g., JPG)
- 📚 Required to cite the original Figshare repository when using this dataset in publications
- 🔐 Distributed under CC BY 4.0; attribution required for redistribution or adaptation

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                      |
|----------------------------|-------------------------------------------------------------------------------------|
| **📦 Data Format**         | Images are stored as .mat files; ensure appropriate libraries are installed to load |
| **🔍 Class Distribution**  | Verify class balance across the 3 tumor types; consider class-weighted loss         |
| **📐 Resolution Variance** | Original scans may vary in dimensions; apply uniform resizing prior to training     |
| **🧪 Validation Strategy** | Utilize the provided `cvind.mat` for standardized cross-validation benchmarking     |

#### 💡 Suggested Preprocessing Pipeline

1. **Load .mat files**: Use `scipy.io.loadmat` in Python or native MATLAB functions to extract image data.
2. **Convert formats **(optional): Use the provided MATLAB script or a Python equivalent to save images as JPG/PNG.
3. **Standardize input format**: Convert all images to a consistent color space (single-channel grayscale) and fixed
   resolution (e.g., 224x224 or 256x256).
4. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
5. **Cross-validation splitting**: Load `cvind.mat` to assign images to specific folds for training and validation.
6. **Augmentation **(training only): Incorporate rotation, flipping, and intensity jittering to improve model
   generalization.
7. **Stratified evaluation**: Report per-class metrics (precision, recall, F1-score) to assess performance across tumor
   subtypes.

#### 🔗 Associated Resources

- **Figshare Repository**: https://doi.org/10.6084/m9.figshare.1512427
- **Related Datasets**:
    - [Brain Tumor MRI Dataset (Glioma, Meningioma, Pituitary, No Tumor)](https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{cheng2024braintumor,
    author = {Cheng, Jun},
    title = {brain tumor dataset},
    year = {2024},
    publisher = {Figshare},
    doi = {10.6084/m9.figshare.1512427},
    url = {https://doi.org/10.6084/m9.figshare.1512427}
}
```

---


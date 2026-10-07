### 🫁 Lung Adenocarcinoma Classification (CT Volumes)

**Study**: Feng, Y. (2020). CT Volume Samples for Lung Adenocarcinoma Classification. Mendeley Data, V2.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                     |
|-------------------------|-------------------------------------------------------------|
| **📛 Title**            | Lung Adenocarcinoma Classification                          |
| **🔗 Source**           | https://www.kaggle.com/datasets/saurabhshahane/adenocarcima |
| **🫁 Target Organ**     | Lungs                                                       |
| **📅 Last Accessed**    | October 06, 2026                                            |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                               |
| **📐 Image Size**       | 128 × 128 × 128 voxels (3D volume)                          |
| **📁 Data Format**      | NumPy arrays (.npy)                                         |
| **👥 Demographics**     | ❌ Not included                                              |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)      |

#### 📊 Dataset Composition

| Category                | Details                           |
|-------------------------|-----------------------------------|
| **🖼️ Total Samples**   | 1,050 3D CT volume samples        |
| **🏥 Imaging Modality** | Computed Tomography (CT)          |
| **📦 Total Size**       | ~4.61 GB                          |
| **🏥 Source**           | Locally cropped from 3D CT images |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of early-stage lung adenocarcinoma pathology
- **Number of Classes**: 3️⃣
    - 🟡 Atypical Adenomatous Hyperplasia (AAH) - 21 samples
    - 🟠 Adenocarcinoma In Situ (AIS) - 444 samples
    - 🔴 Minimally Invasive Adenocarcinoma (MIA) - 585 samples

#### 💡 Usage Notes

- ✅ Specifically designed for the challenging task of differentiating early-stage adenocarcinoma spectrum lesions.
- ✅ Pre-processed into fixed-size 3D NumPy arrays, ready for direct ingestion into 3D Convolutional Neural Networks (
  3D-CNNs).
- ✅ Tumor is centered within the 128³ voxel volume, simplifying the learning task for the model.
- 📚 Required to cite the original Mendeley Data repository (DOI: 10.17632/r3tbsgtpzg.2) in publications.
- 🔐 Distributed under CC BY 4.0; attribution required.

#### ⚠️ Usage Considerations

| Aspect                        | Recommendation                                                                                                     |
|-------------------------------|--------------------------------------------------------------------------------------------------------------------|
| **🔍 Severe Class Imbalance** | AAH class is significantly underrepresented (21 samples); apply heavy oversampling, SMOTE, or class-weighted loss. |
| **📦 3D Memory Constraints**  | 128³ volumes require substantial GPU memory; consider cropping to 64³ or using patch-based training if needed.     |
| **🧪 Validation Strategy**    | Implement patient-aware splitting if patient metadata becomes available to prevent data leakage.                   |

#### 💡 Suggested Preprocessing Pipeline

1. **Load NumPy arrays**: Use `numpy.load()` to read the .npy files directly into memory.
2. **Verify centering**: Confirm that the nodule/lesion remains centered within the volume post-loading.
3. **Intensity windowing**: Apply lung windowing (e.g., -1000 to 400 Hounsfield Units) and normalize to [0, 1].
4. **3D Augmentation **(training only): Incorporate 3D rotation, flipping, and elastic deformations to improve model
   robustness.
5. **Stratified evaluation**: Report per-class precision, recall, F1-score, and a confusion matrix to assess
   differentiation between AAH, AIS, and MIA.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{feng2020lungadeno,
    author = {Feng, Yuanli},
    title = {CT Volume Samples for Lung Adenocarcinoma Classification},
    year = {2020},
    publisher = {Mendeley Data},
    version = {2},
    doi = {10.17632/r3tbsgtpzg.2},
    url = {https://data.mendeley.com/datasets/r3tbsgtpzg/2}
}
```

---

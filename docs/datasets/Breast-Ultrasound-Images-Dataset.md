### 🫀 Breast Ultrasound Images Dataset (BUSI)

**Study**: Al-Dhabyani, W., Gomaa, M., Khaled, H., & Fahmy, A. (2020). Dataset of breast ultrasound images.
*Data in Brief*, 28, 104863.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                     |
|-------------------------|-----------------------------------------------------------------------------|
| **📛 Title**            | Breast Ultrasound Images Dataset (BUSI)                                     |
| **🔗 Source**           | https://www.kaggle.com/datasets/aryashah2k/breast-ultrasound-images-dataset |
| **🫀 Target Organ**     | Breast                                                                      |
| **📅 Last Accessed**    | September 11, 2026                                                          |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification, 🎭 Segmentation, 📍 Detection                |
| **📐 Image Size**       | ~500 × 500 pixels (average)                                                 |
| **📁 Data Format**      | PNG (.png) with ground truth masks appended                                 |
| **👥 Demographics**     | ✅ Female patients, ages 25–75 (N=600)                                       |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                      |

#### 📊 Dataset Composition

| Category                  | Details                         |
|---------------------------|---------------------------------|
| **🖼️ Total Images**      | 780 ultrasound images           |
| **🔬 Imaging Modality**   | Medical Ultrasound Imaging      |
| **📦 Total Size**         | ~266.19 MB (compressed)         |
| **🏥 Source Institution** | Baseline data collection (2018) |

#### 🏷️ Classification & Segmentation Task Details

- **Task Type**: Multiclass classification and lesion segmentation
- **Number of Classes**: 3️⃣
    - ✅ Normal
    - 🟢 Benign
    - 🔴 Malignant
- **Annotation Format**: Ground truth (GT) segmentation masks are presented at the bottom of each image file.

**📊 Dataset Distribution**:
| Class | Image Count |
|------------|-------------|
| ✅ Normal | 266 |
| 🟢 Benign | ~437*       |
| 🔴 Malignant| ~210*       |
*(Note: Counts may vary slightly based on exact file extraction, but total is 780).*

#### 💡 Usage Notes

- ✅ One of the most widely used benchmark datasets for breast ultrasound analysis.
- ✅ Supports joint learning of classification, detection, and segmentation due to the inclusion of GT masks.
- ✅ Relatively small and clean dataset, ideal for prototyping, transfer learning, and few-shot learning studies.
- 📚 Required to cite the original *Data in Brief* publication when using this dataset.
- 🔐 License: CC0: Public Domain.

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Mask Extraction**     | GT masks are appended to the bottom of the image; a preprocessing step is required to crop and separate the mask from the original image. |
| **📐 Resolution Variance** | Images average 500x500 but may vary; standardize to fixed dimensions (e.g., 224x224 or 256x256).                                          |
| **🧪 Class Imbalance**     | Normal class is well-represented, but verify benign/malignant ratios for specific tasks; apply stratified splitting.                      |

#### 💡 Suggested Preprocessing Pipeline

1. **Mask Separation**: Programmatically crop the bottom portion of each PNG to isolate the ground truth mask, saving it
   as a separate binary file.
2. **Standardize geometry**: Resize both the ultrasound image and the extracted mask to uniform dimensions (e.g.,
   256×256). Use nearest-neighbor interpolation for the mask.
3. **Intensity normalization**: Apply speckle noise reduction (e.g., Non-Local Means or Median filtering) and scale
   pixel values to [0, 1].
4. **Augmentation **(training only): Incorporate rotation, flipping, and elastic deformations; preserve the
   morphological integrity of the lesion.
5. **Stratified splitting**: Partition data by patient (if metadata permits) or use stratified k-fold cross-validation
   to maintain class balance.
6. **Evaluation metrics**: Report AUC-ROC and F1-score for classification; compute Dice/IoU for segmentation.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{aldhabyani2020dataset,
  title={Dataset of breast ultrasound images},
  author={Al-Dhabyani, Walid and Gomaa, Mohammed and Khaled, Hussien and Fahmy, Aly},
  journal={Data in brief},
  volume={28},
  pages={104863},
  year={2020},
  publisher={Elsevier},
  doi={10.1016/j.dib.2019.104863}
}
```

---

### 🎀 Breast Cancer Grading (H&E Stained)

**Study**: Yan, R. (2021). Breast cancer grading guided by nuclei-related features in HE-stained pathological images.
GitHub.  
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                |
|-------------------------|--------------------------------------------------------|
| **📛 Title**            | Breast Cancer Grading (Nuclei-related Features)        |
| **🔗 Source**           | https://github.com/YANRUI121/Breast-cancer-grading     |
| **🫁 Target Organ**     | Breast                                                 |
| **📅 Last Accessed**    | August 27, 2026                                        |
| **🎯 Supported Tasks**  | 🏷️ Multi-class Classification (Grading)               |
| **📐 Image Size**       | Variable (Acquired at 20X and 40X magnification)       |
| **📁 Data Format**      | JPEG (.jpg)                                            |
| **👥 Demographics**     | ❌ Not included                                         |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended) |

#### 📊 Dataset Composition

| Category                | Details                                                   |
|-------------------------|-----------------------------------------------------------|
| **🖼️ Total Images**    | 3,644 H&E-stained breast invasive ductal carcinoma images |
| **🏥 Imaging Modality** | Histopathology (20X and 40X magnification)                |
| **📦 Total Size**       | ~Not specified (Lightweight)                              |
| **🏥 Source**           | Research Lab Collection                                   |

#### 🏷️ Classification Task Details

- **Task Type**: Multi-class ordinal classification (Histological Grading)
- **Number of Classes**: 3️⃣
    - 1️⃣ Grade 1 (Well-differentiated)
    - 2️⃣ Grade 2 (Moderately differentiated)
    - 3️⃣ Grade 3 (Poorly differentiated)
      *(Note: The first number in each filename indicates the grade, e.g., "1—YYY...jpg")*

#### 💡 Usage Notes

- ✅ Specifically focused on invasive ductal carcinoma, guided by nuclei-related morphological features.
- ✅ Contains a mix of 20X (2,486 images) and 40X (1,158 images) magnifications, offering multi-scale learning
  opportunities.
- 🔐 License: Academic use (Contact author for commercial terms).

#### ⚠️ Usage Considerations

| Aspect                        | Recommendation                                                                                                                                     |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Magnification Variance** | The dataset mixes 20X and 40X images. Consider training separate models per magnification or using magnification-aware augmentation/normalization. |
| **📐 Filename Parsing**       | The grade is encoded in the filename prefix. Ensure your dataloader correctly parses this integer label rather than relying on folder structure.   |
| **🧪 Validation Strategy**    | Implement stratified k-fold cross-validation to ensure all three grades are proportionally represented in training and validation splits.          |

#### 💡 Suggested Preprocessing Pipeline

1. **Label Extraction**: Parse the leading integer from each filename to assign the ground-truth grade label.
2. **Magnification Grouping**: Optionally split the dataset or add a magnification metadata channel to help the model
   adapt to 20X vs. 40X resolution differences.
3. **Color Normalization**: Apply Macenko or Vahadane stain normalization to standardize H&E appearance.
4. **Standardize Input**: Resize all images to a fixed dimension (e.g., 224x224) and convert to tensors.
5. **Augmentation**: Apply rotation, flipping, and mild elastic deformations to simulate natural tissue variations.

#### 📚 Citation

If you use this dataset, please contact the author and cite:

```bibtex
@misc{yan2021breastcancergrading,
  author = {Yan, Rui},
  title = {Breast cancer grading guided by nuclei-related features in HE-stained pathological images},
  year = {2021},
  publisher = {GitHub},
  url = {https://github.com/YANRUI121/Breast-cancer-grading}
}
```

---

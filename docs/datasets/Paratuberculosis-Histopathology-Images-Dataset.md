### 🦠 Paratuberculosis Histopathology Images Dataset

**Study**: Hananeh, W., & Fraiwan, M. (2025). A dataset of histopathology images of paratuberculosis disease. Mendeley
Data, V3.

[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                                       |
|-------------------------|-----------------------------------------------------------------------------------------------|
| **📛 Title**            | Paratuberculosis Histopathology Images Dataset                                                |
| **🔗 Source**           | https://data.mendeley.com/datasets/zjhymwjtxv/3                                               |
| **🐄 Target Organ**     | Intestinal Tissue (Veterinary Pathology)                                                      |
| **📅 Last Accessed**    | May 24, 2026                                                                                  |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification (Normal vs. Infected)                                               |
| **📐 Image Size**       | Variable (histopathology slides; standardization recommended)                                 |
| **📁 Data Format**      | Image files (format unspecified; typical: JPG/PNG); optional scale-bar variants in `ImagesS/` |
| **👥 Demographics**     | ❌ Not included (veterinary tissue samples; de-identified)                                     |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                                        |

#### 📊 Dataset Composition

| Category                  | Details                                                                     |
|---------------------------|-----------------------------------------------------------------------------|
| **🖼️ Total Images**      | 366 histopathology images of intestinal tissue                              |
| **🔬 Imaging Modality**   | Brightfield histopathology (H&E-stained tissue sections)                    |
| **🎨 Color Format**       | RGB (typical for histopathology)                                            |
| **📦 Total Size**         | ~28.6 MB (compressed)                                                       |
| **🏫 Source Institution** | Jordan University of Science and Technology, Faculty of Veterinary Medicine |
| **👨‍⚕️ Annotation**      | Expert veterinary pathologist-labeled binary classes                        |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification of paratuberculosis infection status in intestinal tissue
- **Number of Classes**: 2️⃣

| Class Label | Description                                                          | Image Count | Clinical Interpretation                    |
|-------------|----------------------------------------------------------------------|-------------|--------------------------------------------|
| ✅ Negative  | Normal intestinal tissue                                             | 157         | No evidence of paratuberculosis            |
| ⚠️ Positive | Tissue infected with *Mycobacterium avium* subsp. *paratuberculosis* | 209         | Histopathological signs of Johne's disease |

**📊 Dataset Distribution**:

| Class     | Image Count | Percentage |
|-----------|-------------|------------|
| Negative  | 157         | ~42.9%     |
| Positive  | 209         | ~57.1%     |
| **Total** | **366**     | **100%**   |

**🔬 Additional Resource: Scale-Bar Variants**

- The `ImagesS/` subdirectory contains identical images with an overlaid scale bar to clarify magnification level
- Useful for research requiring explicit spatial calibration or multi-scale analysis

#### 💡 Usage Notes

- ✅ First publicly available histopathology dataset dedicated to paratuberculosis (Johne's disease) detection
- ✅ Binary classification task suitable for benchmarking veterinary diagnostic AI models
- ✅ Near-balanced class distribution (~43/57) supports stable training without aggressive resampling
- ✅ Scale-bar variant images enable research on resolution-aware feature extraction
- ✅ Small dataset size (~366 images) ideal for few-shot learning, transfer learning, or data augmentation studies
- 📚 Required to cite the original Mendeley Data repository (DOI: 10.17632/zjhymwjtxv.3) in publications
- 🔐 Verify licensing terms on Mendeley Data; attribution typically required under CC BY 4.0

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                  |
|----------------------------|-------------------------------------------------------------------------------------------------|
| **🔍 Limited Sample Size** | Small dataset (n=366); employ strong regularization, augmentation, or transfer learning         |
| **🧪 Class Balance**       | Mild imbalance (~57% positive); consider stratified sampling or class-weighted loss             |
| **📐 Resolution Variance** | Images may vary in magnification; standardize input dimensions prior to training                |
| **🔐 Ethical Compliance**  | Veterinary tissue samples; adhere to institutional animal research guidelines                   |
| **🧭 Domain Specificity**  | Focused on paratuberculosis in ruminants; generalizability to other species requires validation |
| **🎨 Stain Variability**   | Apply stain normalization (e.g., Macenko method) if integrating external cohorts                |

#### 💡 Suggested Preprocessing Pipeline

1. **Download and extract**: Obtain dataset from Mendeley Data; choose between standard images or `ImagesS/` scale-bar
   variants based on research needs.
2. **Organize directory structure**: Arrange images into class-labeled subfolders (e.g., `Negative/`, `Positive/`) for
   framework-native data loading.
3. **Standardize geometry**: Resize images to uniform dimensions (e.g., 224×224 or 512×512) while preserving aspect
   ratio.
4. **Color normalization**: Apply stain normalization to mitigate inter-slide H&E staining variability.
5. **Augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering; preserve
   histological feature integrity.
6. **Stratified splitting**: Partition data with stratification to maintain class balance across train/validation/test
   sets.
7. **Evaluation metrics**: Report sensitivity, specificity, AUC-ROC, and F1-score; include confusion matrices to assess
   diagnostic performance.

#### 🔗 Associated Resources

- **Mendeley Data Repository**: https://data.mendeley.com/datasets/zjhymwjtxv/3
- **Institutional Affiliation**: Jordan University of Science and Technology, Faculty of Veterinary Medicine
- **Related Publications**:
    - Hananeh, W., & Fraiwan, M. (2025). "A dataset of histopathology images of paratuberculosis disease." *Mendeley
      Data*, V3.
    - Relevant veterinary pathology literature on Johne's disease diagnosis and histopathological features.
- **Related Datasets**:
    - [Dartmouth Kidney Cancer Histology Dataset](https://bmirds.github.io/KidneyCancer/) (human histopathology
      classification)
    - [CRC-HGD-v1](https://data.mendeley.com/datasets/yfp5sfj47m/2) (colorectal grading)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{hananeh2025paratuberculosis,
    author = {Hananeh, Wael and Fraiwan, Mohammad},
    title = {A dataset of histopathology images of paratuberculosis disease},
    year = {2025},
    publisher = {Mendeley Data},
    version = {3},
    doi = {10.17632/zjhymwjtxv.3},
    url = {https://data.mendeley.com/datasets/zjhymwjtxv/3}
}
```

---


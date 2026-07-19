### 🔬 Histopathological Imaging Database for Oral Cancer Analysis

**Study**: Rahman, T. Y., Mahanta, L. B., Das, A. K., & Sarma, J. D. (2020). Histopathological imaging database for oral
cancer analysis. *Data in Brief*, 29, 105114.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                           |
|-------------------------|-------------------------------------------------------------------|
| **📛 Title**            | Histopathological Imaging Database for Oral Cancer Analysis       |
| **🔗 Source**           | https://data.mendeley.com/datasets/ftmp4cvtmb/2                   |
| **🗣️ Target Organ**    | Oral Cavity (Buccal Mucosa)                                       |
| **📅 Last Accessed**    | April 11, 2026                                                    |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification, 🎭 Segmentation, 🔍 Feature Extraction |
| **📐 Image Size**       | 2048 x 1536 pixels (fixed resolution)                             |
| **📁 Data Format**      | JPEG (.jpg)                                                       |
| **👥 Demographics**     | ❌ Not included (de-identified; 230 patients total)                |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)            |

#### 📊 Dataset Composition

| Category                    | Details                                                                  |
|-----------------------------|--------------------------------------------------------------------------|
| **🖼️ Total Images**        | 1,224 histopathological images                                           |
| **🔬 Imaging Modality**     | Brightfield histopathology (H&E-stained punch biopsy sections)           |
| **🔍 Magnification Levels** | 100x (10x objective x 10x eyepiece), 400x (40x objective x 10x eyepiece) |
| **📦 Total Size**           | ~2.89 GB (compressed)                                                    |
| **🏥 Curation**             | Ayursundra Healthcare Pvt. Ltd. & Dr. B. Borooah Cancer Institute, India |
| **📅 Collection Period**    | October 2016 - November 2017                                             |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification (Normal vs. Malignant)
- **Number of Classes**: 2️⃣
    - ✅ Normal Epithelium of Oral Cavity
    - ⚠️ Oral Squamous Cell Carcinoma (OSCC)

**📊 Image Distribution by Magnification**:

| Magnification | Category | Image Count | Primary Application Scope                                                                    |
|---------------|----------|-------------|----------------------------------------------------------------------------------------------|
| **100x**      | Normal   | 89          | Architectural/tissue-level analysis, epithelial layer segmentation, tumor invasion detection |
| **100x**      | OSCC     | 439         | —                                                                                            |
| **400x**      | Normal   | 201         | Cellular/nuclear-level analysis, texture-based feature extraction                            |
| **400x**      | OSCC     | 495         | —                                                                                            |
| **Total**     | —        | **1,224**   | —                                                                                            |

**🔬 Multi-Scale Analysis Capability**:

- **100x images**: Optimized for tissue architecture assessment, basement membrane invasion detection, and whole-image
  feature extraction.
- **400x images**: Suitable for cytological analysis, nuclear morphometry, and fine-grained textural pattern
  classification.

#### 💡 Usage Notes

- ✅ First publicly available dataset dedicated to oral cavity histopathology with OSCC labels
- ✅ Dual-magnification design enables multi-scale feature learning and resolution-aware modeling
- ✅ Expert-validated labels derived from corresponding pathological reports
- ✅ Open access under CC BY 4.0 license; attribution required for reuse
- 📚 Cite both the *Data in Brief* article and the Mendeley Data repository in publications

#### ⚠️ Usage Considerations

| Aspect                         | Recommendation                                                                                 |
|--------------------------------|------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**         | OSCC class is substantially larger than Normal; apply class weighting or oversampling          |
| **🔬 Magnification Strategy**  | Process 100x and 400x sets separately or fuse features via multi-branch architectures          |
| **🧪 Domain Specificity**      | Images sourced from buccal mucosa; generalizability to other oral subsites requires validation |
| **🎨 Stain Variability**       | Apply stain normalization (e.g., Macenko) to mitigate inter-slide color variation              |
| **🧭 Data Leakage Prevention** | Partition by patient ID (not image) to ensure no patient appears in both train and test sets   |

#### 💡 Suggested Preprocessing Pipeline

1. **Organize by magnification**: Create separate directories for 100x and 400x images, subdivided by class.
2. **Patient-aware splitting**: Use metadata (if available) or file naming conventions to ensure patient-level
   stratification.
3. **Resolution standardization**: Resize images to model-compatible dimensions (e.g., 224x224, 512x512) while
   preserving aspect ratio.
4. **Color normalization**: Apply histogram matching or stain normalization to reduce batch effects.
5. **Augmentation **(training): Incorporate rotation, flipping, and mild intensity jittering; avoid aggressive
   transformations that distort histological structures.
6. **Feature extraction **(optional): For traditional ML approaches, extract GLCM, LBP, or color histogram features as
   demonstrated in the original study.
7. **Evaluation**: Report sensitivity, specificity, and AUC-ROC alongside accuracy, given the clinical diagnostic
   context.

#### 🔗 Associated Resources

- **GitHub Repository**:
  https://github.com/Tabassum2019/A-histopathological-image-repository-of-normal-epithelium-of-Oral-Cavity-and-OSCC
- **Related Publications**:
    - Rahman, T. Y., Mahanta, L. B., Chakraborty, C., Das, A. K., & Sarma, J. D. (2018). Textural pattern classification
      for oral squamous cell carcinoma. Journal of microscopy, 269(1), 85-93. [DOI](https://doi.org/10.1111/jmi.12611)
    - Rahman, T. Y., Mahanta, L. B., Das, A. K., & Sarma, J. D. (2020). Automated oral squamous cell carcinoma
      identification using shape, texture and color features of whole image strips. Tissue and Cell, 63,
        101322. [DOI](https://doi.org/10.1016/j.tice.2019.101322)
- **Contact**: Corresponding authors via Mendeley Data page or institutional affiliations

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{rahman2023oralcancer,
    author = {Rahman, Tabassum Yesmin and Mahanta, Lipi B. and Das, Anup K. and Sarma, Jagannath D.},
    title = {Histopathological imaging database for Oral Cancer analysis},
    year = {2023},
    publisher = {Mendeley Data},
    version = {2},
    doi = {10.17632/ftmp4cvtmb.2},
    url = {https://data.mendeley.com/datasets/ftmp4cvtmb/2}
}

@article{rahman2020dib,
    title = {Histopathological imaging database for oral cancer analysis},
    author = {Rahman, Tabassum Yesmin and Mahanta, Lipi B. and Das, Anup K. and Sarma, Jagannath D.},
    journal = {Data in Brief},
    volume = {29},
    pages = {105114},
    year = {2020},
    publisher = {Elsevier},
    doi = {10.1016/j.dib.2020.105114}
}
```

---


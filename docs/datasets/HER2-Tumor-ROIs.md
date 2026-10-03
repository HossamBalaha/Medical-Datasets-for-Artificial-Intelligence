### 🫀 HER2 tumor ROIs

**Study**: Farahmand, S., Fernandez, A. I., Ahmed, F. S., Rimm, D. L., Chuang, J. H., Reisenbichler, E., & Zarringhalam,
K. (2022). Deep learning trained on hematoxylin and eosin tumor region of Interest predicts HER2 status and trastuzumab
treatment response in HER2+ breast cancer. *Modern Pathology*, 35(1), 44–51.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                          |
|-------------------------|------------------------------------------------------------------|
| **📛 Title**            | HER2 tumor ROIs                                                  |
| **🔗 Source**           | https://www.cancerimagingarchive.net/collection/her2-tumor-rois/ |
| **🫀 Target Organ**     | Breast                                                           |
| **📅 Last Accessed**    | October 03, 2026                                                 |
| **🎯 Supported Tasks**  | 🏷️ Classification, 🎭 Segmentation (ROI)                        |
| **📐 Image Size**       | Variable (Whole Slide Images, 20x magnification)                 |
| **📁 Data Format**      | SVS (images), XML (ROI annotations), XLSX (clinical data)        |
| **👥 Demographics**     | ✅ 273 subjects (Yale and TCGA cohorts)                           |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)           |

#### 📊 Dataset Composition

| Category                | Details                                  |
|-------------------------|------------------------------------------|
| **🖼️ Total Slides**    | 273 Whole Slide Images (WSIs)            |
| **🔬 Imaging Modality** | Brightfield histopathology (H&E stained) |
| **📦 Total Size**       | ~40 GB                                   |
| **🏥 Source**           | The Cancer Imaging Archive (TCIA)        |

#### 🏷️ Classification & Segmentation Task Details

- **Task Type**: Slide-level classification and ROI segmentation
- **Number of Classes**:
    - **HER2 Status**: HER2+ (Amplified), HER2- (Non-amplified)
    - **Treatment Response**: Responder, Non-responder (for trastuzumab therapy)
- **Annotation Targets**: Expert-pathologist annotated Regions of Interest (ROIs) for invasive carcinoma, excluding
  necrosis or benign stroma.

#### 💡 Usage Notes

- ✅ Unique dataset linking H&E morphology to both HER2 status and trastuzumab treatment response.
- ✅ Includes XML ROI annotations, enabling focused training on tumor regions and reducing background noise.
- ✅ Combines Yale cohort (192 cases) and TCGA-BRCA cohort (182 filtered cases) for robust evaluation.
- 📚 Required to cite the original TCIA collection and the associated *Modern Pathology* publication.
- 🔐 Distributed under CC BY 4.0; attribution required.

#### ⚠️ Usage Considerations

| Aspect                    | Recommendation                                                                                      |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| **📦 Large File Sizes**   | SVS files are massive; use libraries like `OpenSlide` or `tifffile` for efficient loading.          |
| **🧪 ROI Utilization**    | Leverage the provided XML annotations to tile tumor regions specifically, improving model accuracy. |
| **🔐 Ethical Compliance** | Approved by Yale Human Investigation Committee; adhere to TCIA data usage policies.                 |

#### 💡 Suggested Preprocessing Pipeline

1. **Parse metadata**: Load the XLSX clinical data to map slide IDs to HER2 status and treatment response.
2. **Load WSIs**: Use `OpenSlide` to read the high-resolution SVS images.
3. **Extract ROIs**: Parse the XML annotation files to extract tumor region coordinates and tile these areas.
4. **Standardize resolution**: Resize extracted tiles to a uniform dimension (e.g., 224×224 or 512×512).
5. **Color normalization**: Apply stain normalization (e.g., Macenko method) to mitigate inter-slide H&E variability.
6. **Stratified evaluation**: Report slide-level AUC-ROC, sensitivity, and specificity for HER2 status and treatment
   response prediction.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{farahmand2022deep,
    title = {Deep learning trained on hematoxylin and eosin tumor region of Interest predicts HER2 status and trastuzumab treatment response in HER2+ breast cancer},
    author = {Farahmand, Saman and Fernandez, Aileen I and Ahmed, Fahad Shabbir and Rimm, David L and Chuang, Jeffrey H and Reisenbichler, Emily and Zarringhalam, Kourosh},
    journal = {Modern Pathology},
    volume = {35},
    number = {1},
    pages = {44--51},
    year = {2022},
    publisher = {Elsevier}
}

@dataset{farahmand2022her2,
    author = {Farahmand, Saman and Fernandez, Aileen I and Ahmed, Fahad Shabbir and Rimm, David L. and Chuang, Jeffrey H. and Reisenbichler, Emily and Zarringhalam, Kourosh},
    title = {HER2 and trastuzumab treatment response H&E slides with tumor ROI annotations},
    year = {2022},
    publisher = {The Cancer Imaging Archive},
    doi = {10.7937/E65C-AM96},
    url = {https://www.cancerimagingarchive.net/collection/her2-tumor-rois/}
}
```

---

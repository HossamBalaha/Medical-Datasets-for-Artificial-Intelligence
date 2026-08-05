### 🫀 Digital Mammography Dataset for Breast Cancer Diagnosis Research (DMID)

**Study**: Oza, P., Oza, R., Oza, U., Sharma, P., Patel, S., Kumar, P., & Gohel, B. (2023). Digital mammography Dataset
for Breast Cancer Diagnosis Research (DMID) [Data set]. Figshare.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                 |
|-------------------------|-------------------------------------------------------------------------|
| **📛 Title**            | Digital Mammography Dataset for Breast Cancer Diagnosis Research (DMID) |
| **🔗 Source**           | https://doi.org/10.6084/m9.figshare.24522883                            |
| **🫀 Target Organ**     | Breast                                                                  |
| **📅 Last Accessed**    | August 05, 2026                                                         |
| **🎯 Supported Tasks**  | 🏷️ Classification,  Segmentation                                       |
| **📐 Image Size**       | Variable (High-resolution DICOM and TIFF formats)                       |
| ** Data Format**        | DICOM, TIFF, PNG (masks), XLSX (metadata)                               |
| **👥 Demographics**     | ❌ Not explicitly detailed in the primary metadata                       |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                  |

#### Dataset Composition

| Category              | Details                                                                  |
|-----------------------|--------------------------------------------------------------------------|
| **🖼️ Total Images**  | Mammograms (Exact count varies by split; includes DCM and TIFF variants) |
| ** Imaging Modality** | Digital Mammography (X-ray)                                              |
| **📦 Total Size**     | ~10.92 GB (Compressed archives)                                          |
| **📦 Data Sources**   | Clinical mammography records (de-identified)                             |

#### 🏷️ Classification & Segmentation Task Details

- **Task Type**: Binary classification (Normal vs. Abnormal) and pixel-level semantic segmentation.
- **Number of Classes**: 2️⃣ Binary (Normal tissue, Abnormal regions/lesions).
- **Annotations**: Includes pixel-level annotation masks for abnormal regions and comprehensive CSV/XLSX metadata.

#### 💡 Usage Notes

- ✅ Highly valuable for multi-task learning frameworks combining detection, classification, and segmentation.
- ✅ Provides multiple image formats (DICOM for raw clinical data, TIFF/PNG for processed research data).
- 📚 Required to cite the original Figshare repository and the associated publication when using this data.
- 🔐 License: CC BY 4.0

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                            |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| **📐 Format Handling**     | DICOM files require specialized libraries (e.g., `pydicom`) for ingestion and windowing.                  |
| ** Class Imbalance**       | Mammography datasets inherently suffer from class imbalance; apply appropriate weighting or oversampling. |
| **🧪 Validation Strategy** | Implement patient-wise splitting to prevent data leakage across train and test sets.                      |

#### Suggested Preprocessing Pipeline

1. **Format Conversion**: Convert DICOM files to standardized 16-bit or 8-bit grayscale TIFF/PNG formats.
2. **Windowing/Normalization**: Apply mammographic windowing (e.g., breast window) and normalize pixel intensities
   to [0, 1].
3. **Mask Alignment**: Ensure pixel-level segmentation masks are perfectly aligned with the corresponding image
   dimensions.
4. **Region of Interest (ROI) Extraction**: Crop or pad images to a fixed resolution (e.g., 512x512 or 1024x1024) while
   preserving aspect ratio.
5. **Augmentation**: Utilize geometric transformations (rotation, flipping) carefully, ensuring masks are transformed
   identically to images.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{oza2023dmid,
  author = {Oza, Parita and Oza, Rajiv and Oza, Urvi and Sharma, Paawan and Patel, Samir and Kumar, Pankaj and Gohel, Bakul},
  title = {Digital mammography Dataset for Breast Cancer Diagnosis Research (DMID)},
  year = {2023},
  publisher = {Figshare},
  doi = {10.6084/m9.figshare.24522883},
  url = {https://doi.org/10.6084/m9.figshare.24522883}
}
```

---

### 🫀 Digital Pathology Dataset for Breast Cancer Diagnosis

**Study**: Naghshineh Kani, S., Soyak, B. C., Gokce, M., Duyar, Z., Alicikus, H., Yapıcıer, Ö., & Oner, M. U. (2024).
Digital Pathology Dataset for Breast Cancer Diagnosis [Data set]. Zenodo.
[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                               |
|-------------------------|-------------------------------------------------------|
| **📛 Title**            | Digital Pathology Dataset for Breast Cancer Diagnosis |
| **🔗 Source**           | https://zenodo.org/records/14131968                   |
| **🫀 Target Organ**     | Breast                                                |
| **📅 Last Accessed**    | July 03, 2026                                         |
| **🎯 Supported Tasks**  | 🎭 Segmentation (Tissue Region)                       |
| **📐 Image Size**       | Variable (Whole Slide Images)                         |
| **📁 Data Format**      | .svs (Aperio) in ZIP archives                         |
| **👥 Demographics**     | ❌ Not included                                        |
| **🔄 Train/Test Split** | ❌ Not provided                                        |

#### 📊 Dataset Composition

| Category                  | Details                                                              |
|---------------------------|----------------------------------------------------------------------|
| **🖼️ Total Slides**      | 235 Whole Slide Images (WSIs)                                        |
| **🔬 Imaging Modality**   | Brightfield histopathology (H&E and IHC stains)                      |
| **📦 File Structure**     | 36 ZIP files for H&E (72 slides) + 55 ZIP files for IHC (163 slides) |
| **🏥 Source Institution** | Bahçeşehir University Medical School, Turkey                         |

#### 🎭 Segmentation Task Details

- **Task Type**: Binary/Multi-class tissue region segmentation
- **Annotation Targets**: Tissue regions vs. background in H&E and IHC stained slides
- **Associated Code
  **: [Tissue Region Segmentation Code](https://github.com/sepidehnaghshineh/Tissue-region-segmentation-in-HE-and-IHC-stained-pathology-slides)

#### 💡 Usage Notes

- ✅ High-quality IHC and H&E WSIs provided in standard .svs format
- ✅ Suitable for benchmarking tissue region segmentation algorithms across different staining modalities
- ✅ Includes associated Python code for tissue region segmentation using deep learning
- 📚 Required to cite the original Zenodo repository when using this dataset
- 🔐 Distributed under CC BY 4.0; attribution required

#### ⚠️ Usage Considerations

| Aspect                    | Recommendation                                                                            |
|---------------------------|-------------------------------------------------------------------------------------------|
| **📦 Large File Sizes**   | WSIs are massive; ensure adequate storage and use libraries like `OpenSlide` or `libvips` |
| **🎨 Stain Variability**  | Dataset includes both H&E and IHC; models may need to handle stain-specific features      |
| **🔐 Ethical Compliance** | Approved by Bahçeşehir University Clinical Research IRB (Approval No: 2022-10/03)         |

#### 💡 Suggested Preprocessing Pipeline

1. **Extract archives**: Unzip the 91 ZIP files containing the .svs WSIs.
2. **Load WSIs**: Use `OpenSlide` or `tifffile` to read the high-resolution .svs images.
3. **Tissue detection**: Apply thresholding or the provided deep learning model to mask out background/glass regions.
4. **Patch extraction**: Extract overlapping or non-overlapping tiles for training segmentation models.
5. **Evaluation**: Compute Dice/IoU scores for tissue vs. background segmentation.

#### 🔗 Associated Resources

- **Zenodo Repository**: https://zenodo.org/records/14131968
- **Code Repository
  **: https://github.com/sepidehnaghshineh/Tissue-region-segmentation-in-HE-and-IHC-stained-pathology-slides

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{naghshinehkani2024digital,
  author = {Naghshineh Kani, Sepideh and Soyak, Burak Can and Gokce, Melih and Duyar, Zeynep and Alicikus, Hasan and Yapıcıer, Özlem and Oner, Mustafa Umit},
  title = {Digital Pathology Dataset for Breast Cancer Diagnosis},
  year = {2024},
  publisher = {Zenodo},
  doi = {10.5281/zenodo.14131968},
  url = {https://doi.org/10.5281/zenodo.14131968}
}
```

---


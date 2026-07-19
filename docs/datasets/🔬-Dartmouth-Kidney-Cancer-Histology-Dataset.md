### 🔬 Dartmouth Kidney Cancer Histology Dataset

**Study**: Zhu, M., Ren, B., Richards, R., Suriawinata, M., Tomita, N., & Hassanpour, S. (2021). Development and
Evaluation of a Deep Neural Network for Histologic Classification of Renal Cell Carcinoma on Biopsy and Surgical
Resection Slides. *Scientific Reports*, 11, 7080.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                 |
|-------------------------|-------------------------------------------------------------------------|
| **📛 Title**            | Dartmouth Kidney Cancer Histology Dataset                               |
| **🔗 Source**           | https://bmirds.github.io/KidneyCancer/                                  |
| **🫘 Target Organ**     | Kidney (Renal)                                                          |
| **📅 Last Accessed**    | April 11, 2026                                                          |
| **🎯 Supported Tasks**  | 🏷️ Classification                                                      |
| **📐 Image Size**       | Variable (WSIs downsampled to 5x magnification from original 20x scans) |
| **📁 Data Format**      | PNG (.png) for whole-slide images; CSV (.csv) for metadata              |
| **👥 Demographics**     | ❌ Not included (de-identified per IRB approval)                         |
| **🔄 Train/Test Split** | ✅ Yes (provided in MetaData.csv)                                        |

#### 📊 Dataset Composition

| Category                | Details                                                                    |
|-------------------------|----------------------------------------------------------------------------|
| **🖼️ Total Images**    | 563 whole-slide images (H&E-stained FFPE tissue sections)                  |
| **🏥 Imaging Modality** | Brightfield histopathology (Hematoxylin & Eosin stain)                     |
| **🔬 Scanner**          | Aperio AT2 whole-slide scanner (original 20x; converted to 5x via libvips) |
| **📦 File Structure**   | 11 ZIP archives (DHMC_wsi_01.zip - DHMC_wsi_11.zip) + MetaData.csv         |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of renal cell carcinoma subtypes
- **Number of Classes**: 4️⃣
    - 🟠 Renal Oncocytoma
    - 🟣 Chromophobe RCC
    - 🔵 Clear cell RCC
    - 🟢 Papillary RCC

**📊 Slide Distribution by Type**:

| Slide Type         | Slide IDs | Archive File       | Approx. Size |
|--------------------|-----------|--------------------|--------------|
| Surgical Resection | 001-484   | DHMC_wsi_01-10.zip | ~85.8 GB     |
| Biopsy (Test Set)  | 485-563   | DHMC_wsi_11.zip    | ~4.7 GB      |
| **Metadata**       | All 563   | MetaData.csv       | —            |

**📋 Metadata Contents** (`MetaData.csv`):

- Slide identifier
- Histologic class label
- Slide type (resection/biopsy)
- Dataset split assignment (train/validation/test)

#### 💡 Usage Notes

- ✅ Suitable for benchmarking deep learning models for whole-slide image classification
- ✅ Includes both resection and biopsy specimens for domain generalization studies
- ✅ Pre-defined train/validation/test splits enable reproducible evaluation
- 📚 Required to cite the original *Scientific Reports* publication when using this dataset
- 🔐 Access requires completion of a Research Use Agreement (non-commercial use only)

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                         |
|----------------------------|------------------------------------------------------------------------------------------------------------------------|
| **🔐 Access Protocol**     | Dataset requires form submission; download links expire after 4 hours                                                  |
| **⚖️ Licensing**           | Non-commercial research use only; redistribution prohibited without permission                                         |
| **🔍 Class Distribution**  | Verify class balance via MetaData.csv; consider stratified sampling if needed                                          |
| **📐 Resolution Handling** | Images are downsampled to 5x; account for magnification in model architecture                                          |
| **🧪 Domain Shift**        | Biopsy slides (DHMC_wsi_11.zip) may exhibit different characteristics than resection slides; evaluate generalizability |

#### 💡 Suggested Preprocessing Pipeline

1. **Request access**: Complete the registration form at the source URL to receive download links.
2. **Parse metadata**: Load `MetaData.csv` to map slide identifiers to labels and dataset splits.
3. **Organize data**: Extract ZIP archives into structured directories (e.g., by split or class).
4. **Patch extraction **(optional): For memory-efficient training, extract fixed-size patches from WSIs using libraries
   such as `OpenSlide` or `libvips`.
5. **Normalization**: Apply stain normalization (e.g., Macenko or Vahadane methods) to mitigate inter-slide variability.
6. **Augmentation**: Incorporate rotation, flipping, and color jittering to improve model robustness.
7. **Evaluation**: Report per-subtype metrics (precision, recall, F1-score) alongside overall accuracy.

#### 🔗 Associated Resources

- **Code Repository**: [DeepSlide](https://github.com/hassanpourlab/DeepSlide) - PyTorch framework for WSI
  classification
- **Related Datasets**: [Dartmouth Lung Cancer Histology Dataset](https://bmirds.github.io/LungCancer/) (same research
  group)
- **Contact**: 📧 BMIRDS team via the contact form on the dataset homepage

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{zhu2021development,
    title = {Development and evaluation of a deep neural network for histologic classification of renal cell carcinoma on biopsy and surgical resection slides},
    author = {Zhu, Mengdan and Ren, Bing and Richards, Ryland and Suriawinata, Matthew and Tomita, Naofumi and Hassanpour, Saeed},
    journal = {Scientific Reports},
    volume = {11},
    number = {1},
    pages = {7080},
    year = {2021},
    publisher = {Nature Publishing Group UK London},
    doi = {10.1038/s41598-021-86747-7}
}
```

---


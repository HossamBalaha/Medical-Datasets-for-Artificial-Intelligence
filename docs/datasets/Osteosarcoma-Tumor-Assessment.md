### 🦴 Osteosarcoma Tumor Assessment

**Study**: Leavey, P., Sengupta, A., Rakheja, D., Daescu, O., Arunachalam, H. B., & Mishra, R. (2019). Osteosarcoma data
from UT Southwestern/UT Dallas for Viable and Necrotic Tumor Assessment. The Cancer Imaging Archive (TCIA).
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                        |
|-------------------------|--------------------------------------------------------------------------------|
| **📛 Title**            | Osteosarcoma-Tumor-Assessment                                                  |
| **🔗 Source**           | https://www.cancerimagingarchive.net/collection/osteosarcoma-tumor-assessment/ |
| **🦴 Target Organ**     | Bone (Appendicular and axial skeleton)                                         |
| **📅 Last Accessed**    | August 13, 2026                                                                |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                                                  |
| **📐 Image Size**       | 1024 × 1024 pixels (at 10X resolution)                                         |
| **📁 Data Format**      | JPEG (.jpg) for images, CSV (.csv) for machine learning features               |
| **👥 Demographics**     | ❌ Not included (4 patients selected from 50 archival samples)                  |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                         |

#### 📊 Dataset Composition

| Category                | Details                                                  |
|-------------------------|----------------------------------------------------------|
| **🖼️ Total Images**    | 1,144 histopathological image tiles                      |
| **🏥 Imaging Modality** | Brightfield histopathology (Hematoxylin & Eosin stained) |
| **📦 Total Size**       | ~196.84 MB                                               |
| **🏥 Source**           | University of Texas Southwestern Medical Center, Dallas  |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of osteosarcoma tissue viability
- **Number of Classes**: 3️⃣
    - ✅ Non-Tumor (536 images, 47%)
    - ⚫ Necrotic Tumor (263 images, 23%)
    - 🔴 Viable Tumor (345 images, 30%)

#### 💡 Usage Notes

- ✅ Annotated by two board-certified medical experts based on the diversity of tumor specimens post-surgical resection.
- ✅ Includes a companion CSV file (`ML_Features_1144.csv`) containing 65 pre-extracted machine learning features per
  tile.
- ✅ Explicitly designed for benchmarking convolutional neural networks on viable vs. necrotic tumor discrimination.
- 📚 Required to cite the original TCIA collection and associated publications.
- 🔐 License: CC BY 3.0

#### ⚠️ Usage Considerations

| Aspect                    | Recommendation                                                                                            |
|---------------------------|-----------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**    | Non-tumor images dominate the dataset; consider class-weighted loss or stratified sampling.               |
| **📐 Resolution**         | Fixed at 1024x1024; resize to model-compatible dimensions (e.g., 224x224) if needed.                      |
| **🧪 Data Leakage**       | Tiles originate from only 4 unique patients; implement strict patient-aware splitting to prevent leakage. |
| **🔐 Ethical Compliance** | Dataset contains patient-derived archival data; adhere to institutional review requirements.              |

#### 💡 Suggested Preprocessing Pipeline

1. **Parse metadata**: Load `ML_Features_1144.csv` to map image filenames to ground-truth labels and pre-extracted
   features.
2. **Standardize input**: Resize images to a uniform dimension while preserving the aspect ratio.
3. **Color normalization**: Apply stain normalization (e.g., Macenko method) to mitigate H&E inter-slide variability.
4. **Augmentation**: Incorporate rotation, flipping, and intensity jittering to improve generalization on the small
   patient cohort.
5. **Stratified evaluation**: Report per-class precision, recall, and F1-score, alongside a confusion matrix.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{leavey2019osteosarcoma,
  author = {Leavey, P. and Sengupta, A. and Rakheja, D. and Daescu, O. and Arunachalam, H. B. and Mishra, R.},
  title = {Osteosarcoma data from UT Southwestern/UT Dallas for Viable and Necrotic Tumor Assessment (Osteosarcoma-Tumor-Assessment)},
  year = {2019},
  publisher = {The Cancer Imaging Archive},
  doi = {10.7937/tcia.2019.bvhjhdas},
  url = {https://www.cancerimagingarchive.net/collection/osteosarcoma-tumor-assessment/}
}
```

---

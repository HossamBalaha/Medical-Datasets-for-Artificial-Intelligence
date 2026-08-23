### 🫁 Chest Xray Masks and Labels

**Study**: Jaeger, S., et al. (2014). Automatic tuberculosis screening using chest radiographs. *IEEE Trans Med
Imaging*, 33(2), 233-45. & Candemir, S., et al. (2014). Lung segmentation in chest radiographs using anatomical atlases.
*IEEE Trans Med Imaging*, 33(2), 577-90.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                     |
|-------------------------|-----------------------------------------------------------------------------|
| **📛 Title**            | Chest Xray Masks and Labels                                                 |
| **🔗 Source**           | https://www.kaggle.com/datasets/nikhilpandey360/chest-xray-masks-and-labels |
| **🫁 Target Organ**     | Lungs / Chest                                                               |
| **📅 Last Accessed**    | August 21, 2026                                                             |
| **🎯 Supported Tasks**  | 🎭 Segmentation, 🏷️ Classification                                         |
| **📐 Image Size**       | Variable (DICOM converted to PNG)                                           |
| **📁 Data Format**      | PNG (images and masks), Text files (clinical readings)                      |
| **👥 Demographics**     | ❌ Not explicitly detailed (de-identified)                                   |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                      |

#### 📊 Dataset Composition

| Category                   | Details                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| **🖼️ Total Images**       | 800 chest X-rays (Montgomery County: 138, Shenzhen: 662)                          |
| **🎭 Total Masks**         | 704 pixel-level lung segmentation masks                                           |
| **🏥 Imaging Modality**    | Radiographic X-ray (Posterior-Anterior)                                           |
| **📦 Total Size**          | ~5.41 GB                                                                          |
| **🏥 Source Institutions** | Montgomery County Dept. of Health (USA) & Shenzhen No.3 People’s Hospital (China) |

#### 🎭 Segmentation & Classification Task Details

- **Segmentation Task**: Binary semantic segmentation of the lung fields from the background and mediastinum.
- **Classification Task**: Binary classification of Tuberculosis (TB) manifestations (e.g., effusions, miliary patterns)
  vs. Normal.
- **Annotation Targets**: Expert-drawn lung masks and radiology readings for disease presence.

#### 💡 Usage Notes

- ✅ Highly valuable for benchmarking lung segmentation algorithms (e.g., U-Net) as a preprocessing step for downstream
  disease classification.
- ✅ Combines two distinct, well-known public datasets (Montgomery and Shenzhen), offering diversity in imaging protocols
  and patient populations.
- ✅ Includes clinical text readings, enabling research into multi-modal (image + text) diagnostic models.
- 📚 Required to cite the original IEEE publications when using this dataset.
- 🔐 License: CC0: Public Domain

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                                    |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Missing Masks**       | Not all 800 images have corresponding masks (only 704 provided); cross-reference filenames before training segmentation models.   |
| **📦 Data Heterogeneity**  | Sourced from two different countries with varying X-ray equipment; consider domain adaptation or stratified evaluation by source. |
| **🧪 Validation Strategy** | Implement patient-aware or source-aware partitioning to prevent data leakage and ensure robust generalization.                    |

#### 💡 Suggested Preprocessing Pipeline

1. **Cross-reference files**: Map image filenames to their corresponding mask files and clinical reading texts,
   discarding unmatched pairs if necessary.
2. **Standardize geometry**: Resize images and masks to a uniform dimension (e.g., 256x256 or 512x512), ensuring masks
   are resized with nearest-neighbor interpolation to preserve binary integrity.
3. **Apply intensity normalization**: Scale image pixel values to [0, 1] or standardize using dataset-wide statistics.
4. **Augmentation **(training only): Apply synchronized geometric transformations (rotation, flipping) to both images
   and masks; apply photometric jittering only to images.
5. **Stratified evaluation**: Report Dice coefficient and Intersection over Union (IoU) for segmentation, and AUC-ROC
   for TB classification.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{jaeger2014automatic,
  title={Automatic tuberculosis screening using chest radiographs},
  author={Jaeger, Stefan and Karargyris, Alexandros and Candemir, Sema and Folio, Les and Siegelman, Jonathan and Callaghan, Fiona and Xue, Zhiyun and Palaniappan, Kannappan and Singh, Rahul K and Antani, Sameer and others},
  journal={IEEE transactions on medical imaging},
  volume={33},
  number={2},
  pages={233--245},
  year={2014},
  publisher={IEEE},
  doi={10.1109/TMI.2013.2284099}
}
```

---

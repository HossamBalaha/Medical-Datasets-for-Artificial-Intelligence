### 🫁 Tuberculosis (TB) Chest X-ray Database

**Study**: Rahman, T., Khandakar, A., Kadir, M. A., Islam, K. R., Islam, K. F., Mahbub, Z. B., Ayari, M. A., &
Chowdhury, M. E. H. (2020). Reliable Tuberculosis Detection using Chest X-ray with Deep Learning, Segmentation and
Visualization. *IEEE Access*, 8, 191586-191601.
[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                           |
|-------------------------|-----------------------------------------------------------------------------------|
| **📛 Title**            | Tuberculosis (TB) Chest X-ray Database                                            |
| **🔗 Source**           | https://www.kaggle.com/datasets/tawsifurrahman/tuberculosis-tb-chest-xray-dataset |
| **🫁 Target Organ**     | Lungs / Chest                                                                     |
| **📅 Last Accessed**    | June 24, 2026                                                                     |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification                                                         |
| **📐 Image Size**       | Variable (Chest X-rays)                                                           |
| **📁 Data Format**      | Images (folders), metadata.xlsx                                                   |
| **👥 Demographics**     | ❌ Not included                                                                    |
| **🔄 Train/Test Split** | ❌ Not provided (700 public TB, 2800 NIAID TB, 3500 Normal)                        |

#### 📊 Dataset Composition

| Category                | Details                                                                            |
|-------------------------|------------------------------------------------------------------------------------|
| **🖼️ Total Images**    | 4,200 publicly accessible chest X-rays                                             |
| **🏥 Imaging Modality** | Radiographic X-ray (Frontal)                                                       |
| **🎨 Color Format**     | Grayscale / RGB (scan-dependent)                                                   |
| **📦 Sources**          | NLM (Montgomery, Shenzhen), Belarus Set, NIAID TB Portal, RSNA Pneumonia Challenge |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification (Tuberculosis vs. Normal)
- **Number of Classes**: 2️⃣
- 🫁 Tuberculosis
- ✅ Normal

**📊 Dataset Distribution**:

| Class           | Image Count | Notes                                                         |
|-----------------|-------------|---------------------------------------------------------------|
| ✅ Normal        | 3,500       | Aggregated from multiple sources                              |
| 🫁 Tuberculosis | 700         | Publicly accessible; 2,800 more available via NIAID agreement |
| **Total**       | **4,200**   | —                                                             |

#### 💡 Usage Notes

- ✅ Largest publicly available TB Chest X-ray database for benchmarking deep learning models
- ✅ Aggregated from multiple global institutions (NLM, Belarus, NIAID, RSNA) supports domain generalization studies
- ✅ Includes metadata files for image references and provenance tracking
- 📚 Required to cite the original *IEEE Access* publication when using this dataset
- 🔐 Data files © Original Authors; verify specific terms for each constituent source

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**     | Severe imbalance (3500 Normal vs. 700 TB); apply class-weighted loss or oversampling                       |
| **📦 Data Heterogeneity**  | Sourced from multiple databases with varying resolutions and protocols; consider domain adaptation         |
| **🔐 Licensing**           | Aggregated dataset; ensure compliance with individual source licenses (e.g., NIAID data-sharing agreement) |
| **🧪 Validation Strategy** | No predefined split; implement patient-aware or source-aware partitioning to prevent data leakage          |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Utilize framework-native utilities to ingest the `Normal` and `Tuberculosis`
   subfolders.
2. **Standardize input format**: Convert all images to a consistent color space (single-channel grayscale) and fixed
   resolution (e.g., 224x224 or 256x256).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
4. **Augmentation **(training only): Incorporate rotation, flipping, and intensity jittering to improve model
   generalization.
5. **Stratified evaluation**: Report per-class metrics (precision, recall, F1-score, AUC-ROC) to assess performance
   given the class imbalance.

#### 🔗 Associated Resources

- **Kaggle Repository**: https://www.kaggle.com/datasets/tawsifurrahman/tuberculosis-tb-chest-xray-dataset
- **NIAID TB Portal**: https://tbportals.niaid.nih.gov/download-data (for additional 2,800 TB images)
- **Related Publications**: Rahman et al., "Reliable Tuberculosis Detection using Chest X-ray with Deep Learning,
  Segmentation and Visualization," *IEEE Access*, 2020.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{rahman2020reliable,
  title={Reliable tuberculosis detection using chest X-ray with deep learning, segmentation and visualization},
  author={Rahman, Tawsifur and Khandakar, Amith and Kadir, Muhammad Abdul and Islam, Khandaker Rejaul and Islam, Khandakar F and Mazhar, Rashid and Hamid, Tahir and Islam, Mohammad Tariqul and Kashem, Saad and Mahbub, Zaid Bin and others},
  journal={Ieee Access},
  volume={8},
  pages={191586--191601},
  year={2020},
  publisher={IEEE}
}
```

---


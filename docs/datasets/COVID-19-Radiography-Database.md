### 🫁 COVID-19 Radiography Database

**Study**: Chowdhury, M. E. H., Rahman, T., Khandakar, A., Mazhar, R., Kadir, M. A., Mahbub, Z. B., ... & Islam, M. T. (
2020). Can AI help in screening Viral and COVID-19 pneumonia?. *IEEE Access*, 8, 132665-132676.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                     |
|-------------------------|-----------------------------------------------------------------------------|
| **📛 Title**            | COVID-19 Radiography Database                                               |
| **🔗 Source**           | https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database |
| **🫁 Target Organ**     | Lungs / Chest                                                               |
| **📅 Last Accessed**    | June 26, 2026                                                               |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification, 🎭 Segmentation                              |
| **📐 Image Size**       | 299 × 299 pixels (fixed)                                                    |
| **📁 Data Format**      | PNG (.png) for images and masks, XLSX (.xlsx) for metadata                  |
| **👥 Demographics**     | ❌ Not included (de-identified)                                              |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                      |

#### 📊 Dataset Composition

| Category                   | Details                                                  |
|----------------------------|----------------------------------------------------------|
| **🖼️ Total Images**       | 21,165 chest X-ray images                                |
| **🏥 Imaging Modality**    | Radiographic X-ray                                       |
| **🎨 Color Format**        | PNG (Grayscale / RGB)                                    |
| **🏥 Source Institutions** | Qatar University, University of Dhaka, and collaborators |
| **📦 Total Size**          | ~806.84 MB                                               |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of lung conditions
- **Number of Classes**: 4️⃣
- 🦠 COVID-19
- 🫁 Lung Opacity (Non-COVID lung infection)
- ✅ Normal
- 🦠 Viral Pneumonia

**📊 Dataset Distribution**:

| Class              | Image Count | Description                                 |
|--------------------|-------------|---------------------------------------------|
| 🦠 COVID-19        | 3,616       | Positive cases of SARS-CoV-2 infection      |
| ✅ Normal           | 10,192      | Healthy lung scans                          |
| 🫁 Lung Opacity    | 6,012       | Non-COVID lung infections (e.g., bacterial) |
| 🦠 Viral Pneumonia | 1,345       | Viral pneumonia cases                       |
| **Total**          | **21,165**  | —                                           |

#### 🎭 Segmentation Task Details

- **Task Type**: Binary semantic segmentation of lung regions
- **Annotation Targets**: Ground-truth lung segmentation masks for the entire dataset
- **Format**: PNG masks corresponding to the chest X-ray images

#### 💡 Usage Notes

- ✅ Suitable for benchmarking deep learning models for COVID-19 and pneumonia detection
- ✅ Includes ground-truth lung segmentation masks for joint classification and segmentation tasks
- ✅ Winner of the COVID-19 Dataset Award by the Kaggle Community
- ✅ Fixed 299×299 resolution simplifies preprocessing for standard CNN architectures
- 📚 Required to cite the original *IEEE Access* publications when using this dataset

#### ⚠️ Usage Considerations

| Aspect                       | Recommendation                                                                                               |
|------------------------------|--------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**       | Normal class heavily dominates; apply class-weighted loss, focal loss, or undersampling                      |
| **🧪 Multi-Class Nature**    | Distinguishing between COVID-19, Viral Pneumonia, and other Lung Opacities requires careful feature learning |
| **📐 Resolution**            | Images are fixed at 299×299; ensure model input layers match or resize accordingly                           |
| **🔐 Licensing**             | Data files © Original Authors; verify specific terms for commercial or clinical deployment                   |
| **🧭 Domain Generalization** | Aggregated from multiple global sources; validate on external cohorts for clinical deployment                |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Utilize framework-native utilities to ingest the `COVID`, `Lung_Opacity`, `Normal`, and
   `Viral Pneumonia` subfolders.
2. **Standardize input format**: Confirm uniform 299×299 dimensions; convert to single-channel grayscale if desired.
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
4. **Load segmentation masks**: Align lung mask PNGs with their corresponding X-ray images for segmentation tasks.
5. **Augmentation **(training only): Incorporate rotation, flipping, and intensity jittering to improve model
   generalization.
6. **Stratified evaluation**: Report per-class precision, recall, F1-score, and AUC-ROC to assess performance given the
   class imbalance.

#### 🔗 Associated Resources

- **Kaggle Repository**: https://www.kaggle.com/datasets/tawsifurrahman/covid19-radiography-database
- **Related Dataset**: COVID-QU-Ex Dataset (33,920 images with lung masks)
- **Related Publications**:
    - Chowdhury, M. E. H., et al. (2020). "Can AI help in screening Viral and COVID-19 pneumonia?" *IEEE Access*.
    - Rahman, T., et al. (2020). "Exploring the Effect of Image Enhancement Techniques on COVID-19 Detection using Chest
      X-ray Images."

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{chowdhury2020can,
  title={Can AI help in screening viral and COVID-19 pneumonia?},
  author={Chowdhury, Muhammad EH and Rahman, Tawsifur and Khandakar, Amith and Mazhar, Rashid and Kadir, Muhammad Abdul and Mahbub, Zaid Bin and Islam, Khandakar Reajul and Khan, Muhammad Salman and Iqbal, Atif and Al Emadi, Nasser and others},
  journal={Ieee Access},
  volume={8},
  pages={132665--132676},
  year={2020},
  publisher={IEEE}
}
@article{rahman2021exploring,
  title={Exploring the effect of image enhancement techniques on COVID-19 detection using chest X-ray images},
  author={Rahman, Tawsifur and Khandakar, Amith and Qiblawey, Yazan and Tahir, Anas and Kiranyaz, Serkan and Kashem, Saad Bin Abul and Islam, Mohammad Tariqul and Al Maadeed, Somaya and Zughaier, Susu M and Khan, Muhammad Salman and others},
  journal={Computers in biology and medicine},
  volume={132},
  pages={104319},
  year={2021},
  publisher={Elsevier}
}
```

--- 


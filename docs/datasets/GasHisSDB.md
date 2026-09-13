### 🩺 GasHisSDB: Gastric Histopathology Sub-size Image Database

**Study**: MIaMIA Group. (2021). GasHisSDB. Figshare.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                   |
|-------------------------|-----------------------------------------------------------|
| **📛 Title**            | GasHisSDB: Gastric Histopathology Sub-size Image Database |
| **🔗 Source**           | https://figshare.com/articles/dataset/GasHisSDB/15066147  |
| **🩺 Target Organ**     | Gastrointestinal Tract (Stomach)                          |
| **📅 Last Accessed**    | September 11, 2026                                        |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                             |
| **📐 Image Size**       | 160×160, 120×120, and 80×80 pixels (sub-size patches)     |
| **📁 Data Format**      | Image patches (RAR archive)                               |
| **👥 Demographics**     | ❌ Not included                                            |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)    |

#### 📊 Dataset Composition

| Category                | Details                                                 |
|-------------------------|---------------------------------------------------------|
| **🖼️ Total Images**    | 245,196 histopathological image patches                 |
| **🔬 Imaging Modality** | Brightfield histopathology (H&E stained gastric tissue) |
| **📦 Total Size**       | ~4.08 GB (compressed)                                   |
| **🏥 Source**           | MIaMIA Group                                            |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of gastric histopathology sub-size images
- **Number of Classes**: Multiple (designed to evaluate discrepancies among different image classification methods)
- **Patch Variants**: The dataset is explicitly divided into three sub-databases based on resolution: 160×160 pixels,
  120×120 pixels, and 80×80 pixels.

#### 💡 Usage Notes

- ✅ Specifically designed to evaluate and benchmark a variety of image classification methods, from classical machine
  learning to modern CNNs and Transformer-based classifiers.
- ✅ The multi-resolution sub-database structure enables research on the impact of image scale and resolution on
  classification performance.
- 📚 Required to cite the original Figshare repository when using this dataset.
- 🔐 License: CC BY 4.0

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                      |
|----------------------------|-----------------------------------------------------------------------------------------------------|
| **📐 Resolution Variance** | Choose the specific sub-database (160x, 120x, or 80x) that matches your model's input requirements. |
| **🧪 Validation Strategy** | No predefined split; implement patient-aware or slide-aware partitioning to prevent data leakage.   |
| **🔍 Class Balance**       | Verify the distribution of classes within the chosen resolution subset before training.             |

#### 💡 Suggested Preprocessing Pipeline

1. **Extract archive**: Unzip the `GasHisSDB.rar` file and select the desired resolution sub-folder.
2. **Organize directory structure**: Arrange images into class-labeled subfolders for framework-native data loading.
3. **Standardize input**: Confirm uniform dimensions; resize if your specific architecture requires a different input
   size.
4. **Color normalization**: Apply stain normalization (e.g., Macenko method) to mitigate inter-slide H&E staining
   variability.
5. **Augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering to improve
   generalization.
6. **Stratified evaluation**: Report per-class precision, recall, F1-score, and confusion matrices.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{miamia2021gashissdb,
  author = {{MIaMIA Group}},
  title = {GasHisSDB},
  year = {2021},
  publisher = {Figshare},
  doi = {10.6084/m9.figshare.15066147},
  url = {https://figshare.com/articles/dataset/GasHisSDB/15066147}
}
```

---

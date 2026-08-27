### 🫀 Liver Histopathology (Fibrosis) Ultrasound Images

**Study**: Joo, Y., et al. (2023). Classification of Liver Fibrosis From Heterogeneous Ultrasound Image. IEEE Access.  
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                                        |
|-------------------------|------------------------------------------------------------------------------------------------|
| **📛 Title**            | Liver Histopathology (Fibrosis) Ultrasound Images                                              |
| **🔗 Source**           | https://www.kaggle.com/datasets/vibhingupta028/liver-histopathology-fibrosis-ultrasound-images |
| **🫁 Target Organ**     | Liver                                                                                          |
| **📅 Last Accessed**    | August 27, 2026                                                                                |
| **🎯 Supported Tasks**  | 🏷️ Multi-class Classification (Fibrosis Staging)                                              |
| **📐 Image Size**       | Variable (High-Resolution Ultrasound)                                                          |
| **📁 Data Format**      | JPEG (.jpg)                                                                                    |
| **👥 Demographics**     | ❌ Not explicitly detailed in public metadata                                                   |
| **🔄 Train/Test Split** | ✅ Implicitly provided (Seoul St. Mary’s for train/val, Eunpyeong for test)                     |

#### 📊 Dataset Composition

| Category                | Details                                                   |
|-------------------------|-----------------------------------------------------------|
| **🖼️ Total Images**    | 6,323 files                                               |
| **🏥 Imaging Modality** | Medical Ultrasound (Abdominal US)                         |
| **📦 Total Size**       | ~1.89 GB                                                  |
| **🏥 Source**           | Seoul St. Mary’s Hospital & Eunpyeong St. Mary’s Hospital |

#### 🏷️ Classification Task Details

- **Task Type**: Multi-class ordinal classification (METAVIR scoring system)
- **Number of Classes**: 5️⃣
    - ✅ **F0 (No Fibrosis)**: 2,114 images (Healthy liver tissue, no scarring)
    - 🟡 **F1 (Portal Fibrosis)**: 861 images (Scar tissue around portal veins)
    - 🟠 **F2 (Periportal Fibrosis)**: 793 images (Scarring around liver boundary regions)
    - 🔴 **F3 (Septal Fibrosis)**: 857 images (Thickened scar tissue forming bands/septa)
    - 🟣 **F4 (Cirrhosis)**: 1,698 images (Advanced fibrosis, extensive scarring, loss of function)

#### 💡 Usage Notes

- ✅ Provides a real-world clinical distribution where F0 and F4 are more prevalent than early-stage fibrosis (F1-F3).
- ✅ Sourced from two different hospitals, offering a natural domain shift for robust generalization testing.
- 📚 Recommended to cite the original IEEE Access publication.
- 🔐 License: Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0).

#### ⚠️ Usage Considerations

| Aspect                      | Recommendation                                                                                                                                                               |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**      | F1, F2, and F3 are underrepresented (~13% each). Consider using focal loss, class weighting, or targeted oversampling to prevent model bias toward F0 and F4.                |
| **📐 Ultrasound Artifacts** | US images inherently contain speckle noise and shadowing. Models must learn to be robust to these artifacts rather than overfitting to machine-specific noise patterns.      |
| **🧪 Validation Strategy**  | Leverage the hospital split: train/validate on Seoul St. Mary’s data and hold out Eunpyeong St. Mary’s data strictly for final testing to evaluate cross-domain performance. |

#### 💡 Suggested Preprocessing Pipeline

1. **Exploratory Analysis**: Visually inspect the speckle noise patterns and contrast levels across the different
   METAVIR classes.
2. **Standardize input format**: Resize all images to a uniform dimension (e.g., 224x224 or 256x256) and convert to
   grayscale or 3-channel RGB as required by the backbone network.
3. **Noise Reduction (Optional)**: Apply mild speckle noise reduction filters (e.g., Median or Anisotropic Diffusion) if
   the baseline model struggles with ultrasound artifacts.
4. **Intensity Normalization**: Scale pixel values to [0, 1] or apply Contrast Limited Adaptive Histogram Equalization (
   CLAHE) to enhance tissue boundary visibility.
5. **Stratified Splitting**: If not using the hospital split, ensure stratified k-fold cross-validation to maintain the
   imbalanced class distribution across all folds.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{joo2023classification,
  author={Joo, Y. and Park, H. -C. and Lee, O. -J. and Yoon, C. and Choi, M. H. and Choi, C.},
  journal={IEEE Access}, 
  title={Classification of Liver Fibrosis From Heterogeneous Ultrasound Image}, 
  year={2023},
  volume={11},
  pages={9920-9930},
  doi={10.1109/ACCESS.2023.3240000}
}
```

---

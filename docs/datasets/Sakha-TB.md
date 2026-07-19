### 🫁 Sakha-TB

**Study**: Pchelintsev, Ya, Khvostikov, A, Buchatskaia, O, Nikiforova, N, Shepeleva, L, Prokopev, E, Parolina, L, &
Krylov, A. (2022). Robustness Analysis of Chest X-Ray Computer Tuberculosis Diagnosis. *Computational Mathematics and
Modeling*, 33(4), 472-486.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                   |
|-------------------------|---------------------------------------------------------------------------|
| **📛 Title**            | Sakha-TB                                                                  |
| **🔗 Source**           | https://imaging.cs.msu.ru/en/research/TB/Sakha-TB                         |
| **🫁 Target Organ**     | Lungs / Chest                                                             |
| **📅 Last Accessed**    | June 24, 2026                                                             |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification                                                 |
| **📐 Image Size**       | Variable (16-bit and 8-bit PNG)                                           |
| **📁 Data Format**      | PNG (Full: DICOM converted; Compressed: cropped, downsampled, normalized) |
| **👥 Demographics**     | ✅ Balanced by age and gender (to some extent)                             |
| **🔄 Train/Test Split** | ❌ Not provided (400 Normal, 400 TB)                                       |

#### 📊 Dataset Composition

| Category                | Details                                                                                                                                              |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| **🖼️ Total Images**    | 800 frontal chest X-rays                                                                                                                             |
| **🏥 Imaging Modality** | Radiographic X-ray (Frontal)                                                                                                                         |
| **🎨 Color Format**     | Grayscale (16-bit and 8-bit)                                                                                                                         |
| **📦 Variants**         | • Full version (8.73 GB): DICOM converted to PNG with bit depth preserved<br>• Compressed version (0.27 GB): Cropped, downsampled, normalized, 8-bit |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification (Tuberculosis vs. Normal)
- **Number of Classes**: 2️⃣
- 🫁 Tuberculosis
- ✅ Normal

**📊 Dataset Distribution**:
| Class | Image Count |
|---|---|
| ✅ Normal | 400 |
| 🫁 Tuberculosis | 400 |
| **Total** | **800** |

#### 💡 Usage Notes

- ✅ Suitable for benchmarking deep learning models for TB screening from chest X-rays
- ✅ Includes both full-resolution (16-bit) and compressed (8-bit) variants for different computational constraints
- ✅ Balanced class distribution supports stable training without aggressive resampling
- 📚 Required to cite the original *Computational Mathematics and Modeling* publication when using this dataset
- 🔐 Distributed under Creative Commons Attribution 4.0 International license

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                            |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| **📦 Data Format**         | Full version requires handling 16-bit PNGs; ensure libraries support high bit-depth                       |
| **🔍 Class Balance**       | Perfectly balanced (1:1 ratio); standard cross-entropy is sufficient                                      |
| **📐 Resolution Variance** | Compressed version is downsampled; verify if resolution is sufficient for fine-grained feature extraction |
| **🔐 Licensing**           | CC BY 4.0; attribution required for redistribution or adaptation                                          |

#### 💡 Suggested Preprocessing Pipeline

1. **Select variant**: Choose the full version (16-bit) for maximum detail or the compressed version (8-bit) for faster
   iteration.
2. **Standardize input format**: Convert all images to a consistent color space (single-channel grayscale) and fixed
   resolution (e.g., 224x224 or 512x512).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
4. **Augmentation **(training only): Incorporate rotation, flipping, and intensity jittering to improve model
   generalization.
5. **Stratified evaluation**: Report per-class metrics (precision, recall, F1-score, AUC-ROC) to assess diagnostic
   performance.

#### 🔗 Associated Resources

- **Full Version Download**: OneDrive | Yandex Disk (8.73 GB)
- **Compressed Version Download**: OneDrive | Yandex Disk (0.27 GB)
- **Institutional Affiliation**: Laboratory of Mathematical Methods of Image Processing, Lomonosov Moscow State
  University

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{pchelintsev2022robustness,
  title={Robustness Analysis of Chest X-Ray Computer Tuberculosis Diagnosis},
  author={Pchelintsev, Ya and Khvostikov, A and Buchatskaia, O and Nikiforova, N and Shepeleva, L and Prokopev, E and Parolina, L and Krylov, A},
  journal={Computational Mathematics and Modeling},
  volume={33},
  number={4},
  pages={472--486},
  year={2022},
  publisher={Springer}
}
```

---


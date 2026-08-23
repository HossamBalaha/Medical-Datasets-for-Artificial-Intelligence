### 🩹 UWM Wound Classification (Images & Locations)

**Study**: Patel, Y., Shah, T., Dhar, M. K., Zhang, T., Niezgoda, J., Gopalakrishnan, S., & Yu, Z. (2024). Integrated
image and location analysis for wound classification: a deep learning approach. *Scientific Reports*, 14(1).
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                         |
|-------------------------|---------------------------------------------------------------------------------|
| **📛 Title**            | Wound classification using images and locations                                 |
| **🔗 Source**           | https://github.com/uwm-bigdata/wound-classification-using-images-and-locations/ |
| **🖼️ Target Organ**    | Skin                                                                            |
| **📅 Last Accessed**    | August 14, 2026                                                                 |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                                                   |
| **📐 Image Size**       | Variable (Width: 320-700px, Height: 240-525px)                                  |
| **📁 Data Format**      | JPEG (.jpg) for images, custom body map for locations                           |
| **👥 Demographics**     | ❌ Not included (de-identified clinical images)                                  |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                          |

#### 📊 Dataset Composition

| Category                | Details                                             |
|-------------------------|-----------------------------------------------------|
| **🖼️ Total Images**    | 730 wound images                                    |
| **🏥 Imaging Modality** | Clinical Photography (iPad Pro, Canon SX 620 HS)    |
| **📦 Total Size**       | Variable                                            |
| **🏥 Source**           | AZH Wound and Vascular Center, Milwaukee, Wisconsin |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of wound types using integrated image and location analysis
- **Number of Classes**: 4️⃣
    - 🩸 Venous
    - 🍬 Diabetic
    - 🛏️ Pressure
    - 🔪 Surgical

#### 💡 Usage Notes

- ✅ Unique multi-modal dataset combining wound images with detailed anatomical location information.
- ✅ Wound ROIs are cropped using a developed localizer, and locations are annotated by wound professionals using a
  custom body map.
- ✅ Captured over a two-year clinical period, providing realistic clinical variance.
- 📚 Required to cite the original *Scientific Reports* publications when using this dataset.
- 🔐 License: Check repository for specific terms (typically academic/research use).

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                                                               |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Patient Overlap**     | Most images are from separate patients, but some contain multiple photos from the same patient at different sites/stages. Implement patient-aware splitting. |
| **📐 Resolution Variance** | Images vary in dimensions; apply uniform resizing and padding prior to training.                                                                             |
| **🧪 Multi-modal Input**   | Models should ideally leverage both the image features and the location metadata for optimal performance.                                                    |

#### 💡 Suggested Preprocessing Pipeline

1. **Load metadata**: Parse location annotations and map them to the corresponding image files.
2. **Standardize input format**: Resize images to a fixed resolution (e.g., 224x224 or 256x256).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide statistics.
4. **Augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering.
5. **Stratified evaluation**: Report per-class precision, recall, and F1-score, alongside multi-modal fusion metrics.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{patel2024integrated,
  title={Integrated image and location analysis for wound classification: a deep learning approach},
  author={Patel, Y and Shah, T and Dhar, Mrinal Kanti and Zhang, T and Niezgoda, J and Gopalakrishnan, S and Yu, Z},
  journal={Scientific Reports},
  volume={14},
  number={1},
  year={2024},
  publisher={Nature Publishing Group},
  doi={10.1038/s41598-024-56626-w}
}
```

---

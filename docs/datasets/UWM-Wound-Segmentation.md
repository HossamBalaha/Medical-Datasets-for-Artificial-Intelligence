### 🩹 UWM Wound Segmentation

**Study**: Wang, C., Anisuzzaman, D. M., Williamson, V., Dhar, M. K., Rostami, B., Niezgoda, J., Gopalakrishnan, S., &
Yu, Z. (2020). Fully Automatic Wound Segmentation with Deep Convolutional Neural Networks. *Scientific Reports*, 
10:21897.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                |
|-------------------------|--------------------------------------------------------|
| **📛 Title**            | UWM Wound Segmentation                                 |
| **🔗 Source**           | https://github.com/uwm-bigdata/wound-segmentation/     |
| **🖼️ Target Organ**    | Skin                                                   |
| **📅 Last Accessed**    | August 14, 2026                                        |
| **🎯 Supported Tasks**  | 🎭 Semantic Segmentation                               |
| **📐 Image Size**       | Variable (cropped and zero-padded natural images)      |
| **📁 Data Format**      | JPEG/PNG (images), JSON/Mask (segmentation)            |
| **👥 Demographics**     | ❌ Not included (de-identified clinical images)         |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended) |

#### 📊 Dataset Composition

| Category                | Details                                                            |
|-------------------------|--------------------------------------------------------------------|
| **🖼️ Total Images**    | Variable (built by UWM lab and AZH Wound and Vascular Center)      |
| **🏥 Imaging Modality** | Clinical Photography (natural images in clinical settings)         |
| **📦 Total Size**       | Variable                                                           |
| **🏥 Source**           | Advancing the Zenith of Healthcare (AZH) Wound and Vascular Center |

#### 🎭 Segmentation Task Details

- **Task Type**: Binary semantic segmentation of wound areas
- **Annotation Targets**: Wound region vs. background
- **Annotation Protocol**: Fully annotated by wound professionals and preprocessed with cropping and zero-padding.

#### 💡 Usage Notes

- ✅ Suitable for benchmarking deep learning models (U-Net, MobileNetV2, Mask-RCNN, SegNet, VGG16) for wound area
  segmentation.
- ✅ Preprocessed with cropping and zero-padding to standardize input for clinical setting images.
- ✅ Expert-annotated by wound care professionals ensuring high label reliability.
- 📚 Required to cite the original *Scientific Reports* publication when using this dataset.
- 🔐 License: Check repository for specific terms (typically academic/research use).

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------|
| **📐 Resolution Variance** | Natural images vary in resolution; apply uniform resizing prior to model ingestion.         |
| **🧪 Domain Specificity**  | Captured in clinical settings; models may require domain adaptation for in-the-wild images. |
| **🔐 Ethical Compliance**  | Dataset contains de-identified patient images; adhere to institutional review requirements. |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Ingest images and corresponding segmentation masks.
2. **Standardize input format**: Resize images and masks to a consistent dimension (e.g., 256x256 or 512x512).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide statistics.
4. **Augmentation **(training only): Incorporate rotation, flipping, and color jittering to simulate varied clinical
   lighting.
5. **Stratified evaluation**: Report Dice coefficient and Intersection over Union (IoU) for segmentation performance.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{wang2020fully,
  title={Fully Automatic Wound Segmentation with Deep Convolutional Neural Networks},
  author={Wang, C and Anisuzzaman, DM and Williamson, V and Dhar, MK and Rostami, B and Niezgoda, J and Gopalakrishnan, S and Yu, Z},
  journal={Scientific Reports},
  volume={10},
  pages={21897},
  year={2020},
  publisher={Nature Publishing Group},
  doi={10.1038/s41598-020-78799-w}
}
```

---

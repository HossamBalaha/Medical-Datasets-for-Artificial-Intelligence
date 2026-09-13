### 🫁🫀 Chest CT Images and Segmentation Masks Dataset

**Study**: Rahul T. (2026). Chest CT Images and Segmentation Masks Dataset. Kaggle.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                                   |
|-------------------------|-------------------------------------------------------------------------------------------|
| **📛 Title**            | Chest CT Images and Segmentation Masks Dataset                                            |
| **🔗 Source**           | https://www.kaggle.com/datasets/rahult1999/chest-ct-images-and-segmentation-masks-dataset |
| **🫁🫀 Target Organ**   | Lungs / Heart (Cardiac/Chest region)                                                      |
| **📅 Last Accessed**    | September 11, 2026                                                                        |
| **🎯 Supported Tasks**  | 🎭 Semantic Segmentation                                                                  |
| **📐 Image Size**       | Variable (CT slices)                                                                      |
| **📁 Data Format**      | Images and corresponding pixel-level segmentation masks                                   |
| **👥 Demographics**     | ❌ Not included                                                                            |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                                    |

#### 📊 Dataset Composition

| Category                | Details                                    |
|-------------------------|--------------------------------------------|
| **🖼️ Total Images**    | ~28,800 files (14.4k images + 14.4k masks) |
| **🔬 Imaging Modality** | Computed Tomography (CT)                   |
| **📦 Total Size**       | ~3.64 GB (compressed)                      |
| **🏥 Source**           | Aggregated medical imaging sources         |

#### 🎭 Segmentation Task Details

- **Task Type**: Binary/Multi-class semantic segmentation of cardiac/chest anatomical regions
- **Annotation Targets**: Pixel-level ground-truth masks identifying target anatomical structures (e.g., heart, lungs)
  from surrounding tissues.
- **Pairing**: Each CT image is strictly matched with its corresponding mask via sample identifiers.

#### 💡 Usage Notes

- ✅ Ideal for developing and benchmarking U-Net, CNN, and Transformer-based medical image segmentation architectures.
- ✅ Paired image-mask structure enables straightforward supervised learning pipelines.
- ✅ Supports research in automated anatomical region detection and computer-aided medical image analysis.
- 📚 Recommended to cite the original Kaggle repository when using this dataset.
- 🔐 License: Unknown (Verify specific terms on Kaggle).

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                               |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Mask Alignment**      | Verify that image and mask filenames perfectly align; check for any spatial shifts or resizing artifacts.                    |
| **📐 Resolution Variance** | Standardize input dimensions and ensure masks are resized using nearest-neighbor interpolation to preserve binary integrity. |
| **🧪 Validation Strategy** | Implement patient-aware splitting if metadata permits, to prevent data leakage between train and test sets.                  |

#### 💡 Suggested Preprocessing Pipeline

1. **Load paired data**: Utilize custom data loaders to simultaneously fetch the CT image and its corresponding
   segmentation mask.
2. **Standardize geometry**: Resize both images and masks to uniform dimensions (e.g., 256×256 or 512×512). Use
   nearest-neighbor for masks.
3. **Intensity normalization**: Apply standard CT windowing (e.g., mediastinal or lung window) and scale pixel values
   to [0, 1].
4. **Synchronized augmentation**: Apply identical geometric transformations (rotation, flipping, elastic deformations)
   to both images and masks.
5. **Evaluation metrics**: Report Dice Similarity Coefficient (DSC) and Intersection over Union (IoU) for segmentation
   performance.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{rahul2026chestctseg,
  author = {Rahul, T.},
  title = {Chest CT Images and Segmentation Masks Dataset},
  year = {2026},
  publisher = {Kaggle},
  url = {https://www.kaggle.com/datasets/rahult1999/chest-ct-images-and-segmentation-masks-dataset}
}
```

---

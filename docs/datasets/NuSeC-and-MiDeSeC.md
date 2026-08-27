### 🔬 NuSeC and MiDeSeC (Breast Cancer Histopathology)

**Study**: Nemati, N., et al. (2025). Deep Learning Methodologies for Nuclei Segmentation and Mitosis Detection in
Histopathological Images Analysis. Kaggle.  
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                           |
|-------------------------|-------------------------------------------------------------------|
| **📛 Title**            | NuSeC and MiDeSeC: Nuclei & Mitosis Segmentation/Classification   |
| **🔗 Source**           | https://www.kaggle.com/datasets/sonianmty/nusec-and-midesec       |
| **🫁 Target Organ**     | Breast                                                            |
| **📅 Last Accessed**    | August 27, 2026                                                   |
| **🎯 Supported Tasks**  | 🎭 Instance Segmentation, 📍 Object Detection, 🏷️ Classification |
| **📐 Image Size**       | Variable (High-resolution .bmp / .jpg)                            |
| **📁 Data Format**      | .bmp / .jpg (Images), .csv (Annotation coordinates)               |
| **👥 Demographics**     | ❌ Not included                                                    |
| **🔄 Train/Test Split** | ✅ Provided (Separate train and test image folders)                |

#### 📊 Dataset Composition

| Category                | Details                                           |
|-------------------------|---------------------------------------------------|
| **🖼️ Total Images**    | 350+ annotated histopathology images              |
| **🏥 Imaging Modality** | Histopathology (H&E stained breast cancer tissue) |
| **📦 Total Size**       | ~832 MB                                           |
| **🏥 Source**           | Ankara University (TÜBİTAK Project 121E379)       |

#### 🏷️ Task Details

- **Task Type**: Pixel-level segmentation and object detection
- **NuSeC Dataset**: Nuclei Segmentation and Classification (identifying and outlining individual cell nuclei).
- **MiDeSeC Dataset**: Mitosis Detection, Segmentation, and Classification (identifying dividing cells, crucial for
  cancer grading).

#### 💡 Usage Notes

- ✅ Highly specialized dataset for computational pathology tasks that require pixel-perfect accuracy, such as automated
  breast cancer grading.
- ✅ Annotations are provided in `.csv` format, mapping directly to image filenames, facilitating custom dataloader
  creation.
- 🔐 License: Specified in description (TÜBİTAK academic project).

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                                                           |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Annotation Format**   | The `.csv` files contain coordinate/mask data. You will need to write a custom parser to convert these into binary segmentation masks or bounding boxes. |
| **📐 High Resolution**     | Original `.bmp` files are large. Consider tiling or patching strategies during training to fit GPU memory constraints.                                   |
| **🧪 Validation Strategy** | Evaluate using instance segmentation metrics (e.g., Panoptic Quality (PQ), Average Precision (AP) at IoU=0.5) rather than simple pixel-wise accuracy.    |

#### 💡 Suggested Preprocessing Pipeline

1. **Annotation Parsing**: Read the `.csv` files and generate corresponding binary or instance-level segmentation
   masks (e.g., using `PIL` or `OpenCV`).
2. **Patching**: Extract smaller patches (e.g., 512x512) from the high-resolution `.bmp` images, ensuring the patch
   contains at least one annotated object to maintain a positive sample ratio.
3. **Normalization**: Normalize pixel intensities to [0, 1] and apply stain normalization to reduce H&E variability.
4. **Augmentation**: Apply spatial augmentations (rotation, flipping) *synchronously* to both the image and its
   corresponding segmentation mask.
5. **Model Selection**: Utilize state-of-the-art instance segmentation architectures like Mask R-CNN, HoVer-Net, or
   Cellpose.

#### 📚 Citation

If you use this dataset, please cite the associated studies:

```bibtex
@dataset{nemati2025nusecmidesec,
  author = {Nemati, Nooshin and others},
  title = {NuSeC and MiDeSeC: Nuclei and Mitosis Segmentation/Classification},
  year = {2025},
  publisher = {Kaggle},
  url = {https://www.kaggle.com/datasets/sonianmty/nusec-and-midesec}
}
```

---

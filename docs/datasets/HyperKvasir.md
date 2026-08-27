### 🩺 HyperKvasir: Gastrointestinal Endoscopy Dataset

**Study**: Borgli, H., et al. (2020). HyperKvasir, a comprehensive multi-class image and video dataset for
gastrointestinal endoscopy. Scientific Data.  
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                          |
|-------------------------|------------------------------------------------------------------|
| **📛 Title**            | HyperKvasir: Gastrointestinal Endoscopy Dataset                  |
| **🔗 Source**           | https://datasets.simula.no/hyper-kvasir/                         |
| **🫁 Target Organ**     | Gastrointestinal Tract                                           |
| **📅 Last Accessed**    | August 27, 2026                                                  |
| **🎯 Supported Tasks**  | 🏷️ Classification, 🎭 Segmentation, 📍 Object Detection         |
| **📐 Image Size**       | Variable (High-resolution endoscopic frames)                     |
| **📁 Data Format**      | JPEG (Images), MP4 (Videos), JSON (Bounding Boxes), PNG (Masks)  |
| **👥 Demographics**     | ❌ Not included                                                   |
| **🔄 Train/Test Split** | ❌ Not explicitly provided (community-defined splits recommended) |

#### 📊 Dataset Composition

| Category                | Details                                                                |
|-------------------------|------------------------------------------------------------------------|
| **🖼️ Total Images**    | 10,662 labeled images, 99,417 unlabeled images, 1,000 segmented images |
| **🏥 Imaging Modality** | Gastrointestinal Endoscopy (White-light)                               |
| **📦 Total Size**       | ~58.6 GB (Full dataset)                                                |
| **🏥 Source**           | Simula Research Laboratory / Multiple clinical partners                |

#### 🏷️ Task Details

- **Task Type**: Multi-class classification, Semantic Segmentation, and Video Analysis
- **Number of Classes**: 23 distinct gastrointestinal findings (e.g., Polyp, Barrett’s esophagus, Z-line, Ileocecal
  valve, Ulcerative colitis).
- **Segmentation Subset**: 1,000 polyp images with pixel-wise masks and bounding boxes.

#### 💡 Usage Notes

- ✅ The largest publicly available gastrointestinal endoscopy dataset, offering unprecedented scale for both supervised
  and self-supervised learning.
- ✅ Includes a dedicated, high-quality segmentation subset with bounding boxes, making it ideal for unified
  detection-segmentation models.
- 🔐 License: CC BY 4.0 (Attribution required).

#### ⚠️ Usage Considerations

| Aspect                        | Recommendation                                                                                                                                                             |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Severe Class Imbalance** | The 23 classes are highly imbalanced (some findings are rare). Use focal loss, class weighting, or few-shot learning techniques to prevent majority-class bias.            |
| **📐 Video Redundancy**       | The 373 videos contain highly correlated consecutive frames. If using video frames as images, apply temporal subsampling (e.g., 1 frame per second) to avoid data leakage. |
| **🧪 Validation Strategy**    | Adopt the official benchmark splits if available, or ensure patient-level splitting to avoid evaluating on frames from the same endoscopy procedure.                       |

#### 💡 Suggested Preprocessing Pipeline

1. **Task Selection**: Choose a specific subset (e.g., labeled images for classification, or the 1,000 segmented images
   for polyp segmentation) to manage computational resources.
2. **Mask Generation**: For segmentation, pair the JPEG images with their corresponding PNG masks, ensuring filenames
   match exactly.
3. **Resolution Handling**: Resize images to a standard resolution (e.g., 256x256 or 512x512), preserving the aspect
   ratio with padding if necessary to avoid distorting anatomical structures.
4. **Color Augmentation**: Apply brightness, contrast, and hue adjustments to simulate different endoscopic light
   conditions and camera settings.
5. **Model Selection**: Use architectures designed for medical imaging, such as UNet++ or DeepLabV3+ for segmentation,
   and ConvNeXt or Swin Transformer for classification.

#### 📚 Citation

If you use this dataset, you **must** cite the original publication:

```bibtex
@article{Borgli2020,
  title = {{HyperKvasir, a comprehensive multi-class image and video dataset for gastrointestinal endoscopy}},
  author = {Borgli, Hanna and Thambawita, Vajira and Smedsrud, Pia H and Hicks, Steven and Jha, Debesh and Eskeland, Sigrun L and Randel, Kristin Ranheim and Pogorelov, Konstantin and Lux, Mathias and Nguyen, Duc Tien Dang and Johansen, Dag and Griwodz, Carsten and Stensland, H{\aa}kon K and Garcia-Ceja, Enrique and Schmidt, Peter T and Hammer, Hugo L and Riegler, Michael A and Halvorsen, P{\aa}l and de Lange, Thomas},
  doi = {10.1038/s41597-020-00622-y},
  journal = {Scientific Data},
  volume = {7},
  number = {1},
  pages = {283},
  year = {2020}
}
```

---

### 🩹 Medetec Wound Database

**Study**: Medetec Publications. Medetec Wound Database: stock pictures of wounds.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                      |
|-------------------------|--------------------------------------------------------------|
| **📛 Title**            | Medetec Wound Database                                       |
| **🔗 Source**           | https://www.medetec.co.uk/files/medetec-image-databases.html |
| **🖼️ Target Organ**    | Skin                                                         |
| **📅 Last Accessed**    | August 14, 2026                                              |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                                |
| **📐 Image Size**       | Variable (originally 35mm transparencies, digitized)         |
| **📁 Data Format**      | JPEG/PNG (digitized stock pictures)                          |
| **👥 Demographics**     | ❌ Not included                                               |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)       |

#### 📊 Dataset Composition

| Category                | Details                                                 |
|-------------------------|---------------------------------------------------------|
| **🖼️ Total Images**    | Variable (comprehensive collection of open wound types) |
| **🏥 Imaging Modality** | Clinical Photography (digitized 35mm transparencies)    |
| **📦 Total Size**       | Variable                                                |
| **🏥 Source**           | Medetec Publications                                    |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of wound and skin trauma types
- **Number of Classes**: Multiple (includes Venous ulcers, Arterial ulcers, Pressure ulcers, Diabetic foot ulcers,
  Malignant wounds, Burn and scalds, Extravasation injuries, Pilonidal sinus, etc.)

#### 💡 Usage Notes

- ✅ Extensive repository of free stock images covering a wide variety of open wounds encountered by wound care
  practitioners.
- ✅ Valuable for training models to recognize diverse and rare wound etiologies.
- ⚠️ **Image Quality Note**: Many images were originally captured as 35mm transparencies. Some may exhibit degraded
  quality due to historical mould growth, despite repair efforts.
- 📚 Recommended to cite Medetec Publications when using this dataset.
- 🔐 License: Verify usage terms on the Medetec website (typically free for educational/research use with attribution).

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                               |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------|
| **🎨 Image Degradation**   | Some images may have artifacts or reduced quality; consider quality filtering or robust augmentation.                        |
| **📐 Resolution Variance** | Digitized transparencies vary in resolution; standardize dimensions prior to training.                                       |
| **🧪 Class Imbalance**     | Rare wound types (e.g., Meningitis wounds, Pilonidal sinus) will be underrepresented; apply appropriate sampling strategies. |

#### 💡 Suggested Preprocessing Pipeline

1. **Categorize images**: Organize images into class-labeled subdirectories based on wound type.
2. **Quality filtering**: Optionally inspect and filter out severely degraded images if they hinder model convergence.
3. **Standardize input format**: Resize all images to a uniform dimension (e.g., 224x224 or 512x512).
4. **Apply intensity normalization**: Scale pixel values to [0, 1] and apply contrast enhancement (e.g., CLAHE) to
   mitigate historical degradation.
5. **Stratified evaluation**: Report macro-averaged metrics to ensure fair evaluation across rare and common wound
   classes.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@misc{medetec2026wound,
  title={Medetec Wound Database: stock pictures of wounds},
  author={{Medetec Publications}},
  year={2026},
  url={https://www.medetec.co.uk/files/medetec-image-databases.html},
  note={Accessed: August 14, 2026}
}
```

---

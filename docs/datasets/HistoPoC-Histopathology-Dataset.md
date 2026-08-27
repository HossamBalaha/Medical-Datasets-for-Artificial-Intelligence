### 🤰 HistoPoC Histopathology Dataset

**Study**: Mahmood, T., et al. (2026). Computer-Aided Diagnosis in Spontaneous Abortion: A Histopathology Dataset.
Kaggle.  
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                  |
|-------------------------|--------------------------------------------------------------------------|
| **📛 Title**            | HistoPoC: Histopathology Dataset for Spontaneous Abortion                |
| **🔗 Source**           | https://www.kaggle.com/datasets/tahirlee/histopoc-histopathology-dataset |
| **🫁 Target Organ**     | Uterus / Reproductive (Products of Conception)                           |
| **📅 Last Accessed**    | August 27, 2026                                                          |
| **🎯 Supported Tasks**  | 🏷️ Multi-class Classification (Tissue Phenotyping)                      |
| **📐 Image Size**       | Variable (Captured at 10× magnification)                                 |
| **📁 Data Format**      | JPEG (.jpg)                                                              |
| **👥 Demographics**     | ❌ Not included                                                           |
| **🔄 Train/Test Split** | ✅ Provided (Train and Test folders included)                             |

#### 📊 Dataset Composition

| Category                | Details                                         |
|-------------------------|-------------------------------------------------|
| **🖼️ Total Images**    | 5,666 annotated histopathology images           |
| **🏥 Imaging Modality** | Histopathology (H&E stained, 10× magnification) |
| **📦 Total Size**       | ~59 MB                                          |
| **🏥 Source**           | Atia General Hospital, Karachi, Pakistan        |

#### 🏷️ Classification Task Details

- **Task Type**: Multi-class tissue phenotyping
- **Number of Classes**: 4️⃣
    - 🩸 Chorionic villi
    - 🩸 Decidual tissue
    - 🩸 Hemorrhage
    - 🩸 Trophoblastic tissue

#### 💡 Usage Notes

- ✅ Believed to be the first publicly available dataset focusing specifically on tissue phenotyping in products of
  conception (POC) after spontaneous abortion.
- ✅ Lightweight and well-structured, making it highly accessible for academic research and intelligent diagnostic system
  prototyping.
- 🔐 License: CC BY-SA 4.0.

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                                                                       |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**     | Tissue types may have unequal representation (e.g., Hemorrhage has >1100 images, while others may have fewer). Apply class weighting or focal loss.                  |
| **📐 Magnification Limit** | At 10× magnification, cellular details are less prominent than at 40×. Models must rely more on tissue architecture and texture rather than fine nuclear morphology. |
| **🧪 Validation Strategy** | Utilize the provided Train/Test split, but consider implementing cross-validation within the training set for robust hyperparameter tuning.                          |

#### 💡 Suggested Preprocessing Pipeline

1. **Directory Parsing**: Load data directly from the provided `Train` and `Test` folder hierarchy.
2. **Standardize Input**: Resize all images to a consistent dimension (e.g., 224x224) and convert to 3-channel RGB
   tensors.
3. **Color Augmentation**: Apply stain augmentation (e.g., Macenko jitter) to simulate variations in H&E staining
   protocols.
4. **Geometric Augmentation**: Use random rotations and flips, which are clinically valid for histopathology slides.
5. **Model Selection**: Start with lightweight, pretrained CNNs (e.g., ResNet-18, EfficientNet-B0) as baselines before
   exploring vision transformers.

#### 📚 Citation

If you use this dataset, please cite the original authors:

```bibtex
@dataset{mahmood2026histopoc,
  author = {Mahmood, Tahir and others},
  title = {HistoPoC Histopathology Dataset},
  year = {2026},
  publisher = {Kaggle},
  url = {https://www.kaggle.com/datasets/tahirlee/histopoc-histopathology-dataset}
}
```

---

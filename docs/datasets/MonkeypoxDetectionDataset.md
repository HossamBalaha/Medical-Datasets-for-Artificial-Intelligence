### 🖼️ Monkeypox Detection Dataset, 2025

**Study**: Mohsen, S. (2025). Monkeypox Detection Dataset, 2025. Kaggle.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                         |
|-------------------------|-----------------------------------------------------------------|
| **📛 Title**            | Monkeypox Detection Dataset, 2025                               |
| **🔗 Source**           | https://www.kaggle.com/datasets/drsaeedmohsen/monkeypox-dataset |
| **🖼️ Target Organ**    | Skin                                                            |
| **📅 Last Accessed**    | August 05, 2026                                                 |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification                                       |
| **📐 Image Size**       | Variable                                                        |
| **📁 Data Format**      | Images (JPG/PNG)                                                |
| **👥 Demographics**     | ❌ Not specified                                                 |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)          |

#### 📊 Dataset Composition

| Category                | Details                                 |
|-------------------------|-----------------------------------------|
| **🖼️ Total Images**    | 1,140 images                            |
| **🔬 Imaging Modality** | Dermatology / Clinical Photography      |
| **📦 Total Size**       | ~56.12 MB                               |
| **📦 Data Sources**     | Web-scraped and curated clinical images |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification.
- **Number of Classes**: 2️⃣ Binary.
    - 🦠 Monkeypox (620 images)
    - ✅ Others / Normal / Other skin conditions (520 images)

#### 💡 Usage Notes

- ✅ Provides a focused, balanced dataset for binary dermatological disease detection.
- ✅ Useful for rapid prototyping of skin lesion classification models.
- ⚠️ The dataset lacks extensive metadata and formal clinical validation; results should be interpreted as
  proof-of-concept.
- 🔐 License: Unknown (Verify terms of use on Kaggle before commercial application).

#### ️ Usage Considerations

| Aspect                  | Recommendation                                                                                                                             |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Data Quality**     | Web-scraped datasets may contain noisy labels or duplicate images; perform rigorous deduplication and visual inspection.                   |
| **🎨 Background Noise** | Clinical photos often contain complex backgrounds; apply background removal or focus on ROI cropping.                                      |
| **🧪 Generalization**   | Models trained on this specific dataset may not generalize well to diverse skin tones or lighting conditions without further augmentation. |

#### 💡 Suggested Preprocessing Pipeline

1. **Deduplication**: Apply perceptual hashing (e.g., pHash) to remove exact or near-duplicate images.
2. **Standardization**: Resize all images to a uniform resolution (e.g., 224x224).
3. **Background Removal**: Optionally apply a saliency detection model to isolate the skin lesion from the background.
4. **Normalization**: Scale pixel values to [0, 1] and apply standard normalization.
5. **Augmentation**: Use aggressive color augmentation and random cropping to simulate varying clinical photography
   conditions.

#### 📚 Citation

If you use this dataset, please cite the Kaggle repository:

```bibtex
@dataset{mohsen2025monkeypox,
  author = {Mohsen, Saeed},
  title = {Monkeypox Detection Dataset, 2025},
  year = {2025},
  publisher = {Kaggle},
  url = {https://www.kaggle.com/datasets/drsaeedmohsen/monkeypox-dataset}
}
```

---

### 🖼️ PAD-UFES-20: Skin Lesion Dataset

**Study**: Pacheco, A. G. C., et al. (2020). PAD-UFES-20: a skin lesion dataset composed of patient data and clinical
images collected from smartphones. Mendeley Data.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                         |
|-------------------------|-------------------------------------------------|
| **📛 Title**            | PAD-UFES-20: Skin Lesion Dataset                |
| **🔗 Source**           | https://data.mendeley.com/datasets/zr7vgbcyr2/1 |
| **🖼️ Target Organ**    | Skin                                            |
| **📅 Last Accessed**    | June 30, 2026                                   |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                   |
| **📐 Image Size**       | Variable (smartphone cameras)                   |
| **📁 Data Format**      | PNG (images), CSV (metadata)                    |
| **👥 Demographics**     | ✅ Age, Skin type, Location, Diameter            |
| **🔄 Train/Test Split** | ❌ Not provided (2,298 images)                   |

#### 📊 Dataset Composition

| Category                  | Details                                               |
|---------------------------|-------------------------------------------------------|
| **🖼️ Total Images**      | 2,298 skin lesion images                              |
| **🏥 Imaging Modality**   | Smartphone clinical photography                       |
| **🎨 Color Format**       | RGB                                                   |
| **📦 Total Size**         | ~3.35 GB (compressed)                                 |
| **🏥 Source Institution** | Universidade Federal do Espírito Santo (UFES), Brazil |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of skin lesions
- **Number of Classes**: 6️⃣
- ⚫ Basal Cell Carcinoma (BCC)
- 🔴 Squamous Cell Carcinoma (SCC)
- 🟡 Actinic Keratosis (ACK)
- 🟤 Seborrheic Keratosis (SEK)
- 🟠 Melanoma (MEL)
- 🟢 Nevus (NEV)

#### 💡 Usage Notes

- ✅ Unique dataset captured using everyday smartphone devices (real-world conditions)
- ✅ Includes rich clinical metadata (22 features per sample)
- ✅ Biopsy-proven labels for malignant classes (BCC, SCC, MEL)
- 📚 Required to cite the original Mendeley Data repository
- 🔐 Verify usage terms on Mendeley Data; typically CC BY 4.0

#### ⚠️ Usage Considerations

| Aspect                      | Recommendation                                                                  |
|-----------------------------|---------------------------------------------------------------------------------|
| **🔍 Class Imbalance**      | Verify per-class distribution; apply class-weighted loss if needed              |
| **📐 Resolution Variance**  | Smartphone images vary in quality; standardize dimensions and apply enhancement |
| **🧪 Metadata Integration** | Leverage clinical features (age, location) to improve model performance         |
| **🔐 Ethical Compliance**   | Dataset contains patient data; adhere to institutional review requirements      |

#### 💡 Suggested Preprocessing Pipeline

1. **Load metadata**: Parse CSV to map image paths to diagnostic labels and clinical features.
2. **Standardize input format**: Convert all images to a consistent color space and fixed resolution.
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide statistics.
4. **Augmentation **(training only): Incorporate rotation, flipping, and color jittering to simulate varied lighting.
5. **Stratified evaluation**: Report per-class precision, recall, F1-score, and confusion matrices.

#### 🔗 Associated Resources

- **Mendeley Data Repository**: https://data.mendeley.com/datasets/zr7vgbcyr2/1
- **Related Datasets**:
    - [ISIC 2019](https://www.kaggle.com/c/isic-2019)
    - [Skin Cancer MNIST](https://www.kaggle.com/datasets/andrewmvd/skin-cancer-mnist)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{pacheco2020pad,
  title={PAD-UFES-20: A skin lesion dataset composed of patient data and clinical images collected from smartphones},
  author={Pacheco, Andre GC and Lima, Gustavo R and Salomao, Amanda S and Krohling, Breno and Biral, Igor P and De Angelo, Gabriel G and Alves Jr, F{\'a}bio CR and Esgario, Jos{\'e} GM and Simora, Alana C and Castro, Pedro BC and others},
  journal={Data in brief},
  volume={32},
  pages={106221},
  year={2020},
  publisher={Elsevier}
}
```

---


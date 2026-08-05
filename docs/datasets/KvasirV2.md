### 🩺 Kvasir v2: A Gastrointestinal Tract Dataset

**Study**: Pogorelov, K., et al. (2017). KVASIR: A Multi-Class Image Dataset for Computer Aided Gastrointestinal Disease
Detection. MMSys.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                                |
|-------------------------|----------------------------------------------------------------------------------------|
| **📛 Title**            | Kvasir v2: A Gastrointestinal Tract Dataset                                            |
| **🔗 Source**           | https://www.kaggle.com/datasets/plhalvorsen/kvasir-v2-a-gastrointestinal-tract-dataset |
| **🩺 Target Organ**     | Gastrointestinal Tract                                                                 |
| **📅 Last Accessed**    | August 05, 2026                                                                        |
| **🎯 Supported Tasks**  | 🏷️ Classification, 🔍 Content-Based Retrieval                                         |
| **📐 Image Size**       | Variable (720x576 to 1920x1072 pixels)                                                 |
| **📁 Data Format**      | Images (JPG/PNG) organized in class-specific directories                               |
| **👥 Demographics**     | ❌ Not included (de-identified endoscopic footage)                                      |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                                 |

#### 📊 Dataset Composition

| Category                | Details                                     |
|-------------------------|---------------------------------------------|
| **🖼️ Total Images**    | 8,000 images (1,000 per class)              |
| **🔬 Imaging Modality** | Endoscopy (Optical imaging of the GI tract) |
| **📦 Total Size**       | ~2.52 GB                                    |
| **📦 Data Sources**     | SimulaMet / Oslo University Hospital        |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification and image retrieval.
- **Number of Classes**: 8️⃣ Multiclass.
    - Anatomical Landmarks: Z-line, Pylorus, Cecum.
    - 🦠 Pathological Findings: Esophagitis, Polyps, Ulcerative Colitis.
    - 🛠️ Endoscopic Procedures: Dyed-lifted-polyps, Dyed-resection-margins.

#### 💡 Usage Notes

- ✅ Annotated and verified by experienced medical endoscopists, ensuring high label reliability.
- ✅ Excellent benchmark for both deep learning classification and traditional content-based image retrieval (CBIR).
- 📚 Required to cite the original MMSys 2017 paper when using this data.
- 🔐 License: CC BY-SA 4.0

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                       |
|----------------------------|----------------------------------------------------------------------------------------------------------------------|
| **📐 Resolution Variance** | Images vary significantly in resolution; uniform resizing is mandatory.                                              |
| **🖼️ Picture-in-Picture** | Some images contain a green ScopeGuide overlay; consider masking or cropping this region to prevent model confusion. |
| **🧪 Validation Strategy** | Use stratified k-fold cross-validation to ensure balanced evaluation across all 8 classes.                           |

#### 💡 Suggested Preprocessing Pipeline

1. **Directory Ingestion**: Use framework-native utilities (e.g., `ImageFolder`) to load the class-specific directories.
2. **Overlay Masking**: Detect and crop or blur the green ScopeGuide picture-in-picture overlay in the corner of
   specific images.
3. **Standardization**: Resize all images to a fixed dimension (e.g., 224x224 or 299x299).
4. **Normalization**: Apply ImageNet mean and standard deviation normalization for transfer learning.
5. **Augmentation**: Apply color jittering and geometric transformations to improve robustness against varying
   endoscopic lighting conditions.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@inproceedings{pogorelov2017kvasir,
  author = {Pogorelov, Konstantin and Randel, Kristin Ranheim and Griwodz, Carsten and Eskeland, Sigrun Losada and de Lange, Thomas and Johansen, Dag and Spampinato, Concetto and Dang-Nguyen, Duc-Tien and Lux, Mathias and Schmidt, Peter Thelin and Riegler, Michael and Halvorsen, P{\aa}l},
  title = {KVASIR: A Multi-Class Image Dataset for Computer Aided Gastrointestinal Disease Detection},
  booktitle = {Proceedings of the 8th ACM on Multimedia Systems Conference (MMSys)},
  year = {2017},
  pages = {164--169},
  doi = {10.1145/3083187.3083212}
}
```

---

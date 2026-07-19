### 🦴 Digital Knee X-ray Images: Knee Osteoarthritis Grading

**Study**: Gornale, S., & Patravali, P. (2020). Digital Knee X-ray Images. Mendeley Data, V1.

[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                           |
|-------------------------|-----------------------------------------------------------------------------------|
| **📛 Title**            | Digital Knee X-ray Images: Knee Osteoarthritis Grading                            |
| **🔗 Source**           | https://www.kaggle.com/datasets/orvile/digital-knee-x-ray-images                  |
| **🦴 Target Organ**     | Knee Joint                                                                        |
| **📅 Last Accessed**    | May 24, 2026                                                                      |
| **🎯 Supported Tasks**  | 🏷️ Ordinal Classification (Kellgren–Lawrence Grading)                            |
| **📐 Image Size**       | Variable (8-bit grayscale; original acquisition via PROTEC PRS 500E)              |
| **📁 Data Format**      | JPEG/PNG (.jpg/.png); annotations in filenames or `Digital Knee X-ray Images.csv` |
| **👥 Demographics**     | ❌ Not included (de-identified clinical images)                                    |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                            |

#### 📊 Dataset Composition

| Category                  | Details                                                           |
|---------------------------|-------------------------------------------------------------------|
| **🖼️ Total Images**      | 1,650 digital knee X-ray images                                   |
| **🏥 Imaging Modality**   | Radiographic X-ray (anteroposterior knee views)                   |
| **🎨 Color Format**       | Grayscale, 8-bit depth                                            |
| **📦 Total Size**         | ~121.67 MB (compressed)                                           |
| **🏫 Source Institution** | Rani Channamma University, India                                  |
| **👨‍⚕️ Annotation**      | Dual-expert labeling using Kellgren–Lawrence (K&L) grading system |

#### 🏷️ Classification Task Details

- **Task Type**: Ordinal multiclass classification of knee osteoarthritis severity
- **Number of Classes**: 5️⃣ (ordered severity scale per Kellgren–Lawrence criteria) [[9]]

| K&L Grade | Label    | Description                                                                  | Image Count (MedicalExpert-I) |
|-----------|----------|------------------------------------------------------------------------------|-------------------------------|
| 🔘 0      | Normal   | No radiographic features of OA                                               | 514                           |
| 🟡 1      | Doubtful | Doubtful joint space narrowing, possible osteophytes                         | 477                           |
| 🟠 2      | Mild     | Definite osteophytes, possible joint space narrowing                         | 232                           |
| 🔴 3      | Moderate | Multiple osteophytes, definite joint space narrowing, sclerosis              | 221                           |
| ⚫ 4       | Severe   | Large osteophytes, marked joint space narrowing, severe sclerosis, deformity | 206                           |

**📊 Annotation Protocol**:

- Each image manually labeled by **two independent medical experts** using the Kellgren–Lawrence grading system [[2]]
- Annotations stored either in image filenames or in the companion metadata file `Digital Knee X-ray Images.csv`
- Dataset includes two expert annotation directories: `MedicalExpert-I` and `MedicalExpert-II` for inter-rater
  reliability studies

#### 💡 Usage Notes

- ✅ Suitable for benchmarking ordinal classification models for automated OA severity grading
- ✅ Dual-expert annotations enable research on annotation uncertainty and consensus modeling
- ✅ Includes cartilage region-of-interest (ROI) extraction methodology based on pixel density analysis [[5]]
- ✅ Organized directory structure enables direct integration with standard deep learning data loaders
- 📚 Required to cite the original Mendeley Data repository (DOI: 10.17632/t9ndx37v5h.1) in publications [[14]]
- 🔐 Distributed under CC BY 4.0; attribution required for redistribution or adaptation

#### ⚠️ Usage Considerations

| Aspect                       | Recommendation                                                                             |
|------------------------------|--------------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**       | Grades 0–1 dominate (~60%); consider stratified sampling or class-weighted loss            |
| **🧪 Ordinal Structure**     | Grades represent ordered severity; consider ordinal regression or monotonic constraints    |
| **📐 Resolution Handling**   | Images vary in dimensions; apply uniform resizing prior to model ingestion                 |
| **🔐 Ethical Compliance**    | Dataset contains de-identified patient images; adhere to institutional review requirements |
| **🧭 Domain Generalization** | Single-region sourcing (India); validate on external cohorts for clinical deployment       |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Utilize framework-native utilities (e.g., `torchvision.datasets.ImageFolder`) to ingest
   grade-labeled subfolders.
2. **Standardize input format**: Convert all images to fixed resolution (e.g., 224×224 or 512×512) while preserving
   aspect ratio.
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide statistics.
4. **Augmentation **(training only): Incorporate rotation, flipping, and mild intensity jittering; avoid transformations
   that distort anatomical landmarks.
5. **Ordinal encoding**: Encode K&L grades as ordered integers (0–4) or use one-hot vectors with ordinal constraints.
6. **Stratified evaluation**: Report per-grade precision, recall, F1-score, and ordinal-aware metrics (e.g., weighted
   kappa, mean absolute error).

#### 🔗 Associated Resources

- **Kaggle Repository**: https://www.kaggle.com/datasets/orvile/digital-knee-x-ray-images
- **Mendeley Data **(Primary Source): https://data.mendeley.com/datasets/t9ndx37v5h/1 [[5]]
- **Related Publications**:
    - Gornale, S. S., Patravali, P. U., & Hiremath, P. S. (2020). A Comprehensive Digital Knee X-ray Image Dataset for
      the Assessment of Osteoarthritis. *JSM Biomedical Imaging Data Papers*.
    - Kellgren, J. H., & Lawrence, J. S. (1957). Radiological assessment of osteo-arthrosis. *Annals of the Rheumatic
      Diseases*.
- **Related Datasets**:
    - [Knee Osteoarthritis Dataset with KL Grading - 2018](https://www.kaggle.com/datasets/tommyngx/knee-osteoarthritis-dataset-with-kl-grading-2018)
    - [Multi-Class Knee Osteoporosis X-Ray Dataset](https://www.kaggle.com/datasets/mohamedgobara/multi-class-knee-osteoporosis-x-ray-dataset)

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{gornale2020digitalknee,
    author = {Gornale, Shivanand and Patravali, Pooja},
    title = {Digital Knee X-ray Images},
    year = {2020},
    publisher = {Mendeley Data},
    version = {1},
    doi = {10.17632/t9ndx37v5h.1},
    url = {https://doi.org/10.17632/t9ndx37v5h.1}
}
```

---


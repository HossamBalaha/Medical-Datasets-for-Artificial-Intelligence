### 🧠 Rare Neurological Diseases MRI - Curated Edition

**Study**: Ahsan, M. (2026). Rare Neurological Diseases MRI - Curated Edition. Kaggle. (Original source: Ajmain et al.,
2024, Mendeley Data).
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                                    |
|-------------------------|--------------------------------------------------------------------------------------------|
| **📛 Title**            | Rare Neurological Diseases MRI - Curated Edition                                           |
| **🔗 Source**           | https://www.kaggle.com/datasets/ahsanneural/rare-neurological-diseases-mri-curated-edition |
| **🧠 Target Organ**     | Brain                                                                                      |
| **📅 Last Accessed**    | November 10, 2026                                                                          |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                                                               |
| **📐 Image Size**       | Variable (curated to top 20-50% quality)                                                   |
| **📁 Data Format**      | JPG (images), CSV (metadata and disease summary)                                           |
| **👥 Demographics**     | ❌ Not included (linked to Orphadata ORPHA codes)                                          |
| **🔄 Train/Test Split** | ✅ Yes (70% Train / 15% Val / 15% Test, stratified)                                        |

#### 📊 Dataset Composition

| Category                | Details                                                |
|-------------------------|--------------------------------------------------------|
| **🖼️ Total Images**     | 2,000 MRI scans (perfectly balanced: 400 per disease)  |
| **🏥 Imaging Modality** | Magnetic Resonance Imaging (MRI)                       |
| **📦 Total Size**       | ~57.64 MB                                              |
| **🏥 Source**           | Curated from Mendeley Benchmark Diagnostic MRI Dataset |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of rare neurological conditions
- **Number of Classes**: 5️⃣
    - 🧠 Walker-Warburg Syndrome (ORPHA:899)
    - 🧠 Pachygyria with Cerebellar Hypoplasia (ORPHA:2524)
    - 🧠 Moyamoya Disease with IVH (ORPHA:2573)
    - 🧠 Hallervorden-Spatz Disease / PKAN (ORPHA:157850)
    - 🧠 Fukuyama Muscular Dystrophy (ORPHA:272)

#### 💡 Usage Notes

- ✅ Addresses the critical shortage of high-quality, balanced imaging data for rare diseases.
- ✅ Images were selected using automated quality assessment (contrast, sharpness, brightness balance).
- ✅ Pre-split into train/val/test sets with proper stratification, ready for Keras/PyTorch `ImageFolder` loading.
- ✅ Includes official Orphanet (ORPHA) disease codes in the metadata for clinical traceability.
- 📚 Required to cite both this curated Kaggle version and the original Mendeley Data source.
- 🔐 Distributed under CC BY 4.0; attribution required.

#### ⚠️ Usage Considerations

| Aspect                      | Recommendation                                                                                                    |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------|
| **🔍 Rare Disease Context** | While balanced here, real-world prevalence is <1-5 per 100K; models may need calibration for clinical deployment. |
| **📐 Image Quality**        | Top-quality images were selected; performance may drop on lower-quality clinical scans.                           |
| **🧪 Few-Shot Potential**   | Excellent benchmark for meta-learning and few-shot learning algorithms in medical AI.                             |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Utilize framework-native utilities (e.g., `torchvision.datasets.ImageFolder`) to ingest
   the pre-split folders.
2. **Standardize input format**: Resize images to a fixed resolution (e.g., 224×224 or 256×256) while preserving aspect
   ratio.
3. **Apply intensity normalization**: Convert to grayscale or maintain RGB; scale pixel values to [0, 1] or use ImageNet
   normalization for pretrained backbones.
4. **Augmentation **(training only): Incorporate rotation, flipping, and mild intensity jittering to improve
   generalization.
5. **Stratified evaluation**: Report per-class precision, recall, F1-score, and macro-averaged metrics to ensure fair
   evaluation across all 5 rare classes.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{ahsan2026rareneuro,
    author = {Ahsan, Muhammad},
    title = {Rare Neurological Diseases MRI - Curated Edition},
    year = {2026},
    publisher = {Kaggle},
    url = {https://www.kaggle.com/datasets/ahsanneural/rare-neurological-diseases-mri-curated-edition}
}

@dataset{ajmain2024benchmark,
    author = {Ajmain, Moshfiqur Rahman and Khatun, Mst. Farhana and khushbu, sharun akter},
    title = {Benchmark Diagnostic MRI and Medical Imaging Dataset},
    year = {2024},
    publisher = {Mendeley Data},
    version = {1},
    doi = {10.17632/d73rs38yk6.1}
}
```

---
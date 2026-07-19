### 🫁 CheXpert: A Large Chest Radiograph Dataset with Uncertainty Labels and Expert Comparison

**Study**: Irvin, J., Rajpurkar, P., Ko, M., Yu, S. C., Ciurea-Ilcus, S., Chute, C., ... & Ng, A. Y. (2019). CheXpert: A
Large Chest Radiograph Dataset with Uncertainty Labels and Expert Comparison. *Proceedings of the AAAI Conference on
Artificial Intelligence*, 33(01), 590-597.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                                  |
|-------------------------|------------------------------------------------------------------------------------------|
| **📛 Title**            | CheXpert: A Large Chest Radiograph Dataset with Uncertainty Labels and Expert Comparison |
| **🔗 Source**           | https://stanfordmlgroup.github.io/competitions/chexpert/                                 |
| **🫁 Target Organ**     | Lungs / Chest                                                                            |
| **📅 Last Accessed**    | June 26, 2026                                                                            |
| **🎯 Supported Tasks**  | 🏷️ Multiclass / Multi-label Classification                                              |
| **📐 Image Size**       | Variable (Chest X-rays)                                                                  |
| **📁 Data Format**      | JPEG (.jpg) / DICOM                                                                      |
| **👥 Demographics**     | ❌ Not included (de-identified)                                                           |
| **🔄 Train/Test Split** | ✅ Yes (Train / Validation / Test)                                                        |

#### 📊 Dataset Composition

| Category                  | Details                                        |
|---------------------------|------------------------------------------------|
| **🖼️ Total Images**      | 224,316 chest radiographs from 65,240 patients |
| **🏥 Imaging Modality**   | Radiographic X-ray (Frontal and Lateral views) |
| **🎨 Color Format**       | Grayscale                                      |
| **🏥 Source Institution** | Stanford Hospital                              |
| **📅 Collection Period**  | October 2002 – July 2017                       |

#### 🏷️ Classification Task Details

- **Task Type**: Multi-label classification of 14 radiological observations
- **Number of Classes**: 14️⃣ (No Finding, Enlarged Cardiomediastinum, Cardiomegaly, Lung Opacity, Lung Lesion, Edema,
  Consolidation, Pneumonia, Atelectasis, Pneumothorax, Pleural Effusion, Pleural Other, Fracture, Support Devices)
- **Label Types**: Positive (1), Negative (0), Uncertain (-1), or Blank (unmentioned)
- **Competition Tasks**: 5️⃣ (Atelectasis, Cardiomegaly, Consolidation, Edema, Pleural Effusion)

**📊 Dataset Distribution**:

| Split     | Image Count | Purpose                               |
|-----------|-------------|---------------------------------------|
| 🟢 Train  | 223,816     | Model training and development        |
| 🟡 Valid  | 200         | Hyperparameter tuning                 |
| 🔴 Test   | 500         | Final performance evaluation (Expert) |
| **Total** | **224,316** | —                                     |

> **ℹ️ Note**: The training set features uncertainty labels extracted via an automated rule-based labeler from free-text
> radiology reports. The test set contains strong ground truth from a majority vote of 8 board-certified radiologists.

#### 💡 Usage Notes

- ✅ Suitable for benchmarking deep learning models for automated chest X-ray interpretation
- ✅ Features uncertainty labels to handle ambiguous radiology report statements
- ✅ Includes a radiologist-labeled reference standard evaluation set for rigorous benchmarking
- ✅ Supports research on multi-label classification and uncertainty modeling in medical imaging
- 📚 Required to cite the original AAAI publication and Stanford ML Group when using this dataset

#### ⚠️ Usage Considerations

| Aspect                       | Recommendation                                                                                              |
|------------------------------|-------------------------------------------------------------------------------------------------------------|
| **🔍 Label Uncertainty**     | Training labels contain uncertainty; explore approaches like U-Ignore, U-Zeroes, U-Ones, or U-MultiClass    |
| **🧪 Multi-Label Nature**    | Images can have multiple concurrent pathologies; use appropriate loss functions (e.g., BCE with logits)     |
| **📐 View Handling**         | Dataset contains both frontal and lateral views; consider view-agnostic or multi-view architectures         |
| **🔐 Licensing**             | Verify usage terms on the Stanford AIMI website; typically restricted to non-commercial research use        |
| **🧭 Domain Generalization** | Sourced from a single institution (Stanford Hospital); validate on external cohorts for clinical deployment |

#### 💡 Suggested Preprocessing Pipeline

1. **Parse metadata**: Load the provided CSV files to map image paths to the 14 observation labels and uncertainty
   flags.
2. **Standardize input format**: Convert all images to a consistent color space (single-channel grayscale) and fixed
   resolution (e.g., 320x320 or 512x512).
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide mean and standard
   deviation.
4. **Handle uncertainty**: Decide on a strategy for uncertain labels (e.g., U-MultiClass treats uncertainty as a
   separate class).
5. **Augmentation **(training only): Incorporate rotation, flipping, and intensity jittering to improve model
   generalization.
6. **Stratified evaluation**: Report per-class AUC-ROC, sensitivity, and specificity, especially for the 5 competition
   tasks.

#### 🔗 Associated Resources

- **Stanford ML Group Competition Page**: https://stanfordmlgroup.github.io/competitions/chexpert/
- **Stanford AIMI Dataset**: https://stanford.redivis.com/datasets/5yyj-1a9f6ap0x
- **Test Set Labels & Links**: https://github.com/rajpurkarlab/cheXpert-test-set-labels
- **CheXpert Labeler**: https://github.com/stanfordmlgroup/chexpert-labeler

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@inproceedings{irvin2019chexpert,
  title={Chexpert: A large chest radiograph dataset with uncertainty labels and expert comparison},
  author={Irvin, Jeremy and Rajpurkar, Pranav and Ko, Michael and Yu, Yifan and Ciurea-Ilcus, Silviana and Chute, Chris and Marklund, Henrik and Haghgoo, Behzad and Ball, Robyn and Shpanskaya, Katie and others},
  booktitle={Proceedings of the AAAI conference on artificial intelligence},
  volume={33},
  number={01},
  pages={590--597},
  year={2019}
}
```

---


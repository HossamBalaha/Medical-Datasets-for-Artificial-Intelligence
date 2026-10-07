### 🧠 Dynamic Image for 3D MRI Alzheimer’s Disease Classification

**Study**: Xing, X., Liang, G., Blanton, H., Rafique, M. U., Wang, C., Lin, A.-L., & Jacobs, N. (2020). Dynamic Image
for 3D MRI Image Alzheimer's Disease Classification. arXiv preprint arXiv:2012.00119.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                           |
|-------------------------|-------------------------------------------------------------------|
| **📛 Title**            | Dynamic Image for 3D MRI Image Alzheimer’s Disease Classification |
| **🔗 Source**           | https://github.com/mvrl/alzheimer-project                         |
| **🧠 Target Organ**     | Brain                                                             |
| **📅 Last Accessed**    | October 06, 2026                                                  |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification                                         |
| **📐 Image Size**       | Variable (Derived from 3D MRI volumes)                            |
| **📁 Data Format**      | NumPy arrays (.npy) or NIfTI (.nii)                               |
| **👥 Demographics**     | ❌ Not explicitly detailed (Derived from ADNI)                     |
| **🔄 Train/Test Split** | ✅ Yes (5-fold cross-validation splits provided)                   |

#### 📊 Dataset Composition

| Category                | Details                                                   |
|-------------------------|-----------------------------------------------------------|
| **🖼️ Total Samples**   | Processed dynamic images derived from ADNI 3D MRI volumes |
| **🏥 Imaging Modality** | Magnetic Resonance Imaging (MRI)                          |
| **📦 Total Size**       | Variable (Dependent on Google Drive download)             |
| **🏥 Source**           | Alzheimer's Disease Neuroimaging Initiative (ADNI)        |

#### 🏷️ Classification Task Details

- **Task Type**: Binary classification of Alzheimer's Disease progression
- **Number of Classes**: 2️⃣
    - 🧠 Alzheimer's Disease (AD)
    - ✅ Cognitively Normal (CN)

#### 💡 Usage Notes

- ✅ Introduces the "Dynamic Image" representation for 3D MRI, collapsing volumetric data into a single 2D image that
  encodes spatiotemporal or multi-slice appearance changes, significantly reducing computational cost compared to
  3D-CNNs.
- ✅ Based on the widely validated ADNI cohort, ensuring high clinical relevance.
- ✅ Includes ready-to-use 5-fold cross-validation splitting scripts.
- 📚 Required to cite the original arXiv publication and acknowledge the ADNI initiative.
- 🔐 Usage is subject to ADNI data use agreements.

#### ⚠️ Usage Considerations

| Aspect                      | Recommendation                                                                                                                      |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 ADNI Compliance**      | Ensure compliance with Alzheimer's Disease Neuroimaging Initiative (ADNI) data use policies.                                        |
| **📐 Representation Shift** | The dynamic image is a derived representation; models trained on it may not directly transfer to raw 3D volumes without adaptation. |
| **🧪 Cross-Validation**     | Utilize the provided 5-fold split to ensure fair comparison with the original paper's results.                                      |

#### 💡 Suggested Preprocessing Pipeline

1. **Data Conversion**: If starting from raw .nii files, use the provided `ADNI2_MRI_AD_niiData.ipynb` scripts to
   convert volumes to .npy format.
2. **Dynamic Image Generation**: Apply the adapted dynamic image Python script to encode the 3D volume into a 2D
   representation.
3. **Intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide statistics.
4. **2D Augmentation **(training only): Incorporate standard 2D rotations, flipping, and intensity jittering.
5. **Stratified evaluation**: Report accuracy, sensitivity, specificity, and AUC-ROC across the 5 folds.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@misc{xing2020dynamic,
    title = {Dynamic Image for 3D MRI Image Alzheimer's Disease Classification},
    author = {Xing, Xin and Liang, Gongbo and Blanton, Hunter and Rafique, M. Usman and Wang, Chris and Lin, Ai-Ling and Jacobs, Nathan},
    year = {2020},
    eprint = {2012.00119},
    archivePrefix = {arXiv},
    primaryClass = {cs.CV},
    url = {https://arxiv.org/abs/2012.00119}
}
```

---

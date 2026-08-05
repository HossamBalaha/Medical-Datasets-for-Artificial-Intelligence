### 🫁 SARS-COV-2 Ct-Scan Dataset

**Study**: Soares, E., Angelov, P., Biaso, S., Higa Froes, M., & Kanda Abe, D. (2020). SARS-CoV-2 CT-scan dataset: A
large dataset of real patients CT scans for SARS-CoV-2 identification. medRxiv.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                               |
|-------------------------|-----------------------------------------------------------------------|
| **📛 Title**            | SARS-COV-2 Ct-Scan Dataset                                            |
| ** Source**             | https://www.kaggle.com/datasets/plameneduardo/sarscov2-ctscan-dataset |
| **🫁 Target Organ**     | Lungs / Chest                                                         |
| **📅 Last Accessed**    | August 05, 2026                                                       |
| **🎯 Supported Tasks**  | 🏷️ Binary Classification                                             |
| **📐 Image Size**       | Variable (CT slices)                                                  |
| **📁 Data Format**      | Images (PNG)                                                          |
| **👥 Demographics**     | ❌ Not included (de-identified patient data from Sao Paulo, Brazil)    |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                |

#### 📊 Dataset Composition

| Category                | Details                                         |
|-------------------------|-------------------------------------------------|
| **🖼️ Total Images**    | 2,482 CT scans (1,252 Positive, 1,230 Negative) |
| **🔬 Imaging Modality** | Computed Tomography (CT)                        |
| **📦 Total Size**       | ~242.23 MB                                      |
| **📦 Data Sources**     | Hospitals in Sao Paulo, Brazil                  |

#### ️ Classification Task Details

- **Task Type**: Binary classification.
- **Number of Classes**: 2️⃣ Binary.
    - 🦠 COVID-19 (SARS-CoV-2 Positive)
    - ✅ non-COVID (SARS-CoV-2 Negative)

#### 💡 Usage Notes

- ✅ Provides a balanced, large-scale dataset specifically for binary COVID-19 detection via CT scans.
- ✅ Achieved a baseline F1 score of 97.31% using eXplainable Deep Neural Networks (xDNN).
- Required to cite the original medRxiv preprint and the xDNN paper.
- 🔐 License: CC BY-NC-SA 4.0

#### ⚠️ Usage Considerations

| Aspect                 | Recommendation                                                                                                                                      |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| **📐 Slice Variance**  | CT scans are 3D volumes sliced into 2D images; consider whether to treat slices independently or reconstruct 3D volumes.                            |
| **🧪 Patient Leakage** | Multiple slices may originate from the same patient. Implement patient-wise splitting to prevent severe data leakage and overly optimistic metrics. |
| ** Domain Shift**      | Scans are from a specific demographic and scanner type in Brazil; validate on external datasets to ensure generalization.                           |

#### 💡 Suggested Preprocessing Pipeline

1. **Volume Reconstruction **(Optional): Group 2D slices by patient ID if 3D CNNs or RNNs are to be utilized.
2. **Lung Segmentation**: Apply a pre-trained lung segmentation model to isolate the lung parenchyma and remove
   surrounding tissue/bone.
3. **Standardization**: Resize slices to a fixed resolution (e.g., 224x224 or 512x512).
4. **Normalization**: Apply Hounsfield Unit (HU) windowing (e.g., lung window: -1000 to 400 HU) if raw DICOM data is
   available, or standard min-max scaling for PNGs.
5. **Augmentation**: Utilize elastic deformations and random rotations to simulate varying patient positioning.

#### Citation

If you use this dataset, please cite:

```bibtex
@article{soares2020sars,
  title={SARS-CoV-2 CT-scan dataset: A large dataset of real patients CT scans for SARS-CoV-2 identification},
  author={Soares, Eduardo and Angelov, Plamen and Biaso, Sarah and Higa Froes, Michele and Kanda Abe, Daniel},
  journal={medRxiv},
  year={2020},
  doi={10.1101/2020.04.24.20078584}
}
```

---

### 🔬 UNITOPATHO: Colorectal Polyps & Adenoma Grading

**Study**: Barbano, C. A., et al. (2021). Unitopatho, A Labeled Histopathological Dataset for Colorectal Polyps
Classification and Adenoma Dysplasia Grading. IEEE ICIP.  
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                |
|-------------------------|------------------------------------------------------------------------|
| **📛 Title**            | UNITOPATHO: Colorectal Polyps Classification and Adenoma Dysplasia     |
| **🔗 Source**           | https://ieee-dataport.org/open-access/unitopatho                       |
| **🫁 Target Organ**     | Colorectal / Colon                                                     |
| **📅 Last Accessed**    | August 27, 2026                                                        |
| **🎯 Supported Tasks**  | 🏷️ Multi-class Classification, 📊 Dysplasia Grading                   |
| **📐 Image Size**       | Variable (Patches extracted at 800 and 7000 µm/px resolutions)         |
| **📁 Data Format**      | PNG images + Metadata (CSV)                                            |
| **👥 Demographics**     | ❌ Not included (Patient-level anonymized)                              |
| **🔄 Train/Test Split** | ❌ Not explicitly provided (CSV contains metadata for custom splitting) |

#### 📊 Dataset Composition

| Category                | Details                                                       |
|-------------------------|---------------------------------------------------------------|
| **🖼️ Total Images**    | 9,536 H&E-stained image patches                               |
| **🏥 Imaging Modality** | Histopathology (H&E-stained, 20× magnification, 0.4415 µm/px) |
| **📦 Total Size**       | ~274.98 GB (Compressed)                                       |
| **🏥 Source**           | University of Turin (Hamamatsu Nanozoomer S210 scanner)       |

#### 🏷️ Classification Task Details

- **Task Type**: Multi-class classification and hierarchical grading
- **Number of Classes**: 6️⃣
    - 🌱 NORM: Normal tissue
    - 🟢 HP: Hyperplastic Polyp
    - 🟡 TA.LG: Tubular Adenoma, Low-Grade dysplasia
    - 🟠 TA.HG: Tubular Adenoma, High-Grade dysplasia
    - 🔴 TVA.LG: Tubulo-Villous Adenoma, Low-Grade dysplasia
    - 🟣 TVA.HG: Tubulo-Villous Adenoma, High-Grade dysplasia

#### 💡 Usage Notes

- ✅ Expertly annotated by pathologists, making it a high-quality benchmark for colorectal cancer screening AI.
- ✅ Provides both fine-grained (6 classes) and coarse-grained (4 classes: HP, NORM, HG, LG) labeling in the metadata.
- 📚 Recommended to cite the original IEEE ICIP 2021 paper.
- 🔐 License: MIT License (for accompanying code), Open Access (for dataset via IEEE DataPort).

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                                                                                                   |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 Hierarchical Labels** | The dataset supports both 6-class and 4-class tasks. Choose the target granularity based on your clinical use case (e.g., binary benign vs. malignant).          |
| **📐 Resolution Variance** | Two resolutions are provided. Ensure your model architecture can handle the target resolution, or resize consistently during preprocessing.                      |
| **🧪 Validation Strategy** | Use the provided `reference WSI` and `roi` columns in the CSV to ensure patches from the same whole slide image do not appear in both training and testing sets. |

#### 💡 Suggested Preprocessing Pipeline

1. **Metadata Parsing**: Load the provided CSV files to map image IDs to their respective labels, WSI references, and
   coordinates.
2. **Patient/WSI-aware Splitting**: Group data by `reference WSI` before splitting to guarantee no data leakage.
3. **Color Normalization**: Apply stain normalization to standardize the H&E appearance across different scanner
   batches.
4. **Standardize input format**: Resize patches to a fixed dimension (e.g., 224x224 or 256x256) and convert to tensors.
5. **Augmentation**: Apply random rotations (90°, 180°, 270°) and flips, which are highly effective and clinically valid
   for histopathology patches.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@inproceedings{barbano2021unitopatho,
  author={Barbano, Carlo Alberto and Perlo, Daniele and Tartaglione, Enzo and Fiandrotti, Attilio and Bertero, Luca and Cassoni, Paola and Grangetto, Marco},
  booktitle={2021 IEEE International Conference on Image Processing (ICIP)}, 
  title={Unitopatho, A Labeled Histopathological Dataset for Colorectal Polyps Classification and Adenoma Dysplasia Grading}, 
  year={2021},
  pages={76-80},
  doi={10.1109/ICIP42928.2021.9506198}
}
```

---

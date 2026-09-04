### 🩺 Kvasir-SEG

**Study**: Jha, D., Smedsrud, P. H., Riegler, M. A., Halvorsen, P., de Lange, T., Johansen, D., & Johansen, H. D. (
2020). Kvasir-seg: A segmented polyp dataset. In *International Conference on Multimedia Modeling* (pp. 451-462).
Springer.
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                             |
|-------------------------|---------------------------------------------------------------------|
| **📛 Title**            | Kvasir-SEG                                                          |
| **🔗 Source**           | https://datasets.simula.no/kvasir-seg/                              |
| **🩺 Target Organ**     | Gastrointestinal Tract (Colon)                                      |
| **📅 Last Accessed**    | August 31, 2026                                                     |
| **🎯 Supported Tasks**  | 🎭 Semantic Segmentation, 📍 Localization                           |
| **📐 Image Size**       | Variable (332 × 487 to 1920 × 1072 pixels)                          |
| **📁 Data Format**      | JPEG (.jpg) for images, PNG/TIFF for masks, JSON for bounding boxes |
| **👥 Demographics**     | ❌ Not included (de-identified clinical colonoscopy frames)          |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)              |

#### 📊 Dataset Composition

| Category                  | Details                                                  |
|---------------------------|----------------------------------------------------------|
| **🖼️ Total Images**      | 1,000 polyp images with corresponding ground truth masks |
| **🏥 Imaging Modality**   | White-light endoscopy (WLE)                              |
| **📦 Total Size**         | ~46.2 MB (compressed)                                    |
| **🏥 Source Institution** | Simula Research Laboratory, Norway                       |

#### 🎭 Segmentation Task Details

- **Task Type**: Binary semantic segmentation of colorectal polyps
- **Annotation Targets**: Pixel-wise mask corresponding to the polyp region.
- **Annotation Protocol**: Manually annotated and verified by an experienced gastroenterologist using Labelbox.
  Superfluous endoscope position marking probes (ScopeGuide) have been masked out with black boxes.

#### 💡 Usage Notes

- ✅ Open-access dataset designed to push the state-of-the-art in polyp detection and segmentation.
- ✅ Includes bounding box coordinates in a JSON file, enabling joint segmentation and localization research.
- ✅ Highly cited benchmark, enabling direct comparison with a wide range of computer vision methodologies.
- 📚 Required to cite the original *International Conference on Multimedia Modeling* publication when using this dataset.
- 🔐 License: Restricted to research and educational purposes; commercial use is forbidden without prior written
  permission.

#### ⚠️ Usage Considerations

| Aspect                     | Recommendation                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------|
| **📐 Resolution Variance** | Images vary significantly in resolution; standardize to fixed dimensions prior to training. |
| **🧪 Domain Shift**        | Sourced from specific endoscope manufacturers; validate on external cohorts for robustness. |
| **🔐 Licensing**           | Strictly non-commercial; verify terms before any derivative work or deployment.             |

#### 💡 Suggested Preprocessing Pipeline

1. **Load directory structure**: Ingest images and corresponding masks from their respective folders.
2. **Standardize geometry**: Resize images and masks to uniform dimensions (e.g., 256×256 or 512×512) while preserving
   aspect ratio.
3. **Apply intensity normalization**: Scale pixel values to [0, 1] or standardize using dataset-wide statistics.
4. **Augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering; preserve polyp
   boundary integrity.
5. **Evaluation metrics**: Report Dice coefficient and Intersection over Union (IoU) as the primary segmentation
   metrics.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@inproceedings{jha2020kvasir,
  title={Kvasir-seg: A segmented polyp dataset},
  author={Jha, Debesh and Smedsrud, Pia H and Riegler, Michael A and Halvorsen, P{\aa}l and de Lange, Thomas and Johansen, Dag and Johansen, H{\aa}vard D},
  booktitle={International Conference on Multimedia Modeling},
  pages={451--462},
  year={2020},
  organization={Springer},
  doi={10.1007/978-3-030-67832-6_37}
}
```

---

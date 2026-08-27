### 🧬 HEMIT: H&E to mIHC Image Translation

**Study**: Bian, C., et al. (2024). HEMIT: H&E to Multiplex-immunohistochemistry Image Translation with Dual-Branch
Pix2pix Generator. arXiv.  
[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                        |
|-------------------------|----------------------------------------------------------------|
| **📛 Title**            | HEMIT: H&E to Multiplex-immunohistochemistry Image Translation |
| **🔗 Source**           | https://data.mendeley.com/datasets/3gx53zm49d/1                |
| **🫁 Target Organ**     | Colorectal / Colon                                             |
| **📅 Last Accessed**    | August 27, 2026                                                |
| **🎯 Supported Tasks**  | 🔄 Image-to-Image Translation (Stain Translation)              |
| **📐 Image Size**       | 1024 × 1024 pixels                                             |
| **📁 Data Format**      | TIF (Tagged Image File Format)                                 |
| **👥 Demographics**     | ❌ Not included                                                 |
| **🔄 Train/Test Split** | ✅ Provided (Train: 3,717, Validation: 630, Test: 945)          |

#### 📊 Dataset Composition

| Category                | Details                                                            |
|-------------------------|--------------------------------------------------------------------|
| **🖼️ Total Images**    | 5,292 paired image patches                                         |
| **🏥 Imaging Modality** | Histopathology (H&E) and Multiplex Immunohistochemistry (mIHC)     |
| **📦 Total Size**       | ~9.84 GB                                                           |
| **🏥 Source**           | ImmunoAIzer work (Colon cancer patients, University of Manchester) |

#### 🏷️ Translation Task Details

- **Task Type**: Paired Image-to-Image Translation (Synthesizing mIHC from H&E)
- **Input Domain**: H&E stained tissue patches
- **Output Domain**: 3-channel mIHC images (DAPI, panCK, CD3)
- **Alignment**: Cellular-wise registered pairs derived from the same tissue sectioning approach.

#### 💡 Usage Notes

- ✅ Tailored specifically for stain translation tasks, eliminating the need for complex unpaired translation methods (
  like CycleGAN).
- ✅ High alignment quality ensures reliable pixel-wise loss calculation (e.g., L1/L2, SSIM) during training.
- 📚 Recommended to cite the original arXiv preprint and the associated MICCAI workshop paper.
- 🔐 License: Standard academic use (Verify specific terms on the Mendeley Data page).

#### ⚠️ Usage Considerations

| Aspect                    | Recommendation                                                                                                                                                      |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **🔍 File Pairing**       | Input and label images share the exact same filename (e.g., `patch_0_0.tif`). Ensure your dataloader correctly pairs them from the `input` and `label` directories. |
| **📐 Large Patch Size**   | At 1024x1024, these images are large. Consider cropping them into smaller patches (e.g., 256x256 or 512x512) during training to fit GPU memory constraints.         |
| **🧪 Evaluation Metrics** | Use structural metrics (SSIM, PSNR) and perceptual metrics (LPIPS) alongside Pearson Correlation to comprehensively evaluate translation quality.                   |

#### 💡 Suggested Preprocessing Pipeline

1. **Directory Parsing**: Structure your dataloader to read from `train/input`, `train/label`, `val/input`, `val/label`,
   etc., matching filenames exactly.
2. **Format Conversion**: Convert 16-bit or high-dynamic-range TIF files to standard 8-bit RGB/RGBA arrays if required
   by your framework, preserving relative channel intensities.
3. **Patching (Optional)**: Randomly crop the 1024x1024 images into smaller, fixed-size patches (e.g., 256x256) to
   increase dataset size and reduce memory footprint.
4. **Normalization**: Normalize pixel values to [-1, 1] (common for GANs like Pix2pix) or [0, 1] depending on your
   generator's final activation function.
5. **Augmentation**: Apply synchronized geometric transformations (e.g., random horizontal flip, 90-degree rotation) to
   *both* the input and label images simultaneously to maintain spatial alignment.

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@article{bian2024hemit,
  title={HEMIT: H&E to Multiplex-immunohistochemistry Image Translation with Dual-Branch Pix2pix Generator},
  author={Bian, Chang and Phillips, Beth and Cootes, Tim and Fergie, Martin},
  journal={arXiv preprint arXiv:2403.18501},
  year={2024},
  doi={10.17632/3gx53zm49d.1}
}
```

---

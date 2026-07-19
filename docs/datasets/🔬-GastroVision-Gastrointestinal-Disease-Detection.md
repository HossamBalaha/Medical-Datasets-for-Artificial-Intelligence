### 🔬 GastroVision: Gastrointestinal Disease Detection

**Study**: Jha, D., Sharma, V., Riegler, M., Halvorsen, P., & Bagci, U. (2024). GastroVision: A Compact GI Endoscopy
Dataset. Kaggle.

[🔝 Back to Summary](#-dataset-summary)

| Metadata                | Details                                                                                |
|-------------------------|----------------------------------------------------------------------------------------|
| **📛 Title**            | GastroVision: Gastrointestinal Disease Detection                                       |
| **🔗 Source**           | https://www.kaggle.com/datasets/orvile/gastrovision-gastrointestinal-disease-detection |
| **🦴 Target Organ**     | Gastrointestinal Tract (Esophagus, Stomach, Small Bowel, Colon, Rectum)                |
| **📅 Last Accessed**    | May 08, 2026                                                                           |
| **🎯 Supported Tasks**  | 🏷️ Multiclass Classification                                                          |
| **📐 Image Size**       | Variable (endoscopy frames; standardization recommended)                               |
| **📁 Data Format**      | JPEG/PNG (.jpg/.png) organized in class-labeled subdirectories                         |
| **👥 Demographics**     | ❌ Not included (de-identified clinical endoscopy footage)                              |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)                                 |

#### 📊 Dataset Composition

| Category                   | Details                                                                    |
|----------------------------|----------------------------------------------------------------------------|
| **🖼️ Total Images**       | 8,000 gastrointestinal endoscopy images                                    |
| **🔬 Imaging Modality**    | White-light endoscopy (WLE) and narrow-band imaging (NBI) frames           |
| **🏥 Source Institutions** | Baerum Hospital (Norway), Karolinska University Hospital (Sweden)          |
| **📦 File Structure**      | 27 class-labeled directories + Google Drive download (~1.81 GB compressed) |
| **👨‍⚕️ Annotation**       | Expert endoscopist-verified labels                                         |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification of gastrointestinal findings
- **Number of Classes**: 2️⃣7️⃣ organized into four conceptual groups:

**🔍 Anatomical Landmarks **(10 classes)
| Class | Image Count | Description |
|-------|-------------|-------------|
| Cecum | 113 | Ileocecal region identification |
| Duodenal bulb | 205 | First part of duodenum |
| Gastroesophageal_junction_normal z-line | 330 | GEJ landmark |
| Ileocecal valve | 200 | Valve between ileum and cecum |
| Pylorus | 393 | Gastric outlet |
| Retroflex rectum | 67 | Rectal view in retroflexion |
| Small bowel_terminal ileum | 846 | Distal small intestine |
| Normal esophagus | 140 | Healthy esophageal mucosa |
| Normal stomach | 969 | Healthy gastric mucosa |
| Normal mucosa and vascular pattern in the large bowel | 1,467 | Healthy colonic mucosa |

**⚠️ Pathological Findings **(11 classes)
| Class | Image Count | Description |
|-------|-------------|-------------|
| Angiectasia | 17 | Vascular ectasia/bleeding source |
| Barretts esophagus | 95 | Metaplastic esophageal epithelium |
| Blood in lumen | 171 | Active or recent hemorrhage |
| Colon diverticula | 29 | Colonic outpouchings |
| Colorectal cancer | 139 | Malignant colonic lesions |
| Erythema | 15 | Mucosal inflammation/redness |
| Esophageal varices | 7 | Dilated submucosal veins |
| Esophagitis | 107 | Esophageal inflammation |
| Gastric polyps | 65 | Gastric mucosal protrusions |
| Mucosal inflammation large bowel | 29 | Colonic inflammatory changes |
| Ulcer | 6 | Mucosal defect with fibrinous base |

**🩺 Polyp-Related Interventions **(5 classes)
| Class | Image Count | Description |
|-------|-------------|-------------|
| Colon polyps | 820 | Untreated colonic polyps |
| Dyed-lifted-polyps | 141 | Polyps prepared for resection |
| Dyed-resection-margins | 246 | Post-resection margin assessment |
| Resected polyps | 92 | Removed polyp specimens |
| Resection margins | 25 | Margins after polypectomy |

**🛠️ Procedural/Accessory **(1 class)
| Class | Image Count | Description |
|-------|-------------|-------------|
| Accessory tools | 1,266 | Endoscopic instruments, caps, clips |

**📊 Class Distribution Summary**:

| Category                                | Total Images | % of Dataset |
|-----------------------------------------|--------------|--------------|
| Normal Findings                         | ~2,576       | ~32.2%       |
| Pathological Findings                   | ~588         | ~7.4%        |
| Polyp-Related                           | ~1,324       | ~16.6%       |
| Accessory Tools                         | ~1,266       | ~15.8%       |
| Anatomical Landmarks (excluding normal) | ~2,246       | ~28.1%       |
| **Total**                               | **~8,000**   | **100%**     |

> **ℹ️ Note**: Significant class imbalance exists (e.g., Ulcer: n=6 vs. Normal mucosa large bowel: n=1,467). Stratified
> sampling or class-weighted loss functions are strongly recommended.

#### 💡 Usage Notes

- ✅ Suitable for benchmarking endoscopic image classification and computer-aided diagnosis (CAD) systems
- ✅ Multi-institutional sourcing (Norway/Sweden) supports cross-center generalization studies
- ✅ Expert-annotated labels enhance clinical validity for translational research
- ✅ Includes procedural and post-intervention classes for comprehensive workflow modeling
- 📚 Required to cite the original Kaggle repository and associated publications when using this dataset
- 🔐 Distributed under CC BY 4.0; attribution required for redistribution or adaptation

#### ⚠️ Usage Considerations

| Aspect                            | Recommendation                                                                                                           |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| **🔍 Severe Class Imbalance**     | Apply class-weighted cross-entropy loss, focal loss, or oversampling for rare classes (e.g., Ulcer, Esophageal varices)  |
| **🎨 Image Resolution Variance**  | Endoscopy frames vary in resolution; standardize to fixed dimensions (e.g., 224×224) prior to training                   |
| **🧪 Clinical Context Awareness** | Some classes represent procedural states (e.g., dyed-lifted-polyps); ensure task alignment with research objectives      |
| **🔐 Ethical Compliance**         | Dataset contains de-identified clinical imagery; adhere to institutional review requirements for derivative works        |
| **🧭 Domain Generalization**      | Sourced from two European centers; validate on external cohorts (e.g., Asian, North American) before clinical deployment |
| **📦 Data Organization**          | Class directories include "Accessory tools"; consider excluding or treating as auxiliary class depending on task         |

#### 💡 Suggested Preprocessing Pipeline

1. **Download and extract**: Access via Google Drive link; unzip into structured directory preserving class subfolders.
2. **Filter optional classes**: Optionally exclude "Accessory tools" if focus is purely on diagnostic classification.
3. **Standardize geometry**: Resize all images to uniform dimensions (e.g., 256×256 or 512×512) while preserving aspect
   ratio.
4. **Color normalization**: Apply histogram equalization or adaptive contrast enhancement to mitigate endoscope-specific
   color variation.
5. **Class-aware augmentation **(training only): Incorporate rotation, flipping, and mild photometric jittering; apply
   stronger augmentation to underrepresented classes.
6. **Stratified splitting**: Partition data by class to maintain distribution balance; ensure no patient-level leakage
   if metadata permits.
7. **Evaluation metrics**: Report macro-averaged precision, recall, and F1-score alongside per-class metrics to account
   for imbalance; consider hierarchical evaluation grouping related classes.

#### 🔗 Associated Resources

- **Kaggle Repository**: https://www.kaggle.com/datasets/orvile/gastrovision-gastrointestinal-disease-detection
- **Google Drive Download**: https://drive.google.com/drive/folders/1T35gqO7jIKNxC-gVA2YVOMdsL7PSqeAa
- **Related Datasets**:
    - [Kvasir-V2](https://datasets.simula.no/kvasir-v2/) (8,000 GI images, 8 classes)
    - [Kvasir-SEG](https://datasets.simula.no/kvasir-seg/) (Polyp segmentation benchmark)
    - [HyperKvasir](https://datasets.simula.no/hyper-kvasir/) (Multi-label GI classification)
- **Contributors**: Debesh Jha, Vanshali Sharma, Michael Riegler, Pål Halvorsen, Ulas Bagci

#### 📚 Citation

If you use this dataset, please cite:

```bibtex
@dataset{jha2024gastrovision,
    author = {Jha, Debesh and Sharma, Vanshali and Riegler, Michael and Halvorsen, P{\aa}l and Bagci, Ulas},
    title = {GastroVision: Gastrointestinal Disease Detection},
    year = {2024},
    publisher = {Kaggle},
    url = {https://www.kaggle.com/datasets/orvile/gastrovision-gastrointestinal-disease-detection},
    note = {Accessed: May 08, 2026}
}
```

---


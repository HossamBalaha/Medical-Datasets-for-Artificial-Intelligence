### 🦴 BTXRD: Bone Tumor X-ray Radiograph Dataset

**Study**: Yao, S., Huang, Y., Wang, X., Zhang, Y., Paixao, I. C., Wang, Z., ... & Song, J. (2025). A radiograph dataset
for the Classification, Localization, and segmentation of primary bone tumors. Scientific data, 12(1), 88.

[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                              |
|-------------------------|----------------------------------------------------------------------|
| **📛 Title**            | BTXRD: Bone Tumor X-ray Radiograph Dataset                           |
| **🔗 Source**           | https://doi.org/10.6084/m9.figshare.27865398                         |
| **🦴 Target Organ**     | Bone (appendicular and axial skeleton)                               |
| **📅 Last Accessed**    | March 28, 2026                                                       |
| **🎯 Supported Tasks**  | 🏷️ Classification, 🎭 Segmentation, 📍 Localization                 |
| **📐 Image Size**       | Different sizes (to be standardized)                                 |
| **📁 Data Format**      | JPEG (.jpeg) for images, LabelMe-format JSON (.json) annotations     |
| **👥 Demographics**     | ✅ Age (3-88 yrs), Gender (M/F), Imaging center (inside dataset.xlsx) |
| **🔄 Train/Test Split** | ❌ Not provided (user-defined partitioning recommended)               | 

#### 📊 Dataset Composition

| Category               | Details                                                              |
|------------------------|----------------------------------------------------------------------|
| **🖼️ Total Images**   | 3,746 radiographs (IMG000001-IMG003746)                              |
| **🏥 Imaging Centers** | 3 contributing institutions (coded as `center`: 1, 2, 3)             |
| **🧒 Age Range**       | 1-88 years (pediatric to geriatric coverage)                         |
| **⚧ Gender Balance**   | Both Male (M) and Female (F); distribution requires full enumeration |

#### 🦴 Anatomical Coverage

| Region          | Structures Included                                |
|-----------------|----------------------------------------------------|
| **Upper Limb**  | Humerus, Radius, Ulna, Shoulder/Elbow/Wrist joints |
| **Lower Limb**  | Femur, Tibia, Fibula, Foot, Hip/Knee/Ankle joints  |
| **Pelvis**      | Hip bone, Hip joint                                |
| **View Angles** | Frontal, Lateral, Oblique projections              |

#### 🎗️ Tumor Annotation Schema

| Label Category      | Specific Classes                                                                                                                         |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| **Malignancy**      | `benign`, `malignant`, `tumor` (binary/multi-label flags)                                                                                |
| **Benign Types**    | Osteochondroma, Multiple osteochondromas, Simple bone cyst, Giant cell tumor, Osteofibroma, Synovial osteochondroma, Other benign tumors |
| **Malignant Types** | Osteosarcoma, Other malignant tumors (`other mt`)                                                                                        |

#### 🗂️ Annotation Format (LabelMe JSON)

```json
{
  "version": "5.4.1",
  "shapes": [
    {
      "label": "other mt",
      "shape_type": "polygon",
      "points": [
        [
          x1,
          y1
        ],
        [
          x2,
          y2
        ],
        ...
      ],
      "group_id": null
    },
    {
      "label": "other mt",
      "shape_type": "rectangle",
      "points": [
        [
          x_min,
          y_min
        ],
        [
          x_max,
          y_max
        ]
      ]
    }
  ],
  "imagePath": "IMG000001.jpeg",
  "imageWidth": 3213,
  "imageHeight": 2397
}
```

#### ⚠️ Usage Considerations

| Aspect                       | Recommendation                                                                     |
|------------------------------|------------------------------------------------------------------------------------|
| **🔍 Class Imbalance**       | Malignant cases (e.g., osteosarcoma) are rarer; apply stratified sampling          |
| **🧭 Multi-label Cases**     | Images may contain multiple tumor types or anatomical regions; handle accordingly  |
| **📐 Spatial Normalization** | Raw images vary in resolution; resize/normalize before model ingestion             |
| **🔐 Ethical Compliance**    | Dataset contains patient-derived data; adhere to institutional review requirements |
| **🧪 Baseline Splits**       | Consider center-stratified or age-stratified splits to ensure generalizability     |

#### 💡 Suggested Preprocessing Pipeline

1. **Parse metadata**: Load `dataset.xlsx` to extract demographic and label information per `image_id`.
2. **Link annotations**: Match each JPEG with its corresponding LabelMe JSON for segmentation masks.
3. **Standardize geometry**: Resize images to a fixed resolution (e.g., 512x512 or 1024x1024) while preserving aspect
   ratio.
4. **Encode labels**: Convert one-hot or multi-hot vectors for classification; rasterize polygons for segmentation
   masks.
5. **Stratify splits**: Partition data by center, age group, or tumor type to mitigate domain shift.

---


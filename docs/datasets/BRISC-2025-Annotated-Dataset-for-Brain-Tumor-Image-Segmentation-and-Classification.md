### 🧠 BRISC 2025: Annotated Dataset for Brain Tumor Image Segmentation and Classification

**Study**: Fateh, A., Rezvani, Y., Moayedi, S., Rezvani, S., Fateh, F., Fateh, M., & Abolghasemi, V. (2026). BRISC:
Annotated dataset for brain tumor segmentation and classification. Scientific Data.

[🔝 Back to Summary](https://HossamBalaha.github.io/Medical-Datasets-for-Artificial-Intelligence/)

| Metadata                | Details                                                                             |
|-------------------------|-------------------------------------------------------------------------------------|
| **📛 Title**            | BRISC 2025: Annotated Dataset for Brain Tumor Image Segmentation and Classification |
| **🔗 Source**           | https://www.kaggle.com/datasets/briscdataset/brisc2025/                             |
| **🧠 Target Organ**     | Brain                                                                               |
| **📅 Last Accessed**    | March 28, 2026                                                                      |
| **🎯 Supported Tasks**  | 🏷️ Classification, 🎭 Segmentation                                                 |
| **📐 Image Size**       | 512 x 512 pixels                                                                    |
| **📁 Data Format**      | JPG (.jpg) for images, PNG (.png) for masks                                         |
| **👥 Demographics**     | ❌ Not included                                                                      |
| **🔄 Train/Test Split** | ✅ Yes                                                                               |

#### 🏷️ Classification Task Details

- **Task Type**: Multiclass classification
- **Number of Classes**: 4️⃣
    - 🧠 Glioma
    - 🧠 Meningioma
    - ✅ No tumor
    - 🧠 Pituitary tumor

**📊 Training Set Distribution**:

- 🧠 Glioma: 1,147 images
- 🧠 Meningioma: 1,329 images
- ✅ No tumor: 1,067 images
- 🧠 Pituitary: 1,457 images

**📊 Test Set Distribution**:

- 🧠 Glioma: 254 images
- 🧠 Meningioma: 306 images
- ✅ No tumor: 140 images
- 🧠 Pituitary: 300 images

#### 🎭 Segmentation Task Details

- **Task Type**: Binary segmentation (tumor vs. background)
- **Mask Format**: ⚪ White-on-⚫ Black binary masks

**📊 Training Set**:

- 🖼️ Images: 3,933
- 🎭 Corresponding Masks: 3,933
- 📁 Organization: Separated folders for images and masks

**📊 Test Set**:

- 🖼️ Images: 860
- 🎭 Corresponding Masks: 860
- 📁 Organization: Separated folders for images and masks

#### 💡 Usage Notes

- ✅ Suitable for benchmarking multi-task learning frameworks
- ✅ Compatible with standard deep learning pipelines for medical imaging
- 📚 Recommended to cite the original Figshare repository when using this dataset in publications

---


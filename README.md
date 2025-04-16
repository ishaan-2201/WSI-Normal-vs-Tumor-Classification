# 🧬 Tumor vs Normal Classification using Whole Slide Images (WSIs)

This project aims to classify Whole Slide Images (WSIs) from the TCGA (The Cancer Genome Atlas) into **Normal** and **Tumor** categories using deep learning. The images were preprocessed into smaller patches using **QuPath**, and a CNN model was trained using **PyTorch** and **ResNet18** architecture.

---

## 📂 Project Overview

### ✅ Steps Followed:

1. **Data Collection**
   - WSIs of tumor and normal tissue downloaded from the [GDC TCGA Portal](https://portal.gdc.cancer.gov/).
2. **Patch Generation**

   - Created patches (512×512) using **QuPath**.
   - Applied tissue detection to avoid background.
   - Saved filtered patches in labeled folders (`/normal`, `/tumor`).

3. **Dataset Split**

   - Used `Split_Dataset.ipynb` to split into:
     - 70% training
     - 15% validation
     - 15% testing

4. **Model Training**

   - Used pretrained `ResNet18` model.
   - Trained using PyTorch.
   - Achieved test accuracy ~88%.

5. **Evaluation Metrics**
   - Precision, Recall, F1-Score
   - Confusion Matrix

---

## 🧠 Tools Used

- QuPath
- Python, PyTorch, torchvision
- scikit-learn (for evaluation)
- Google Colab (recommended for training)

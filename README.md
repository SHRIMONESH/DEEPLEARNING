# 🔬 Deep Learning for Early Detection of Skin Cancer

## Project Overview

This project details the development and evaluation of a deep learning model for the automated **binary classification of skin lesions** as either **Benign** or **Malignant**. The system utilizes a state-of-the-art **Convolutional Neural Network (CNN)**, specifically **ResNet50** via **transfer learning**, to provide an accurate, reliable, and clinically-aware diagnostic aid.

---

## Key Features & Objectives

The primary goals of this project were centered on creating a clinically useful tool:

* [cite_start]**High Accuracy:** Achieve strong classification performance by leveraging a pre-trained **ResNet50** backbone[cite: 43].
* [cite_start]**Clinical Applicability:** Strategically optimize the model to prioritize **Recall (Sensitivity)**, aiming to **minimize False Negatives (missed cancers)**[cite: 44, 106].
* [cite_start]**Interpretability (Trustworthy AI):** Ensure the model's decision-making is transparent using **Grad-CAM heatmaps**[cite: 45, 112].

---

## 💻 Technical Details

### Model Architecture

* [cite_start]**Backbone:** **ResNet50**[cite: 24, 83].
    * [cite_start]**Method:** **Transfer Learning** (pre-trained on ImageNet)[cite: 24, 83, 84].
* **Custom Classifier Head:** A layered structure built on the 2048-Feature Vector from the ResNet50 Global Average Pooling (GAP) output .
* [cite_start]**Implementation:** Convolutional Neural Network (CNN)[cite: 81].

### Methodology

| Component | Detail |
| :--- | :--- |
| **Dataset** | [cite_start]"Kaggle-Skin Cancer (Malignant vs Benign)"[cite: 25, 65]. |
| **Dataset Size** | [cite_start]3,297 dermoscopic images (1,800 Benign, 1,497 Malignant)[cite: 25, 67, 68]. |
| **Preprocessing** | [cite_start]Image resizing (e.g., $224 \times 224$ pixels) and pixel normalization[cite: 70, 71]. |
| **Data Augmentation** | [cite_start]Random rotations, flips, brightness/contrast variations to enhance generalization[cite: 26, 73, 75]. |
| **Loss Function** | [cite_start]Binary Cross-Entropy (BCE)[cite: 26, 91]. |
| **Optimizer** | [cite_start]AdamW with a sophisticated learning rate scheduling strategy[cite: 26, 93]. |
| **Regularization** | [cite_start]Dropout and Weight Decay[cite: 26, 88]. |
*The comprehensive architecture is visualized in the project's transfer learning diagram .*

---

## 📊 Results and Performance

### Core Metrics

[cite_start]The model demonstrated **strong discriminatory power** as evidenced by the high Area Under the Curve (AUC)[cite: 27, 102].

| Metric | Result |
| :--- | :--- |
| **Validation Accuracy** | [cite_start]$\approx 92\%$ [cite: 27, 101] |
| **AUC (Area Under the Curve)** | [cite_start]**0.9752** [cite: 27, 102] |
| **F1-Score (Optimal)** | 0.924 (at threshold 0.200)  |

### Threshold Optimization for Clinical Safety

[cite_start]To mitigate the clinical risk associated with **False Negatives (missed cancers)**, a threshold optimization was performed, shifting from a default threshold (0.5) to a **High Recall Threshold (0.100)**[cite: 107, 108].

| Metric | Initial (Default 0.5) | Optimized (High Recall 0.100) | Improvement |
| :--- | :--- | :--- | :--- |
| **False Negatives** | [cite_start]33 [cite: 104] | [cite_start]**13** [cite: 110] | [cite_start]**$> 60\%$ Reduction** [cite: 28, 110] |
| **Recall (Sensitivity)** | 89.00% (at 0.5)  | [cite_start]**95.67%** [cite: 111] | Significantly increased |
![WhatsApp Image 2025-10-11 at 22 28 43_a8df2daa](https://github.com/user-attachments/assets/29b99040-b3fc-4879-b299-ef2e66148070)
![WhatsApp Image 2025-10-11 at 22 31 06_74be004c](https://github.com/user-attachments/assets/ea0deaea-dbf3-4fca-baed-798d15be6f96)
![WhatsApp Image 2025-10-11 at 22 23 58_bf17bae6](https://github.com/user-attachments/assets/a707e09b-8156-4f54-afde-73bcb67d41a8)


### Model Interpretability (Grad-CAM)

[cite_start]**Grad-CAM heatmaps** confirm the model's trustworthiness by visually demonstrating that it focuses on the **relevant pathological features within the lesion area** when making predictions, rather than relying on external artifacts[cite: 29, 113]. 
---
![WhatsApp Image 2025-10-13 at 09 00 10_ac065d7c](https://github.com/user-attachments/assets/1eaf69e2-f64e-4f69-9d86-6646be50643d)
![WhatsApp Image 2025-10-13 at 09 01 53_6889d9a7](https://github.com/user-attachments/assets/6ce31eca-1af0-409a-b639-4d0ca323b3cc)

## 🎓 Academic Details

* [cite_start]**Course:** 23ELC212 DEEPLEARNING [cite: 5]
* [cite_start]**Institution:** Amrita Vishwa Vidyapeetham, Coimbatore [cite: 1]
* [cite_start]**Department:** Electrical and Electronics Engineering [cite: 2]
* [cite_start]**Program:** B.Tech - Electrical and Computer Science Engineering [cite: 3]
* [cite_start]**Semester:** Third Year - V semester, October 2025 [cite: 7]

---

## Team

| Name | Roll Number |
| :--- | :--- |

| SHRI MONESH | [cite_start]CB.EN.U4ELC23054 [cite: 9] |

[cite_start]**Faculty-in-Charge:** Dr. T. Ananthan [cite: 11]

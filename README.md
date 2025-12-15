# Brain Tumor Classification
This repository presents a deep learning project for **multi-class classification of brain tumors from MRI images using transfer learning**.

The project focuses not only on performance, but also on model comparison and computational cost which are critical aspects in medical imaging applications.

---

## 📍 Problem description
Brain tumor diagnosis from MRI scans is a challenging task due to:
- high intra-class variability,
- visual similarity between different tumor types,
- limited dataset size.
  
The goal is to classify MRI images into **four classes**:

1) Glioma
  
2) Meningioma
   
3) Pituitary
   
4) No Tumor

---

## 📊 Dataset
**Source**: Kaggle - Brain MRI Tumor Dataset (https://www.kaggle.com/datasets/ahmedsorour1/mri-for-brain-tumor-with-bounding-boxes)

**Classes**: 4

**Image format**: RGB

**Image size**: resized to 224x224

---

## ⚙️ Experimental Setup
All experiments share the same training pipeline to ensure fair comparison.

**Framework**: PyTorch

**Architectures**: ResNet-18, ResNet-34

**Training**: early stopping method with LR scheduler and Adam optimization

![Pipeline](https://github.com/valeria-molino/Brain-Tumor-Classification/blob/main/Pipeline.png)

---

## 📈 Performance Results

| # | Model | Training | Accuracy | Confusion Matrix |
|---|----------|--------------|--------|
| 1 | ResNet-18 | Transfer Learning on the last layer | 0.85 | https://github.com/valeria-molino/Brain-Tumor-Classification/blob/main/Confusion_Matrix_ResNet18_TL.png |
| 2 | ResNet-24 | Transfer Learning on the last layer | 0.86 | https://github.com/valeria-molino/Brain-Tumor-Classification/blob/main/Confusion_Matrix_ResNet34_TL.png |
| 3 | **ResNet-18** | **From Scratch** | **0.95** | https://github.com/valeria-molino/Brain-Tumor-Classification/blob/main/Confusion_Matrix_ResNet18_FS.png |

---

## 🔎 Discussion

Although transfer learning is commonly preferred for small datasets, results show that:

- ImageNet features may not fully align with **MRI texture and intensity patterns**

- Training from scratch allows the model to learn **domain-specific representations**

- With proper regularization and early stopping, overfitting was effectively controlled

This highlights that **transfer learning is not always optimal**, especially when the source and target domains differ significantly.

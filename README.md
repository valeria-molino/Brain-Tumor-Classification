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

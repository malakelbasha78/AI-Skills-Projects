PlantVillage Dataset Preprocessing, Augmentation, and Handling Class Imbalance
This document explains the full workflow used to prepare the PlantVillage dataset for deep learning models. It includes steps from dataset download to preprocessing, augmentation, handling class imbalance, and data inspection.
1. Dataset Overview
• Source: PlantVillage Kaggle Dataset
• Number of classes: 39
• Total images after merging and cleaning duplicates: 54,996
• Dataset split: 70% train, 15% validation, 15% test

The dataset contains images of various plant species with both healthy and diseased leaves.
2. Dataset Download and Inspection
The dataset was downloaded using a specialized tool for Kaggle datasets. After download, the folder structure was verified to contain 'train' and 'validation' folders, and the number of images per class was inspected.
3. Merge Train and Validation Folders
• All images from the train and validation folders were combined into a single folder per class.
• This step simplifies preprocessing and avoids splitting issues.
• A backup of the original dataset was created to preserve the raw images.
4. Remove Duplicates
• Duplicate images were detected using a hash-based method.
• Any repeated images were removed to ensure that the dataset contains unique samples.
• Number of duplicates removed: 24
• Total images after cleaning: 54,996
5. Enhance Blurry Images
• Blurry images were detected using a measure of sharpness based on the Laplacian variance.
• Detected blurry images were enhanced using a sharpening filter.
• Number of blurry images enhanced: 3,485

This step improves image quality and ensures better learning for the model.
6. Data Splitting
• The dataset was split into training, validation, and test sets:
  - Train: 70% (38,497 images)
  - Validation: 15% (8,249 images)
  - Test: 15% (8,250 images)
• Each set maintains a representative distribution of all classes.
7. Data Augmentation
Augmentation was applied to training images to improve model generalization. The following transformations were used:
• Random horizontal and vertical flips
• Random rotation up to 30 degrees
• Color adjustment (brightness, contrast, saturation, hue)
• Random resized crop
• Resizing to 224x224 pixels
• Normalization using standard ImageNet statistics

Validation and test images were only resized and normalized without augmentation.
8. Handling Class Imbalance
• The number of images per class in the training dataset was calculated.
• Class weights were computed to balance the influence of each class during training.
• Weighted sampling was applied to ensure balanced class representation in each training batch.
9. Data Inspection
• Sample images were inspected before and after augmentation.
• Class labels, image shapes, and pixel value ranges were verified.
• This step ensures that the preprocessing and augmentation pipeline is correctly applied.
10. Summary
The preprocessing workflow ensures:
• Balanced class representation during training
• High-quality images with duplicates removed and blurry images enhanced
• Robust data augmentation to improve generalization
• Proper train-validation-test splitting for model evaluation

This pipeline makes the dataset ready for training deep learning models effectively.



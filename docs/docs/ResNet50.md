# Plant Disease Classification using ResNet50

## 1. Problem Overview
This project focuses on a real-world image classification problem: identifying plant leaf diseases from images.

## 2. Dataset Description
The [PlantVillage dataset](https://www.kaggle.com/datasets/emmarex/plantdisease) was used. It contains labeled RGB images across 39 disease classes, split into training and validation sets.

## 3. Data Preprocessing
- Removed corrupted images  
- Removed duplicate images using hashing  
- Preserved original train/validation split to avoid data leakage  
- Efficient data loading using `tf.data` pipelines  

## 4. Model Architecture
**Base Model:** ResNet50 (ImageNet pretrained)  

**Custom Head:**  
- Global Average Pooling  
- Batch Normalization  
- Dense (ReLU)  
- Dropout  
- Softmax output layer  

## 5. Training Strategy
- **Stage 1:** Feature extraction with frozen ResNet50  
- **Stage 2:** Fine-tuning last 25 layers with lower learning rate  

## 6. Optimization Techniques
- Data augmentation  
- Normalization  
- Dropout  
- Early stopping  
- Model checkpointing  

## 7. Training Results
Validation accuracy reached ~68% during initial training, with further improvement during fine-tuning.

## 8. Evaluation Metrics
- Accuracy  
- Precision (weighted)  
- Recall (weighted)  
- Confusion Matrix  

## 9. Model Interpretability
Grad-CAM was applied to visualize regions contributing to predictions.

## 10. GUI Integration
A Gradio-based GUI supports image upload and displays predictions with confidence scores.

<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/71fb55f3-3df8-437f-a7a4-79922bc5663b" />
<img width="1280" height="720" alt="image" src="https://github.com/user-attachments/assets/202ba37a-4f11-453f-a974-12bf1be26985" />




## 11. Summary
The system combines robust preprocessing, transfer learning, evaluation, interpretability, and deployment.

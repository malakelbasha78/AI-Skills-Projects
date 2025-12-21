# 📌 EfficientNetB3 Model Documentation

## Plant Disease Classification

---

## 🔹 Introduction

In this project, we used the **EfficientNetB3** model to classify plant leaf diseases from images.
The model takes a leaf image 🌿, analyzes its shape, color, texture, and disease spots, then predicts the disease class along with a confidence score.

The model is built using **Transfer Learning**, meaning we started from a pretrained model that was previously trained on millions of images, then fine-tuned it using our project dataset to specialize in plant disease classification.

---

## 🔹 Dataset Used

We used the **PlantVillage Dataset**, which is a well-known dataset in the field of plant disease classification.
It contains a large number of images covering different plant species and disease types, which helped the model achieve high accuracy.

### Dataset Preparation Steps:

* Splitting the dataset into **Training / Validation / Testing** sets
* Removing corrupted or invalid images
* Resizing all images to a unified input size

---

## 🔹 Preprocessing & Data Augmentation

Before training, several preprocessing steps were applied to improve model performance:

### Preprocessing:

* Image resizing to match EfficientNetB3 input requirements
* Image normalization to stabilize pixel value distributions

### Data Augmentation:

* Random image rotations
* Minor geometric transformations

These steps helped reduce **overfitting** and allowed the model to generalize better.

---

## 🔹 Why EfficientNetB3?

EfficientNetB3 was chosen because it:

* Achieves high accuracy with fewer parameters
* Maintains a good balance between performance and computational cost
* Excels at extracting fine-grained image features

This makes it suitable for complex image classification tasks such as plant disease detection.

---

## 🔹 EfficientNetB3 Model Architecture

We used a **pretrained EfficientNetB3** model and applied the following modifications:

* Freezing the base layers during initial training
* Replacing the classifier head to match the number of disease classes
* Applying **Dropout** to improve generalization
* Performing **Fine-Tuning** on the entire model to boost accuracy

### Training Configuration:

* **Loss Function:** CrossEntropy Loss
* **Optimizer:** Adam
* **Learning Rate Scheduling:**

  * ReduceLROnPlateau
  * CosineAnnealingLR

---

## 🔹 Training Process

During training, we monitored:

* Training Loss
* Validation Accuracy

The best model was selected based on validation performance, and training continued until performance stabilized.

---

## 🔹 Evaluation

After training, the model was evaluated on a separate **Test Set** to measure real-world performance.

### Evaluation Metrics:

* Accuracy
* Precision, Recall, and F1-score
* Confusion Matrix
* Classification Report

The results demonstrated that the model can effectively distinguish between different plant diseases.

---

## 🔹 Grad-CAM (Model Explainability)

We applied **Grad-CAM** to visualize and interpret the model’s predictions.

Grad-CAM generates:

* Heatmaps over the input leaf images
* Highlights the regions the model focused on during prediction

🔴 Red regions indicate the most influential areas contributing to the decision.

This confirms that the model relies on meaningful disease patterns rather than random features.

---

## 🔹 Conclusion

The **EfficientNetB3** model proved to be highly effective for plant disease classification due to its:

* High accuracy
* Strong feature extraction capability
* Efficient computational performance

Combined with **Grad-CAM**, the model becomes:

* Accurate
* Interpretable
* Suitable for real-world agricultural applications 🌱

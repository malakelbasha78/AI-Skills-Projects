📌 Plant Disease Classification using MobileNetV2
🔹 Introduction

In this project, we used the MobileNetV2 deep learning model to classify plant leaf diseases from images.
The model takes a leaf image, analyzes its visual features such as shape, color, and disease spots, and predicts the type of disease associated with the plant.

The model is built using Transfer Learning, where we started from a pretrained MobileNetV2 model that was originally trained on millions of images.
We then fine-tuned it using our dataset to specialize in plant disease classification.

🔹 Dataset Used

We used the PlantVillage Dataset, which is one of the most widely used datasets in the field of plant disease classification.

The dataset includes:

Multiple plant species

Healthy and diseased leaf images

A large number of classes representing different plant diseases

This diversity helped the model learn robust and meaningful features and achieve high accuracy.

Dataset Preparation Steps:

Splitting the dataset into Training / Validation / Testing sets

Removing corrupted or invalid images

Resizing all images to a unified input size

🔹 Preprocessing & Data Augmentation

Before training, several preprocessing and augmentation techniques were applied to improve the model’s performance and generalization.

Preprocessing:

Resizing images to match the model’s required input size

Normalizing pixel values to ensure proper distribution

Data Augmentation:

Random rotations

Minor geometric transformations

These steps help reduce overfitting and allow the model to learn general visual patterns instead of memorizing training images.

🔹 Why MobileNetV2?

We chose MobileNetV2 because it is:

Lightweight and computationally efficient 

Very fast during inference

Suitable for mobile and real-time applications

Able to achieve strong performance despite its small size

This makes MobileNetV2 an excellent choice, especially for mobile deployment and TFLite applications.

🔹 MobileNetV2 Model Architecture

We used a pretrained MobileNetV2 model and applied the following steps:

Freezing the base feature extraction layers

This allows the model to reuse previously learned low-level and mid-level visual features such as edges, textures, and shapes.

Replacing the final classifier head

The last fully connected layer was modified to match the number of plant disease classes in our dataset.

Fine-Tuning

After training the classifier, we unfroze the model and fine-tuned it to improve overall performance.

Training Setup:

Loss Function: CrossEntropy Loss

Optimizer: Adam

Training Strategy:

Monitor training loss

Track validation accuracy

Select the best model based on validation performance

🔹 Evaluation

After training, the model was evaluated using a separate test set to ensure reliable and unbiased performance.

Evaluation Metrics:

Accuracy

Confusion Matrix

Classification Report (Precision, Recall, F1-score)

The results showed that the model is able to effectively distinguish between different plant diseases with high accuracy.

🔹 Grad-CAM (Model Explainability)

To better understand the model’s decisions, we applied Grad-CAM (Gradient-weighted Class Activation Mapping).

Grad-CAM provides:

Heatmaps over the input leaf images

Visualization of the regions the model focuses on when making predictions

🔴 Red regions indicate the most influential areas contributing to the model’s decision.

This confirms that the model is not making random predictions, but is actually focusing on the infected or relevant parts of the leaf.


![WhatsApp Image 2025-12-22 at 12 07 36 PM](https://github.com/user-attachments/assets/39bd3784-9a20-4bad-bd0f-6151a3abe65d)



🔹 Conclusion

The MobileNetV2-based model proved to be a strong solution for plant disease classification because it:

Achieves high accuracy relative to its size

Is fast and lightweight

Is suitable for mobile and real-world deployment

Successfully learns meaningful plant disease patterns

With the addition of Grad-CAM, the model becomes:

Accurate ✅

Interpretable 

Practical for real-world agricultural applications 

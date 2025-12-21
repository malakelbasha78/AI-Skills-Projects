📌 MobileNetV2 Model Documentation
Plant Disease Classification
🔹 Introduction

In this project, we used the MobileNetV2 model to classify plant leaf diseases from images.
The idea of the model is to take a leaf image 🌿, analyze its shape, color, and disease spots, and then predict the type of disease along with a confidence score.

The model is built using Transfer Learning, meaning we started from a pretrained model that had already been trained on millions of images, then fine-tuned it using our project dataset to specialize in plant disease classification.

🔹 Dataset Used

We used the PlantVillage Dataset, as it is one of the most well-known datasets in the field of plant disease classification.
It contains a large number of images for different plant species and diseases, which helped the model achieve high accuracy.

Dataset Preparation Steps:

Splitting the dataset into Training / Validation / Testing sets

Removing corrupted or invalid images

Resizing all images to a unified size

🔹 Preprocessing & Data Augmentation

Before training, several preprocessing steps were applied to improve the model’s performance:

Preprocessing:

Image resizing to match the model’s input size

Normalization to ensure proper pixel value distribution

Data Augmentation:

Simple image rotations

Minor geometric transformations

These steps helped reduce overfitting and allowed the model to learn more general patterns instead of memorizing the training images.

🔹 Why MobileNetV2?

We chose MobileNetV2 because it is:

Very lightweight and fast ⏩

Suitable for mobile and real-time applications

Able to achieve good accuracy despite its small size

This makes it an excellent choice, especially for the Bonus (TFLite / Mobile Deployment) part.

🔹 MobileNetV2 Model Architecture

We used a pretrained MobileNetV2 model and applied the following steps:

Freezing the base layers at the beginning of training

Modifying the final layer (Classifier Head) to match the number of disease classes

After the classifier was well trained, we applied Fine-Tuning to the entire model to improve accuracy

Training Setup:

Loss Function: CrossEntropy Loss

Optimizer: Adam

Training for a suitable number of epochs until performance stabilized

During training, we monitored:

Training Loss

Validation Accuracy

The best model was selected based on validation performance.

🔹 Evaluation

After training, the model was evaluated using a separate Test Set to ensure reliable performance.

Evaluation Metrics:

Accuracy

Confusion Matrix

Classification Report

The results showed that the model is able to distinguish between different plant diseases effectively.

🔹 Grad-CAM (Explainability)

We used Grad-CAM to explain the model’s decisions, which is a very important part of the project.

Grad-CAM provides:

Heatmaps over the leaf images

Visualization of the regions the model focused on during prediction

🔴 Red regions indicate the most influential areas in the model’s decision.

This confirms that the model is not making random predictions, but is actually focusing on the infected parts of the leaf.

🔹 Conclusion

The MobileNetV2 model proved to be an excellent choice because it:

Achieves high accuracy relative to its size

Is fast and lightweight

Is suitable for mobile applications

Successfully learns plant disease patterns

With the addition of Grad-CAM, the model becomes:

Accurate

Interpretable

Suitable for real-world agricultural applications

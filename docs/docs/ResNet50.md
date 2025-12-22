📌 ResNet50 Model Documentation

Plant Disease Classification

🔹 Introduction

In this project, we used the ResNet50 model to classify plant leaf diseases from images.
The model takes a leaf image , analyzes visual patterns such as shape, color variations, texture, and disease spots, then predicts the disease class along with a confidence score.

The model is based on Transfer Learning, where we utilized a ResNet50 model pretrained on ImageNet and fine-tuned it on the PlantVillage dataset to specialize in plant disease classification.

🔹 Dataset Used

We used the PlantVillage Dataset, a widely recognized dataset for plant disease classification tasks.
It contains labeled RGB images covering multiple plant species and disease categories, making it suitable for training deep learning models.

Dataset Preparation Steps:

Using the original training and validation split to avoid data leakage

Removing corrupted images

Removing duplicate images using image hashing techniques

Efficient data loading using optimized pipelines

🔹 Preprocessing & Data Augmentation

To improve the robustness and generalization of the model, several preprocessing steps were applied before training.

Preprocessing:

Image resizing to match ResNet50 input size

Image normalization for stable training

Data Augmentation:

Random transformations applied during training

Augmentation helped reduce overfitting and improved model performance

🔹 Why ResNet50?

ResNet50 was selected because it:

Uses residual connections to prevent vanishing gradients

Performs well on deep image classification tasks

Is a proven architecture for transfer learning

Effectively captures complex visual patterns

These advantages make ResNet50 suitable for detecting subtle disease features in plant leaves.

🔹 ResNet50 Model Architecture

A pretrained ResNet50 model was used as the backbone with the following modifications:

Base ResNet50 loaded with ImageNet weights

Global Average Pooling layer added

Batch Normalization for stable training

Fully connected Dense layer with ReLU activation

Dropout layer to reduce overfitting

Softmax output layer matching the number of disease classes

Training Strategy:

Freezing the base model during initial training

Fine-tuning the last 25 layers using a lower learning rate

🔹 Training Configuration

Loss Function: Categorical Crossentropy

Optimizer: Adam

Regularization Techniques:

Dropout

Early Stopping

Model Checkpointing

🔹 Training Process

During training, the following metrics were monitored:

Training Loss

Validation Accuracy

The training process was divided into two stages: feature extraction and fine-tuning.
The best model was selected based on validation performance.

🔹 Evaluation

After training, the model was evaluated to measure its performance.

Evaluation Metrics:

Accuracy

Precision (weighted)

Recall (weighted)

Confusion Matrix

The model showed consistent performance across multiple disease classes.

🔹 Grad-CAM (Model Explainability)

Grad-CAM was applied to interpret the model’s predictions visually.

Grad-CAM produces:

Heatmaps over input leaf images

Highlights the regions the model focused on while making predictions

 Red areas indicate regions with the highest influence on the model’s decision, confirming that the model focuses on meaningful disease patterns.

🔹 GUI Integration

A Gradio-based graphical user interface (GUI) was implemented to enhance usability.

The GUI allows users to:

Upload plant leaf images

View predicted disease classes

See confidence scores

🔹 Conclusion

The ResNet50 model demonstrated strong performance in plant disease classification due to its:

Deep residual architecture

Reliable transfer learning capabilities

Effective feature extraction

When combined with Grad-CAM and a user-friendly GUI, the system becomes:

Accurate

Interpretable

Practical for real-world agricultural applications

# AI-Skills-Projects
AI project
# 🌱 Plant Disease Classification

## Overview
This project focuses on **classifying plant leaf diseases** from images using **Deep Learning and AI techniques**.  
The goal is to automatically detect plant diseases to help farmers and researchers monitor plant health efficiently.

---

## Project Structure
Plant-Disease-Classification/
├── data/
│   └── new_dataset_ai.ipynb       # Dataset processing & exploration
├── docs/
│   ├── EfficientNetB3.md
│   ├── ResNet50.md
│   └── mobilenetv2.md
├── gui/
│   ├── app.py                     # Main GUI application
│   └── ui_design.py                # GUI design scripts
├── models/
│   ├── EfficientNetB3/
│   │   └── EfficientNetB3.ipynb
│   ├── MobileNetV2/
│   │   └── MobileNetV2.ipynb
│   └── ResNet50/
│       └── ResNet50.ipynb
└── README.md                       # This file

---

## Models Used
- **MobileNetV2**  
- **EfficientNetB3**  
- **ResNet50**  

All models are trained using **Transfer Learning** on the plant leaf dataset.

---

## GUI
The project includes a **Graphical User Interface (GUI)** that allows users to:
- Upload a plant leaf image
- Predict the disease using the trained models
- Display results interactively

---

## Dataset
- `new_dataset_ai.ipynb` contains dataset processing and exploration.  
- Ensure the dataset images are placed in the `data/` folder before running the models.

---

## Tools & Technologies
- Python  
- TensorFlow / Keras  
- Google Colab  
- NumPy, Pandas, Matplotlib  
- GUI: Tkinter (app.py, ui_design.py)  
- GitHub  

---

## How to Run
1. Open the dataset notebook `data/new_dataset_ai.ipynb` to preprocess and explore data.  
2. Train or load any model from `models/` folder.  
3. Run the GUI:  
   ```bash
   python gui/app.py


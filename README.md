# Brain Tumor Classification from Brain MRI Dataset

This project implements a deep learning approach to classify brain MRI images into four categories:
- **glioma_tumor**
- **no_tumor**
- **meningioma_tumor**
- **pituitary_tumor**

The models are built using EfficientNetB0 and EfficientNetB3, leveraging transfer learning from pre-trained ImageNet weights. A Streamlit web application is provided for real-time inference.

---

## Overview

The project includes two main components:

1. **Model Training & Evaluation**  
   - **Data Loading & Preprocessing:** MRI images are loaded, resized, and normalized. Data augmentation is applied to improve generalization.
   - **Model Architecture:** EfficientNetB0 and EfficientNetB3 are fine-tuned with additional custom layers for classification.
   - **Training:** The models are trained using a combination of callbacks (e.g., TensorBoard, ReduceLROnPlateau, and ModelCheckpoint) to monitor progress and save the best-performing model.
   - **Evaluation:** Model performance is evaluated using confusion matrices and classification reports.

2. **Streamlit Web Application**  
   - **User Interface:** Users can upload an MRI image through the web interface.
   - **Inference:** The uploaded image is preprocessed in the same way as during training, and predictions are made using the saved models.
   - **Display:** The app shows the predicted tumor type along with the confidence levels, and visualizes prediction probabilities in a bar chart.

---

## Project Structure

```plaintext
├── main.py               # Training and evaluation code
├── streamlit_app.py      # Streamlit interface for model inference
├── requirements.txt      # List of project dependencies
└── README.md             # This file

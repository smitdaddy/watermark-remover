🖼️ Watermark Removal using Deep Learning

A Computer Vision Project for Image Restoration

📌 Overview

This project demonstrates how to remove watermarks from images using deep learning, implemented in Python using TensorFlow/Keras.
The workflow includes dataset preparation, preprocessing, model building, training, validation, and evaluation.
The notebook (watermarkRemoval_ISE2.ipynb) provides a complete, reproducible pipeline for image restoration.

🚀 Features

Automatic dataset extraction from Google Drive

Image preprocessing and augmentation

Paired watermarked vs. clean image dataset loading

Deep learning model for watermark removal using:

Convolutional Neural Networks (CNNs)

UNet-style encoder–decoder architecture (if used)

Training with EarlyStopping & performance monitoring

Visualization of:

Input watermarked images

Ground-truth clean images

Model-generated watermark-removed outputs

📂 Project Structure
├── watermarkRemoval_ISE2.ipynb     # Main project notebook
├── dataset/
│   ├── wm-nowm/
│   │   ├── wm/                      # Watermarked images
│   │   └── nowm/                    # Clean (ground-truth) images
└── README.md

🛠️ Technologies Used
Programming & Libraries

Python

NumPy

Matplotlib

OpenCV

TensorFlow / Keras

Google Colab (for training & GPU support)

📦 Dataset

The dataset consists of two folders inside /dataset/wm-nowm/:

Folder	Description
wm/	Contains images with watermarks
nowm/	Contains clean / watermark-free images, used as ground truth

Dataset is unzipped and prepared automatically in the notebook.

🧠 Model Architecture

A CNN-based image-to-image model is used for predicting clean images from watermarked inputs.

General architecture pipeline:

Input Layer — watermarked image

Encoder — convolution + downsampling

Bottleneck

Decoder — upsampling + skip connections

Output Layer — predicted clean image

Model is trained using:

Loss Function: Mean Squared Error (MSE)

Optimizer: Adam

Metrics: Validation loss

Callbacks: EarlyStopping

🏋️ Training

Training steps include:

Loading watermarked & clean image pairs

Normalizing and resizing images

Splitting into training & validation sets

Model training with GPU acceleration

Saving trained model weights

📊 Results & Evaluation

During evaluation, the notebook displays:

Watermarked input

Ground-truth clean image

Model output (watermark removed)

Performance is judged visually and via loss metrics.

▶️ How to Run the Project
1. Upload the notebook to Google Colab
Open watermarkRemoval_ISE2.ipynb.
2. Mount Google Drive
The notebook includes:
from google.colab import drive
drive.mount('/content/drive')

3. Ensure dataset ZIP is in Drive
Place your dataset ZIP at:
/content/drive/MyDrive/Dataset.zip

4. Run all cells
The notebook will:


Extract the dataset


Build the model


Train it


Display results



📈 Future Improvements


Add GAN-based architecture (CycleGAN or Pix2Pix)


Support for transparent watermarks


Exporting a lightweight .tflite model for mobile apps


Integrate a web UI for watermark removal



✒️ Authors
Smit Patil, Umer Mir and Khizer Ansari
Computer Engineering Students
Deep Learning & Computer Vision Enthusiasts


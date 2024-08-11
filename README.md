
# Pneumonia Detection App

## Overview

This application utilizes a deep learning model to detect pneumonia from chest X-ray images. Built with TensorFlow, Keras, and PyQt5, it provides a user-friendly interface for uploading X-ray images and obtaining predictions on whether the image shows signs of pneumonia.

## Features

- **Upload Image**: Allows users to select and upload chest X-ray images.
- **Prediction**: Provides a prediction on whether the uploaded image indicates normal conditions or signs of pneumonia.
- **Voice Feedback**: Uses text-to-speech to provide spoken feedback on the prediction result.

## Requirements

Ensure you have the following Python packages installed:

- TensorFlow
- Keras
- NumPy
- Matplotlib
- PyQt5
- Pillow
- pywin32 (for text-to-speech functionality)

You can install the required packages using `pip`:

```bash
pip install tensorflow keras numpy matplotlib pyqt5 pillow pywin32
```

## Setup

1. **Download the Pre-trained Model**: Ensure you have the model file `chest_xray.h5`. This file contains the trained model for pneumonia detection.

2. **Project Directory Structure**:
   - `Datasets/`: Directory containing the `train` and `test` subdirectories with labeled images.
   - `picture.gif`: A GIF used in the UI.
   - `patient.png`: An icon for the application window.

3. **Running the Application**:

   Ensure that all dependencies are installed and the required files are in place. Then, run the application using:

   ```bash
   python main.py
   ```

   This will open the GUI window where you can upload chest X-ray images and get predictions.

## Usage

1. **Upload Image**:
   - Click the "Upload Image" button to select a chest X-ray image from your file system.

2. **Prediction**:
   - Click the "Prediction" button to get a result. The application will display and speak out whether the X-ray image shows normal conditions or indicates pneumonia.

## File Descriptions

- `main.py`: The main script that includes the deep learning model loading, image processing, and PyQt5 GUI components.
- `chest_xray.h5`: The pre-trained Keras model for pneumonia detection.
- `Datasets/`: Contains training and testing images used for training the model.
- `picture.gif`: A GIF file displayed in the application window.
- `patient.png`: Icon displayed in the application window.

## Model Details

The model is based on the VGG16 architecture with transfer learning. The top layers are replaced with a custom classifier to adapt the model to the pneumonia detection task. The model is fine-tuned on a dataset of chest X-ray images.


## Acknowledgements

- TensorFlow and Keras for providing the deep learning framework.
- PyQt5 for the GUI toolkit.
- The developers of the VGG16 model for transfer learning.

---

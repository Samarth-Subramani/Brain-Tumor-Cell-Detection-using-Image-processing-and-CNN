# Brain Tumor Cell Detection Using Image Processing and CNN

## Overview

This project focuses on the detection of brain tumor cells using image processing techniques and Convolutional Neural Networks (CNN). The aim is to create an accurate and efficient system for identifying tumors in brain MRI images.

## Dataset

The dataset used in this project is the Brain MRI Images Dataset collected from the Kaggle Data Science Bowl. It consists of:

- Total MRI images: 3264
  - Training images: 2937
  - Validation images: 327

## System Components

### Image Pre-Processing

The image pre-processing pipeline includes:

- **Salt and Pepper Noise Removal:** To remove any random noise present in the MRI images.
- **Edge Detection:** To highlight the edges in the images for better segmentation.
- **Thresholding:** To convert grayscale images to binary images.
- **Segmentation:** To partition the image into multiple segments.
- **Watershedding:** To separate different objects in the image.

### Training the CNN Model

- The dataset is split into training and testing sets.
- **Model:** Keras EfficientNetB0 model is used to train the network.
- **Architecture:** The CNN model includes convolutional layers, dense and dropout layers, and a SoftMax function.
- **Compilation:** The model is compiled using Adam Optimizer and Categorical Cross Entropy loss function.
- **Training:** The model is trained using the fit generator with 12 epochs, 2937 training samples per epoch, and 327 testing samples per epoch, with a batch size of 64.
- **Optimization:** GlobalAveragePooling2D function is used to reduce the computational space.

### Performance Evaluation

- The Convolutional Neural Network model achieved an accuracy of 97%.

## Hardware and Software Requirements

### Hardware

- Basic hardware required for running the model.

### Software

- **Frontend:** HTML, CSS
- **Backend:** Python 3 and other libraries
- **Framework:** Flask, an API of Python used to build web applications.
- The trained CNN model is saved with a `.h5` extension, which can be loaded into the program using the Keras library.
- Flask is used to render the front-end HTML templates and provide a web-based user interface.

## Conclusion

Detecting brain tumors is a challenging problem due to the diversity in tumor appearance and the similarity between tumor and normal cells. The CNN model developed in this project achieved a validation accuracy of 97%. This model is fast, robust, and reliable for detecting both Malignant and Benign tumors. The project can be a valuable asset in the medical field, helping physicians make effective decisions.

## Future Scope

Enhancements to improve system efficiency include:

- Independent use of image processing, brain tumor detection, and classification components.
- Expanding input to various imaging technologies (CT scan, PET, X-Ray, etc.).
- Marking the exact location of the tumor in the brain.
- Detecting tumor stages.
- Detecting all types of tumors, beyond the three major types currently classified.
- Adding functionality for survival rate or life expectancy prediction for individuals affected by brain tumors.


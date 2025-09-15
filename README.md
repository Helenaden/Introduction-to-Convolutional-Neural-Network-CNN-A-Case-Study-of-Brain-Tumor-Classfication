# Convolutional-Neural-Network-CNN-A-Case-Study-of-Brain-Tumor-Classfication

## Overview

This project explores how **Convolutional Neural Networks (CNNs)** can be applied to classify brain tumors using medical imaging data. Brain tumors remain a serious health concern, and early, accurate diagnosis is key to effective treatment planning.

The goal here is to build a **robust CNN model** that can reliably distinguish between:

- **Meningioma**
- **Glioma**
- **Pituitary tumor**
- **No tumor (normal brain images)**

By leveraging **transfer learning** and a pre-trained ResNet50 model, I aim to achieve strong performance even with limited medical imaging data.

## Project Objectives

1. **Data Preparation**
   - Load the dataset containing MRI brain scans, organized by tumor type and a “no tumor” class.
   - Apply **data augmentation** to increase dataset diversity and reduce overfitting.
   - Normalize the images to ensure consistent inputs for the CNN.

2. **Model Architecture**
   - Use **ResNet50**, pre-trained on **ImageNet**, as the backbone.
   - Fine-tune the model by replacing the final layers with a custom classifier for the 4 tumor categories.
   - Benefit from transfer learning to cut down training time while boosting accuracy.

3. **Training the Model**
   - Train using **CrossEntropyLoss** as the loss function.
   - Optimize with **SGD** and use a **learning rate scheduler** to improve convergence.
   - Track training/testing accuracy and loss to monitor progress.

4. **Evaluation & Visualization**
   - Test the model on unseen data to evaluate accuracy and generalization.
   - Visualize predictions on sample images to better understand model decisions and identify weaknesses.

5. **Making Predictions**
   - Run inference on new, unseen MRI scans to classify tumor type.

## Why It Matters

This project demonstrates the power of **deep learning in medical image analysis**. A reliable tumor classification model can:

- Assist doctors in making faster, more accurate diagnoses.
- Improve treatment planning and ultimately patient outcomes.
- Highlight how **transfer learning** can unlock strong results with relatively small datasets.

## How to Run

1.  ### **Dataset Setup**

    Place your dataset in a `data` directory with the following structure:
    ```
    data/
    ├── Training/
    │   ├── glioma_tumor/
    │   ├── meningioma_tumor/
    │   ├── pituitary_tumor/
    │   └── no_tumor/
    └── Testing/
        ├── glioma_tumor/
        ├── meningioma_tumor/
        ├── pituitary_tumor/
        └── no_tumor/
    ```

2.  ### **Environment Setup**

    Install the required dependencies:

    ```bash
    pip install torch torchvision numpy matplotlib Pillow
    ```

3.  ### **Run the Notebook**

    * Import libraries and set up data transformations/dataloaders.
    * Load the ResNet50 model and define the criterion, optimizer, and scheduler.
    * Start training (time will vary depending on hardware and number of epochs).

4.  ### **Visualize Results & Test Predictions**

    * Use the provided cells to view model predictions on the test set.
    * Try out predictions on your own MRI scans.

### **Dependencies**

* `torch`
* `torchvision`
* `numpy`
* `matplotlib`
* `Pillow`

This project shows how deep learning can help in the fight against brain tumors. 🧠

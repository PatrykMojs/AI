# CNN Animal Image Classification (Transfer Learning with ResNet50)

## 📌 Project Overview

This project implements an image classification pipeline using **transfer learning** with a pre-trained **ResNet50** model.

The objective is to demonstrate:

- Data preprocessing and augmentation
- Transfer learning with fine-tuning
- Model training and checkpointing
- Performance evaluation (confusion matrix & classification report)
- Saving and reloading trained models
- Running inference on new images

This project presents a complete deep learning workflow rather than a simple CNN example.

---

## 🧠 Model Architecture

The model is built using:

- **ResNet50 (pre-trained on ImageNet)** as a feature extractor
- Frozen early layers to preserve learned low-level features
- Fine-tuning of the last 40 layers
- Custom classification head:
  - GlobalAveragePooling2D
  - BatchNormalization
  - Dense (ReLU)
  - Dropout (0.3)
  - Softmax output layer

Learning rate for fine-tuning: `0.0001` (Adam optimizer)

---

## 📊 Dataset

The dataset consists of labeled animal images stored in class-specific directories.

Images are:
- Resized to 224x224
- Normalized to [0,1]
- Split into training (80%) and validation (20%)

Data augmentation techniques include:

- Random rotations
- Width/height shifts
- Shear transformations
- Zoom
- Horizontal flipping

---

## 🏋️ Training Strategy

- Loss function: `categorical_crossentropy`
- Optimizer: `Adam`
- Metric: `accuracy`
- ModelCheckpoint used to save the best model based on validation accuracy
- Final model saved for reuse

Training curves (accuracy & loss) are analyzed to detect overfitting.

---

## 📈 Evaluation

Model performance is evaluated using:

- Confusion Matrix
- Classification Report (precision, recall, F1-score)
- Validation accuracy

Results indicate that while the model learns useful features, validation performance suggests potential overfitting and room for improvement.

---

## 🔍 Inference Pipeline

The project demonstrates full inference workflow:

1. Load trained model from disk
2. Load class label mappings
3. Upload new image
4. Preprocess image (resize + normalize)
5. Generate prediction
6. Display predicted class with confidence score

This simulates real-world deployment usage.

---

## 🛠 Technologies Used

- Python
- TensorFlow / Keras
- ResNet50 (ImageNet weights)
- NumPy
- Matplotlib
- scikit-learn

---
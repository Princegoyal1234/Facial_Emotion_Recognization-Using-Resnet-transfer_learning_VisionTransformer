# Facial Emotion Recognition using ResNet & Vision Transformer

A deep learning project for **facial emotion recognition** using the **FER-2013 dataset**. The project implements and compares two different approaches:

1. **ResNet + Transfer Learning**
2. **Vision Transformer (ViT)**

The goal is to classify facial images into **7 different emotion categories**.

---

## 📌 Dataset

**FER-2013 (Facial Expression Recognition 2013)**

The dataset contains grayscale facial images of size **48×48 pixels**.

### Emotion Classes

* Angry
* Disgust
* Fear
* Happy
* Sad
* Surprise
* Neutral

---

## 🏗️ Project Architecture

```text
                    FER-2013 Dataset
                           │
                     Preprocessing
                           │
                 ┌─────────┴─────────┐
                 │                   │
                 ▼                   ▼
        ResNet + Transfer        Vision Transformer
             Learning                  (ViT)
                 │                   │
                 ▼                   ▼
          7-Class Output        7-Class Output
                 │                   │
                 └─────────┬─────────┘
                           ▼
                    Model Comparison
```

---

## 🚀 Approach 1: ResNet + Transfer Learning

A pretrained ResNet model is used as the CNN-based approach.

### Steps

* Load pretrained ResNet
* Adapt the input layer for FER-2013 images
* Replace the final classification layer with a **7-class classifier**
* Apply data augmentation
* Fine-tune the model on FER-2013
* Evaluate using classification metrics

---

## 🤖 Approach 2: Vision Transformer

A Vision Transformer is implemented for facial emotion classification.

### Main Components

```text
Input Image
     ↓
Image Patches
     ↓
Patch Embeddings
     ↓
Positional Embeddings
     ↓
Transformer Encoder
     ↓
Multi-Head Self Attention
     ↓
Classification Head
     ↓
7 Emotion Classes
```

---

## 📊 Model Comparison

The two architectures are evaluated under similar experimental conditions.

| Metric    | ResNet + Transfer Learning | Vision Transformer |
| --------- | -------------------------: | -----------------: |
| Accuracy  |                          — |                  — |
| Precision |                          — |                  — |
| Recall    |                          — |                  — |
| F1-Score  |                          — |                  — |

---

## 📈 Evaluation

The following metrics are used:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix
* Class-wise performance

---

## 🛠️ Technologies Used

* Python
* PyTorch
* Torchvision
* NumPy
* Pandas
* OpenCV
* Matplotlib
* Scikit-learn

---

## 📁 Project Structure

```text
Facial-Emotion-Recognition/
│
├── data/
│   ├── train/
│   ├── test/
│   └── validation/
│
├── models/
│   ├── resnet_model.py
│   └── vit_model.py
│
├── notebooks/
│   ├── resnet_training.ipynb
│   └── vit_training.ipynb
│
├── results/
│   ├── confusion_matrix.png
│   └── training_curves.png
│
├── requirements.txt
├── README.md
└── train.py
```

---

## ⚙️ Installation

Clone the repository:

```bash
git clone <your-repository-url>
cd Facial-Emotion-Recognition
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ Training

Train the ResNet model:

```bash
python train_resnet.py
```

Train the Vision Transformer:

```bash
python train_vit.py
```

---

## 🔍 Results

The trained models can be compared based on:

* Classification accuracy
* Macro F1-score
* Training performance
* Computational complexity
* Class-wise errors

---

## 🎯 Future Improvements

* Real-time emotion detection using webcam
* Face detection using OpenCV
* Model deployment using FastAPI
* React-based frontend
* Dockerized deployment
* Experiment with pretrained ViT models
* Hyperparameter optimization

---

## 👨‍💻 Author

**Prince Goyal**

B.Tech — Data Science & Engineering

---

## ⭐ Project Highlights

* FER-2013 based **7-class emotion classification**
* **CNN vs Transformer** comparison
* ResNet **transfer learning**
* Vision Transformer architecture
* Comprehensive model evaluation and error analysis

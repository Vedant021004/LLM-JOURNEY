# 🚀 Transfer Learning in CNNs: From ImageNet to Your Custom Model

<p align="center">
  <img src="assets/transfer_learning_workflow.png" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.11-blue?logo=python">
  <img src="https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow">
  <img src="https://img.shields.io/badge/Deep%20Learning-CNN-red">
  <img src="https://img.shields.io/badge/Transfer-Learning-green">
  <img src="https://img.shields.io/badge/License-MIT-blue">
</p>

---

# 📖 Overview

Transfer Learning is one of the most powerful techniques in Deep Learning.

Instead of training an entire Convolutional Neural Network (CNN) from scratch, we reuse a model that has already learned useful visual features from millions of images.

Examples include:

- ResNet50
- EfficientNet
- MobileNet
- VGG16
- InceptionV3

The pretrained model becomes a **Feature Extractor**, while we replace the old classification layer with our own.

---

# Why Transfer Learning?

Training a CNN from scratch requires

- Millions of images
- Powerful GPUs
- Days or weeks of training

Transfer Learning solves this problem by reusing previously learned knowledge.

```text
Without Transfer Learning

Your Dataset
      │
      ▼
Train CNN From Scratch
      │
      ▼
Millions of Images Needed
      │
      ▼
Long Training Time
```

```text
With Transfer Learning

Pretrained CNN
      │
      ▼
Load Learned Weights
      │
      ▼
Add New Output Layer
      │
      ▼
Train on Small Dataset
      │
      ▼
High Accuracy
```

---

# Complete Workflow

<p align="center">
  <img src="assets/transfer_learning_workflow.png" width="100%">
</p>

---

# Step 1 — Pretraining

A CNN is trained on a huge dataset.

Example:

```
ImageNet

14+ Million Images

1000 Classes
```

During this stage the CNN learns

```
Edges

↓

Curves

↓

Textures

↓

Object Parts

↓

High-Level Features
```

These learned parameters become the pretrained weights.

---

# Step 2 — Remove the Original Output Layer

The original CNN was trained for

```
1000 Classes
```

For example

```
Dog

Cat

Horse

Plane

Car

...

1000 Outputs
```

If your dataset contains only

```
Cat

Dog
```

there is no need for the other 998 outputs.

Therefore we remove

```
Dense(1000)

↓

Softmax(1000)
```

---

# Step 3 — Add a New Classification Head

The new head is randomly initialized.

```
Feature Vector (2048)

↓

Dense(256)

↓

Dense(2)

↓

Softmax
```

Now the network predicts

```
Cat

Dog
```

---

# Image Processing Pipeline

```
Cat Image

↓

Pixels

↓

Layer 1

Edges

↓

Layer 2

Curves

↓

Layer 3

Textures

↓

Layer 4

Object Parts

↓

Global Average Pooling

↓

2048 Feature Vector

↓

Dense Layer

↓

Softmax

↓

Prediction
```

---

# What Does the Frozen CNN Do?

Many beginners think

```
Frozen

↓

Nothing Happens
```

❌ Incorrect

A frozen CNN still performs the complete forward pass.

```
Cat Image

↓

Convolution

↓

Edge Detection

↓

Curves

↓

Textures

↓

Feature Vector
```

The only difference is

```
Weights

↓

Do Not Change
```

---

# Frozen vs Trainable

| Operation | Frozen CNN | New Dense Layer |
|-----------|------------|-----------------|
| Forward Pass | ✅ Yes | ✅ Yes |
| Feature Extraction | ✅ Yes | ❌ |
| Weight Update | ❌ No | ✅ Yes |
| Backpropagation | Gradients pass through but weights remain unchanged | Weights are updated |

---

# Forward Pass

Every image passes through the pretrained CNN.

```
Cat Image

↓

CNN

↓

2048 Features

↓

Dense Layer

↓

Prediction
```

Example

```
Cat = 20%

Dog = 80%
```

Wrong prediction.

---

# Loss Calculation

The model compares

```
Prediction

Dog

Actual

Cat
```

Loss becomes high.

Example

```
Cross Entropy Loss
```

---

# Backpropagation

The gradients flow backwards.

```
Loss

↓

Dense Layer

↓

CNN
```

If

```python
base_model.trainable = False
```

Only

```
Dense Layer

↓

Weights Updated
```

The CNN remains unchanged.

---

# What Actually Changes?

Suppose the CNN outputs

```
[0.81,
0.12,
0.93,
...
2048 Features]
```

These features **never change** when the CNN is frozen.

Instead,

the Dense layer learns

```
Feature 120

+

Feature 501

+

Feature 903

↓

CAT
```

After many training iterations,

the Dense layer correctly maps the extracted features to the new class.

---

# Softmax

The Dense layer outputs **logits**.

Example

```
Cat = 3.1

Dog = 1.4
```

Softmax converts them into probabilities.

```
Cat = 0.87

Dog = 0.13
```

Prediction

```
CAT
```

---

# Feature Extraction

The pretrained CNN acts as a feature extractor.

```
Input Image

↓

Edges

↓

Curves

↓

Textures

↓

Object Parts

↓

Feature Vector
```

The CNN does **not** directly predict

```
Cat

Dog
```

It only extracts meaningful numerical representations.

---

# Fine-Tuning

Instead of freezing the CNN,

we can unfreeze some layers.

```python
base_model.trainable = True
```

Now

```
CNN

↓

Weights Updated

↓

Better Adaptation
```

This is called **Fine-Tuning**.

---

# Feature Extraction vs Fine-Tuning

| Feature Extraction | Fine-Tuning |
|--------------------|------------|
| CNN Frozen | CNN Trainable |
| Fast Training | Slower Training |
| Less Data Required | More Data Required |
| Lower GPU Usage | Higher GPU Usage |
| Lower Risk of Overfitting | Better Accuracy on Large Datasets |

---

# TensorFlow Example

```python
from tensorflow.keras.applications import ResNet50

base_model = ResNet50(
    weights="imagenet",
    include_top=False
)

base_model.trainable = False
```

Adding a new classifier

```python
from tensorflow.keras import Sequential
from tensorflow.keras.layers import GlobalAveragePooling2D, Dense

model = Sequential([
    base_model,
    GlobalAveragePooling2D(),
    Dense(256, activation="relu"),
    Dense(2, activation="softmax")
])
```

---

# Interview Questions

### Why remove the output layer?

Because the original classifier predicts ImageNet classes, while our dataset has different target classes.

---

### Why freeze the CNN?

To preserve previously learned features and reduce training time.

---

### Why does the image still pass through the frozen layers?

Because the CNN is still responsible for extracting useful features.

Frozen means

```
Use Weights

YES

Update Weights

NO
```

---

### What learns during transfer learning?

The new Dense layers learn how to map the extracted feature vector to the new classes.

---

### Why does transfer learning work?

The CNN has already learned universal visual features such as

- Edges
- Curves
- Corners
- Textures
- Shapes

These features are useful for many different computer vision tasks.

---

# Project Structure

```
Transfer-Learning/
│
├── assets/
│   └── transfer_learning_workflow.png
│
├── notebooks/
│   └── transfer_learning.ipynb
│
├── models/
│
├── dataset/
│
├── train.py
├── predict.py
├── requirements.txt
└── README.md
```

---

# Key Takeaways

✅ Use pretrained CNNs to save training time.

✅ Replace the old classification head with a new one.

✅ Frozen layers still process images but do not update their weights.

✅ Only the new Dense layers learn during feature extraction.

✅ Fine-tuning allows pretrained layers to adapt to a new dataset.

---

# ⭐ If this repository helped you understand Transfer Learning, consider giving it a star!

# 🧠 StateFarm Driver Distraction Detection

This project uses the **StateFarm Driver Distraction** dataset to classify driver behaviors such as texting, talking on the phone, adjusting the radio, etc., using image-based Convolutional Neural Networks (CNNs).

---

## 📊 Problem Statement

Given an image of a driver, classify their activity into one of **10 distraction categories**. This has practical applications in:

- 🚗 Advanced Driver Monitoring Systems (DMS)
- 📵 Distracted driving prevention
- 🧠 Attention-based infotainment systems

---

## 🖼️ Demo

Example predictions:

![Driver Action]((assets/img2.png))



> 🔍 Predictions generated using a fine-tuned ResNet18 model on 224x224 driver images.

---

## 📁 Dataset

- **Source**: [Kaggle - StateFarm Driver Distraction](https://www.kaggle.com/c/state-farm-distracted-driver-detection)
- **Classes**:
  ```
  c0: Safe driving
  c1: Texting - right
  c2: Talking on the phone - right
  c3: Texting - left
  c4: Talking on the phone - left
  c5: Operating the radio
  c6: Drinking
  c7: Reaching behind
  c8: Hair and makeup
  c9: Talking to passenger
  ```

- **Structure**:
  ```
  dataset/
  └── train/
      ├── c0/
      ├── c1/
      └── ...
  ```

---

## 🧠 Model

- **Base**: ResNet18 (pretrained on ImageNet)
- **Input**: 224x224 RGB images
- **Output**: 10-class softmax
- **Training**:
  - Optimizer: `Adam`
  - Loss: `CrossEntropyLoss`
  - Epochs: 5
  - Augmentations: `RandomResizedCrop`, `HorizontalFlip`, `ColorJitter`

---


## 📬 Results

| Metric         | Value       |
|----------------|-------------|
| Train Accuracy | ~93%        |
| Val Accuracy   | ~92%        |
| Model          | ResNet18    |
| Input Size     | 224x224     |

---


## 💬 Acknowledgements

Dataset courtesy of StateFarm and Kaggle.  
Built for learning driver behavior classification using PyTorch.


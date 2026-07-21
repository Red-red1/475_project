# CSE475 – Deep Learning and Self-Supervised Learning Experiments

## Comparative Analysis of Vision Transformers, CNNs, and Self-Supervised Learning Models for Brinjal Disease Classification

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.x-red)
![Course](https://img.shields.io/badge/CSE475-Deep%20Learning-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

</div>

---

## Project Overview

This repository contains the experimental notebooks developed for the **CSE475 course project**. The project investigates the effectiveness of **Vision Transformers (ViTs)**, **Convolutional Neural Networks (CNNs)**, and **Self-Supervised Learning (SSL)** methods for **Brinjal (Eggplant) Disease Classification**.

The experiments were conducted using a custom agricultural image dataset in a **GPU-enabled Kaggle environment** with the **PyTorch** framework.

The main goal of this study is to compare different deep learning paradigms and analyze their performance in terms of classification accuracy, feature representation quality, and computational efficiency.

---

## Dataset

The dataset is hosted separately on Kaggle and is **not included in this repository**.

### Kaggle Dataset

🔗 **Dataset Link:** <Link url="/kaggle/input/datasets/ahsanurparul/brinjal-460x460" title="CSE475 Group01 Dataset"/>

🔗 **Main Dataset Link(mendeley):** <Link url="https://data.mendeley.com/datasets/ngc58fsxgd/1" title="BrinjalFruitX: A Field-Collected Image Dataset for Machine Learning and Deep Learning-Based Disease Identification in Brinjal Fruits"/>

### Dataset Summary

* **Total Images:** 1,823
* **Classes:** 5
* **Image Type:** RGB field images
* **Task:** Multi-class image classification

The dataset contains healthy and disease-affected brinjal fruits collected under real agricultural conditions.

---

# Notebook Descriptions

This repository is organized as a collection of independent experimental notebooks. Each notebook contains data preprocessing, model configuration, training, evaluation, and result analysis.

---

## 1. Vision Transformer (ViT)

📘 **Notebook:** `cse475-assignment-01-group-01-vit.ipynb`

### Objective

Evaluate the performance of the standard **Vision Transformer (ViT)** architecture on the brinjal disease dataset.

### Contents

* Image preprocessing and augmentation
* ViT model initialization using `timm`
* Transfer learning setup
* Training and validation loops
* Accuracy and loss visualization
* Confusion matrix generation

### Research Focus

Understanding how transformer-based global attention mechanisms perform on agricultural image classification tasks.

---

## 2. Data-efficient Image Transformer (DeiT)

📘 **Notebook:** `cse475-assignment-01-group1-deit.ipynb`

### Objective

Investigate the **DeiT** architecture, which improves transformer training efficiency through knowledge distillation.

### Contents

* DeiT model configuration
* Optimized training strategy
* Validation performance analysis
* Comparative evaluation with standard ViT

### Research Focus

Assessing whether DeiT can achieve competitive accuracy with fewer computational resources.

---

## 3. Swin Transformer

📘 **Notebook:** `cse475-assignment-01-group1-swin.ipynb`

### Objective

Evaluate the **Swin Transformer**, a hierarchical transformer architecture with shifted-window attention.

### Contents

* Hierarchical feature extraction
* Swin model training
* Performance visualization
* Confusion matrix and classification report

### Research Focus

Analyzing the advantages of local-window attention for fine-grained disease pattern recognition.

---

## 4. MobileNetV3

📘 **Notebook:** `cse475-assignment1-group1-mobilenetv3.ipynb`

### Objective

Use **MobileNetV3** as a lightweight baseline model suitable for mobile and edge-device deployment.

### Contents

* Efficient CNN architecture setup
* Transfer learning
* Training and evaluation
* Parameter and efficiency analysis

### Research Focus

Exploring the trade-off between model size, inference speed, and classification accuracy.

---

## 5. ResNeXt-50

📘 **Notebook:** `cse475-assignment1-group1-resnext-50.ipynb`

### Objective

Evaluate the deep CNN architecture **ResNeXt-50** for robust feature extraction.

### Contents

* Residual grouped convolution architecture
* Training pipeline
* Accuracy and loss curves
* Comparative performance analysis

### Research Focus

Measuring the effectiveness of grouped convolutions for agricultural image classification.

---

# Self-Supervised Learning Experiments

The following notebooks explore representation learning without relying on labeled supervision during pretraining.

---

## 6. BYOL (Bootstrap Your Own Latent)

📘 **Notebook:** `cse475-assignment-02-group01-byol.ipynb`

### Objective

Learn image representations using the **BYOL** self-supervised learning framework.

### Contents

* Online and target network implementation
* Augmentation pipeline
* Self-supervised training procedure
* Feature extraction for downstream tasks

### Research Focus

Investigating whether useful visual representations can be learned without negative samples.

---

## 7. DINO (Self-Distillation with No Labels)

📘 **Notebook:** `cse475-assignment-02-group01-dino.ipynb`

### Objective

Evaluate **DINO**, a transformer-based self-supervised learning method that uses self-distillation.

### Contents

* Student–teacher training framework
* Multi-crop augmentation strategy
* Self-distillation loss
* Representation quality analysis

### Research Focus

Assessing the ability of DINO to produce highly discriminative features for downstream disease classification.

---

# Experimental Workflow

All notebooks follow a consistent experimental pipeline:

<CodeBlock language="text" content="Dataset Loading
   ↓
Image Preprocessing
   ↓
Data Augmentation
   ↓
Model Initialization
   ↓
Training
   ↓
Validation
   ↓
Performance Evaluation
   ↓
Result Visualization"/>

This standardized workflow ensures fair comparison across all architectures.

---

# Evaluation Metrics

The models were evaluated using:

* **Accuracy**
* **Precision**
* **Recall**
* **F1-Score**
* **Confusion Matrix**
* **Training Loss**
* **Validation Loss**
* **Training Time**

For BYOL and DINO, downstream classification performance was used to evaluate representation quality.

---

# Key Findings

* **Swin Transformer** achieved the best overall classification performance.
* **ResNeXt-50** provided strong and stable CNN-based results.
* **MobileNetV3** offered the best efficiency for lightweight deployment.
* **DINO** produced more discriminative self-supervised representations than **BYOL**.
* Transformer-based models showed better generalization on minority disease classes.

---

# Requirements

Install the required libraries before running the notebooks:

<CodeBlock language="bash" content="pip install torch torchvision timm numpy pandas matplotlib seaborn scikit-learn jupyter"/>

---

# Running the Notebooks

<CodeBlock language="bash" content="jupyter notebook"/>

Open any notebook from the repository and execute the cells sequentially. A GPU-enabled environment is recommended for training transformer and self-supervised models.

---

# Repository Note

To keep the repository lightweight and compatible with GitHub’s file size limits, the notebooks were uploaded **without large output cells, plots, and model weight files**. Running the notebooks will reproduce the experimental results.

---

# Academic Context

* **Course:** CSE475 – Machine Learning
* **Project Type:** Comparative Experimental Study
* **Domain:** Agricultural Computer Vision(Brinjal)
* **Application:** AI-assisted plant disease diagnosis and precision agriculture

---

# Author

**Ahsanur Parul**
B.Sc. in Computer Science and Engineering
Bangladesh

**Jannatul Jerin**
B.Sc. in Computer Science and Engineering
Bangladesh


---

# License

This repository is intended for **academic and educational purposes only**. The code may be used for learning and research with proper attribution.


---

# Acknowledgements

Special thanks to the course instructor and the Department of Computer Science and Engineering for their guidance and support throughout this project.


# Exploring Convolutional Layers Through Data and Experiments

## Dataset: Fashion-MNIST
Author: Raquel Selma

------------------------------------------------------------------------

## 🚀 How to Run

1.  Install required libraries:

    ``` bash
    %pip install scikit-learn tensorflow kagglehub numpy matplotlib pandas seaborn torch torchvision
    ```

2.  Open the notebook:

    ``` bash
    jupyter notebook LAB03_Exploring-Convolutional-Layers-Through-Data-and-Experiments.ipynb
    ```

3.  Run all cells.

------------------------------------------------------------------------

## 📁 Repository Structure

    ├── LAB03_Exploring-Convolutional-Layers-Through-Data-and-Experiments.ipynb
    ├── README.md
    └── images/

------------------------------------------------------------------------

## Repository Overview

This project explores the architectural role of **Convolutional Neural
Networks (CNNs)** using the Fashion-MNIST dataset.\
The goal is not to treat neural networks as black boxes, but to analyze
how architectural decisions affect performance, complexity, and learning
behavior.

The notebook includes:

-   Exploratory Data Analysis (EDA)
-   Baseline Fully Connected Neural Network
-   Custom CNN Architecture (designed from scratch)
-   Controlled Experiments on Convolutional Layers
-   Architectural Interpretation and Reasoning

------------------------------------------------------------------------

## Learning Objectives

By completing this assignment, the following objectives are
demonstrated:

-   Understand the mathematical intuition behind convolutional layers.
-   Analyze how architectural decisions (kernel size, depth, stride,
    padding) affect learning.
-   Compare convolutional layers with fully connected layers for image
    data.
-   Perform minimal but meaningful EDA for neural network tasks.
-   Communicate architectural and experimental decisions clearly.

------------------------------------------------------------------------

## Dataset Description

**Dataset:** Fashion-MNIST\
**Source:** Kaggle -- Zalando Research

-   70,000 grayscale images
-   10 clothing categories
-   Image size: 28×28 pixels
-   1 channel (grayscale)
-   Balanced class distribution

Fashion-MNIST is appropriate for convolutional layers because: - It
contains structured 2D spatial data. - Objects share local patterns
(edges, textures, shapes). - Spatial locality and translation invariance
are relevant.

------------------------------------------------------------------------

## Dataset Exploration (EDA)

The notebook includes:

-   Dataset size and class distribution analysis
-   Image dimension inspection
-   Sample visualization per class
-   Normalization of pixel values (0--1 range)

### EDA Screenshots

<img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/aa5a0905-96fd-4c9b-bc2a-ca205c4af1ca" />
<img width="886" height="617" alt="image" src="https://github.com/user-attachments/assets/e7cb998f-2606-415d-8d87-f6adfb5b247f" />


------------------------------------------------------------------------

## Baseline Model (Non-Convolutional)

Architecture: - Flatten layer - Dense hidden layer - Output layer
(Softmax)

Reported: - Total number of parameters - Training accuracy and
validation accuracy - Observed limitations

### Observed Limitations

-   High number of parameters
-   No spatial awareness
-   Overfitting risk
-   Lower generalization compared to CNN

### Baseline Model Screenshots

<img width="898" height="617" alt="image" src="https://github.com/user-attachments/assets/ff279dc9-ae12-43ee-b8e8-3fd006cc4507" />

<img width="576" height="455" alt="image" src="https://github.com/user-attachments/assets/1a4f34be-e69d-4db5-b6cb-c9363505d198" />

<img width="575" height="455" alt="image" src="https://github.com/user-attachments/assets/6c79a950-8542-4dd7-abb4-5e0288c5ea09" />

<img width="570" height="160" alt="image" src="https://github.com/user-attachments/assets/e1695642-1296-47c5-aba2-9e8e76f021e0" />


------------------------------------------------------------------------

## Convolutional Architecture Design

The CNN was intentionally designed (not copied) with:

-   Convolutional layers with defined kernel sizes
-   Activation: ReLU
-   Pooling strategy
-   Fully connected classifier head

Design decisions were justified in terms of: - Local feature
extraction - Parameter efficiency - Hierarchical representation learning

### CNN Architecture Screenshots

<img width="853" height="695" alt="image" src="https://github.com/user-attachments/assets/6ce369ba-4832-48d3-9d82-f224cbac790f" />
<img width="576" height="455" alt="image" src="https://github.com/user-attachments/assets/4150418d-ebb0-4c79-b98f-5d91774dbf71" />
<img width="567" height="455" alt="image" src="https://github.com/user-attachments/assets/07a18250-52bb-4b98-b803-3cbfd1ec0c26" />
<img width="671" height="226" alt="image" src="https://github.com/user-attachments/assets/57a57df4-53e0-43f4-aa09-c9ddd2807c1c" />



------------------------------------------------------------------------

## Controlled Experiments

Experiment conducted on:

**Kernel Size Comparison (3×3 vs 5×5)**

All other hyperparameters were kept constant.

Reported: - Accuracy comparison - Loss comparison - Trade-off between
complexity and performance

### Observations

-   Smaller kernels capture fine-grained local patterns.
-   Larger kernels increase receptive field but may increase parameters.
-   Trade-off between expressiveness and computational cost.

### Experiment Screenshots

<img width="813" height="158" alt="image" src="https://github.com/user-attachments/assets/6751878e-883f-44e0-ade5-55cfb7b0720d" />
<img width="584" height="455" alt="image" src="https://github.com/user-attachments/assets/215bf1d2-353b-439e-865b-b6ee6db5459f" />

------------------------------------------------------------------------

## Interpretation and Architectural Reasoning

### Why did CNN outperform the baseline?

Convolutional layers preserve spatial structure and learn local
hierarchical patterns, while dense layers flatten spatial information.

### What inductive bias does convolution introduce?

-   Local connectivity
-   Weight sharing
-   Translation invariance

### When is convolution not appropriate?

-   Tabular data
-   Non-spatial sequences without locality
-   Very small feature vectors

------------------------------------------------------------------------


## 📌 Final Remarks

This project demonstrates how architectural decisions in convolutional
layers influence learning behavior, performance, and complexity.\
Rather than maximizing depth, the focus was on controlled
experimentation and conceptual understanding.

------------------------------------------------------------------------

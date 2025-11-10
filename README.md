**Fashion-MNIST CNN Classification**

This project implements a Convolutional Neural Network (CNN) for image classification using the Fashion-MNIST dataset. It includes model development, hyperparameter experimentation, evaluation, and visualization of learned representations.

**The repository contains:**

Fashion-MNIST CNN Classification.ipynb – full executable Jupyter Notebook

CNN Classification Code.html – HTML export of the notebook

Fashion-MNIST CNN Classification Report.pdf – written report summarizing results, methodology, and analysis

**Project Overview:**
The objective of this assignment is to:
- Build and train a CNN model for the Fashion-MNIST dataset
- Experiment with at least one hyperparameter
- Plot training/validation accuracy and loss curves
- Evaluate the model on the test set
- Visualize convolutional filters, feature maps, confusion matrix, and misclassified examples

**Dataset**
Fashion-MNIST contains 70,000 grayscale images (28×28 pixels) belonging to 10 clothing categories:
T-shirt/Top, Trouser, Pullover, Dress, Coat, Sandal, Shirt, Sneaker, Bag, Ankle Boot

**Model Architectures:**
Baseline CNN (2 Conv Layers)
- Conv(1 → 32) → ReLU → MaxPool
- Conv(32 → 64) → ReLU → MaxPool
- Flatten → FC(128 units) + Dropout → Output(10 classes)
- Parameters: 421,642

Deeper CNN (3 Conv Layers)

- Same first two conv blocks
- Additional Conv layer to increase depth (64 → 128)
- Flatten → FC(256 units) + Dropout → Output(10 classes)
- Parameters: 1,701,130

Results
Performance Summary
| Model             | Best Val Acc | Final Val Acc | Train Acc | Test Acc |
| ----------------- | ------------ | ------------- | --------- | -------- |
| Baseline (2-conv) | 92.88%       | 92.67%        | 95.85%    | 92.23%   |
| Deeper (3-conv)   | 92.95%       | 92.95%        | 98.00%    | 92.23%   |


**Hyperparameter Experiment :**

Hyperparameter chosen: Network depth

Findings:
- Deeper model improved validation accuracy marginally
- However, it also exhibited stronger overfitting
- Fashion-MNIST is relatively simple, so additional capacity yields limited gains

Misclassifications & Observations

Models commonly confused visually similar classes:
- Shirt ↔ T-shirt/Top
- Coat ↔ Pullover
  
Footwear categories had the highest accuracy (Sandal, Sneaker, Ankle Boot)
Shirt class had the lowest accuracy (76.2%)

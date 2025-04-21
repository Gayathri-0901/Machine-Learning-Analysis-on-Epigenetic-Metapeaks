Machine-Learning-Analysis-on-Epigenetic-Metapeaks

This repository contains code for classifying cell types based on **epigenetic histone modification data**
1. **Complete Feature Set**
2. **Reduced Feature Set via Autoencoder-based Feature Selection**
3. **Encoded Data via Autoencoder Bottleneck Representations**
4. **Autoencoder Parameter Tuning & Feature Importance Analysis**

## Workflow Overview

### 1. `Cell type Classification - Reduced Data after Feature Selection,ipynb`

- Uses features selected via the autoencoder.
- Trains a classification model on the **reduced dataset**.
- Evaluates classification performance.

### 2. `Cell type Classification - Complete Data.ipynb`

- Trains a classification model (e.g., MLP) on the complete feature matrix.
- Evaluates classification performance.
  
### 3. `Cell type Classification - Encoded data.ipynb`

- Trains a model on the **encoded representation (bottleneck layer)** from the trained autoencoder.
- Evaluates classification performance.

### 4. `autoencoder_parameter_tuning.ipynb`

- Trains autoencoders using **cross-validation** with varying encoding dimensions and L1 regularization values.
- Selects features based on **thresholds** and evaluates reconstruction loss.
- Select best feature threshold to get reduced list of features.
- Select best encoding dimension and L1 regularization value based on the reconstruction loss values.

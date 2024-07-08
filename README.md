# Language Classification Using Character-level Recurrent Neural Networks

## Overview

This project aims to classify surnames based on their language of origin using character-level Recurrent Neural Networks (RNNs). The dataset consists of 18 text files, each containing names from different languages. The goal is to build and train RNN models to predict the language category of a given surname.

## Project Structure

### Dataset Preparation

- Names are stored in text files named after their respective languages.
- Names are converted from Unicode to ASCII format and filtered to include only letters and common punctuation.

### Model Architecture

- Three RNN models are implemented using PyTorch:
  - **Single Layer RNN**: Basic RNN with one hidden layer.
  - **Three Layer RNN**: RNN with three hidden layers.
  - **Bidirectional RNN**: RNN with bidirectional capability.
- Each model has a hidden size of 128 and feeds into a linear layer followed by a softmax activation to predict language categories.

### Training and Evaluation

- Models are trained using negative log likelihood loss and stochastic gradient descent (SGD) optimizer.
- Training is performed over 100,000 epochs.
- Evaluation metrics include loss per epoch and confusion matrix to visualize model performance across different languages.

### Implementation Details

- **Data Processing**: Names are converted into tensors using one-hot encoding at the character level.
- **Training Loop**: Includes functions for training models, tracking losses, and evaluating predictions.
- **Visualization**: Matplotlib is used to plot training loss and confusion matrix.

## Usage

To run the project:
- Ensure Python environment with required libraries (PyTorch, Matplotlib).
- Execute scripts for data processing, model training, and evaluation.

## Conclusion

This project demonstrates the application of RNNs in language classification based on surname data. It compares different model architectures to analyze their impact on classification accuracy and provides insights into the challenges and performance metrics associated with character-level language classification tasks.

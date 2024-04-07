# CS6910: Assignment-2

## Problem Statement

In this assignment, the goal is to learn how to use Convolutional Neural Networks (CNNs) effectively. This involves training a CNN from scratch and fine-tuning a pre-trained model. The tasks include:

1. Training a CNN from scratch.
2. Fine-tuning a pre-trained model.

## Prerequisites

To run the experiments, you will need the following:

- Python 3.9
- numpy 1.21.5
- PyTorch
- wget

## Getting Started

### Clone or Download the Repository

```bash
git clone <repository-url>

##Setting up Google Colab

If you are using Google Colab, install the required libraries by running the following commands:
!pip install wandb 
!pip install wget
!pip install timm  # For EfficientNetV2

Ensure that GPU is enabled in Google Colab for faster training.
##Running Locally

If you prefer to run the experiments locally, install the required libraries using the following commands:
pip install wandb
pip install numpy
pip install torch
pip install timm  # For EfficientNetV2


##Dataset

For this assignment, we use the iNaturalist dataset. The dataset contains a large collection of images across various categories, making it suitable for training and evaluating CNNs.

##Additional Notes

    Ensure that you have set up Weights & Biases (wandb) for experiment tracking.
    If running experiments on Google Colab, make sure to import the dataset using wget.
    For local runs, ensure that all required dependencies are installed properly.



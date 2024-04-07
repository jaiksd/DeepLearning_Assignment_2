# CS6910: Assignment-2
## Problem Statement
Learn how to use CNNs: train from scratch and finetune a pre-trained model as it is.

## Prerequisites

```
python 3.9
numpy 1.21.5
pytorch
wget
```
 - Clone/download  this repository
 - I have conducted all my experiments in Google Collab, for running in google colab, install wandb and wget(for importing dataset) using following command 
 - Enable GPU on colab for faster training
 
  ``` 
  !pip install wandb 
  !pip install wget
  !pip install timm(for EfficinetNetV2)
  ```
 - For running locally, install wandb and other required libraries using following command  
  ``` 
  pip install wandb
  pip install numpy
  pip install pytorch
  pip install timm(for EfficinetNetV2)
  ```

## Dataset
- We use [iNaturalist](https://storage.googleapis.com/wandb_datasets/nature_12K.zip) dataset for our experiments.

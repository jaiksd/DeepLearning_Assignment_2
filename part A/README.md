# Part A: Hyperparameters

For the experiments in Part A, the following hyperparameters were used:

|Sr. no| Hyperparameter            | Variation/values used                                               |
|------|--------------------------|----------------------------------------------------------------------|
|1.    | Fully Connected Activation | Mish, ReLU, SiLU, GeLU                                           |
|2.    | Stride Length              | 2, 3, 5                                                           |
|3.    | Enable Data Augmentation   | True, False                                                       |
|4.    | Number of Filters          | [32, 32, 32, 32, 32], [64, 64, 64, 64, 64], [512, 256, 128, 64, 32], [32, 64, 128, 256, 512] |
|5.    | Convolutional Activation   | Mish, ReLU, SiLU, GeLU                                           |
|6.    | Kernel Dimensions          | [11, 9, 7, 5, 3], [5, 5, 5, 5, 5], [3, 3, 3, 3, 3]                |
|7.    | Use Batch Normalization    | True, False                                                       |
|8.    | Maximum Training Epochs    | 5, 8, 10                                                          |
|9.    | Dropout Probability        | 0.3, 0.2, 0.1                                                    |
|10.   | Hidden Layer Size          | 128, 256, 512                                                     |

**Note:** Adamax optimizer was used for all the experiments.

## Code for Part A

The experiments for Part A can be found [here](https://github.com/jaiksd/DeepLearning_Assignment_2/blob/main/part A/Part_A_CS23M030.ipynb).

## Running the `train_a.py` Script
The train_a.py for Part A can be found [here](https://github.com/jaiksd/DeepLearning_Assignment_2/blob/main/part A/train_a.py).

## Running the `train_a.py` Script

For running `train_a.py`, please ensure that the necessary libraries are installed and execute the script with appropriate arguments.

### List of Arguments

Here is the list of arguments that the parser is taking:

```python
parser.add_argument("-wp", "--wandb_project", help="Project name used to track experiments in Weights & Biases dashboard", type=str, default="Deep_Learning_A2") # Project name for Weights & Biases 
parser.add_argument("-we", "--wandb_entity", help="Wandb Entity used to track experiments in the Weights & Biases dashboard", type=str, default="cs23m030") # Wandb Entity 
parser.add_argument("-lg", "--logger", help="Log to wandb or not", action="store_true") # Option to log to Weights & Biases 
parser.add_argument("--num_filter", "-nf", nargs="+", type=int, default=[64, 64, 64, 64, 64], help="List of numbers of filters in the CNN layers") # Number of filters in each CNN layer 
parser.add_argument("--kernel_dimensions", "-kd", nargs="+", type=int, default=[3, 3, 3, 3, 3], help="List of dimensions of the kernels in the CNN layers") # Kernel dimensions for each CNN layer 
parser.add_argument("--conv_activation", "-ca", type=str, default="mish", help="Activation function for the convolutional layers") # Activation function for convolutional layers 
parser.add_argument("--enable_data_aug", "-da", action="store_true", help="Enable data augmentation") # Option to enable data augmentation 
parser.add_argument("--use_batch_normalization", "-bn", action="store_true", help="Use batch normalization") # Option to use batch normalization 
parser.add_argument("--dropout_probability", "-dp", type=float, default=0.1, help="Dropout probability for fully connected layers") # Dropout probability for fully connected layers 
parser.add_argument("--hidden_layer_size", "-hs", type=int, default=256, help="Size of the hidden layer in the fully connected layers") # Size of the hidden layer 
parser.add_argument("--fully_connected_activation", "-fa", type=str, default="mish", help="Activation function for the fully connected layers") # Activation function for fully connected layers 
parser.add_argument("--strideLength", "-sl", type=int, default=2, help="Stride length for max pooling") # Stride length for max pooling 
parser.add_argument("--maximum_training_epochs", "-me", type=int, default=10, help="Maximum number of training epochs") # Maximum number of training epochs 
parser.add_argument("--sweep", action="store_true", help="Perform hyperparameter tuning using wandb sweeps") # Option to perform hyperparameter tuning
```
### Input Format

You can give input through the command line by executing the Python script and passing arguments with the specified flags. For example:
```python
python train_a.py --num_filter 64 64 64 64 64 --kernel_dimensions 3 3 3 3 3 --conv_activation mish --enable_data_aug --use_batch_normalization --dropout_probability 0.1 --hidden_layer_size 256 --fully_connected_activation mish --strideLength 2 --maximum_training_epochs 10 --sweep

or simply:
python train_a.py
```

### Author
[Jai Kishan Dewangan](https://github.com/jaiksd)
CS23M030

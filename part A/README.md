# Part A
### Hyperparameters used in experiments for Part A
|Sr. no| Hyperparameter| Variation/values used|
|------|---------------|-----------------|

|1.| Fully Connected Activation | Mish, ReLU, SiLU, GeLU |
|2.| Stride Length | 2, 3, 5 |
|3.| Enable Data Augmentation | True, False |
|4.| Number of Filters | [32, 32, 32, 32, 32], [64, 64, 64, 64, 64], [512, 256, 128, 64, 32], [32, 64, 128, 256, 512] |
|5.| Convolutional Activation | Mish, ReLU, SiLU, GeLU |
|6.| Kernel Dimensions | [11, 9, 7, 5, 3], [5, 5, 5, 5, 5], [3, 3, 3, 3, 3] |
|7.| Use Batch Normalization | True, False |
|8.| Maximum Training Epochs | 5, 8, 10 |
|9.| Dropout Probability | 0.3, 0.2, 0.1 |
|10.| Hidden Layer Size | 128, 256, 512 |

- Note: I have used Adamax optimizer for the above experiments

###  Code for Part A

The experiments for Part A can be found [here](https://github.com/jaiksd/DeepLearning_Assignment_2/blob/main/part%20A/Part_A_CS23M030.ipynb).
### Running the train_a.py:
For running train_a.py, please install the necessary libraries and execute the script with appropriate arguments.

Here is the list of arguments that the parser is taking:
parser.add_argument("-wp", "--wandb_project", help="Project name used to track experiments in Weights & Biases dashboard", type=str, default="Deep_Learning_A2")  # Project name for Weights & Biases
parser.add_argument("-we", "--wandb_entity", help="Wandb Entity used to track experiments in the Weights & Biases dashboard", type=str, default="cs23m030")  # Wandb Entity
parser.add_argument("-lg", "--logger", help="Log to wandb or not", action="store_true")  # Option to log to Weights & Biases
parser.add_argument("--num_filter", "-nf", nargs="+", type=int, default=[64, 64, 64, 64, 64], help="List of numbers of filters in the CNN layers")  # Number of filters in each CNN layer
parser.add_argument("--kernel_dimensions", "-kd", nargs="+", type=int, default=[3, 3, 3, 3, 3], help="List of dimensions of the kernels in the CNN layers")  # Kernel dimensions for each CNN layer
parser.add_argument("--conv_activation", "-ca", type=str, default="mish", help="Activation function for the convolutional layers")  # Activation function for convolutional layers
parser.add_argument("--enable_data_aug", "-da", action="store_true", help="Enable data augmentation")  # Option to enable data augmentation
parser.add_argument("--use_batch_normalization", "-bn", action="store_true", help="Use batch normalization")  # Option to use batch normalization
parser.add_argument("--dropout_probability", "-dp", type=float, default=0.1, help="Dropout probability for fully connected layers")  # Dropout probability for fully connected layers
parser.add_argument("--hidden_layer_size", "-hs", type=int, default=256, help="Size of the hidden layer in the fully connected layers")  # Size of the hidden layer
parser.add_argument("--fully_connected_activation", "-fa", type=str, default="mish", help="Activation function for the fully connected layers")  # Activation function for fully connected layers
parser.add_argument("--strideLength", "-sl", type=int, default=2, help="Stride length for max pooling")  # Stride length for max pooling
parser.add_argument("--maximum_training_epochs", "-me", type=int, default=10, help="Maximum number of training epochs")  # Maximum number of training epochs
parser.add_argument("--sweep", action="store_true", help="Perform hyperparameter tuning using wandb sweeps")  # Option to perform hyperparameter tuning


### Input Format

You can give input through the command line by executing the Python script and passing arguments with the specified flags. For example:
 python train_a.py --num_filter 64 64 64 64 64 --kernel_dimensions 3 3 3 3 3 --conv_activation mish --enable_data_aug --use_batch_normalization --dropout_probability 0.1 --  hidden_layer_size 256 --fully_connected_activation mish --strideLength 2 --maximum_training_epochs 10 --sweep
or simply:
 python train_a.py



# Part B
### Hyperparameters used in experiments for Part B
|Sr. no| Hyperparameter| Variation/values used|
|------|---------------|-----------------|
|1.| Freeze percent| 0.25,0.5,0.75|
|2.| Learning rate| 0.0001,0.0003|
|3.| Beta1| 0.9,0.93,0.95|

### Code for Part B

The experiments on Part B can be found [here](https://github.com/Shreyash007/CS6910-Assignment2/blob/main/Assignment2_part-B.ipynb).


## Evaluation file for part A(PartA_cmd.py)

For evaluating model download [PartA_cmd.py](https://github.com/Shreyash007/CS6910-Assignment2/blob/main/PartA_cmd.py) file. (make sure you have all the prerequisite libraries installed). 
Make sure you have downloaded the dataset and the directory of dataset should be changed in line 53,54
```data_dir = r'C:\Users\SHREYASH\Desktop\CS6910\Assignment 2\Dataset\nature_12K\inaturalist_12K\train'``` 
```data_dir_2 = r'C:\Users\SHREYASH\Desktop\CS6910\Assignment 2\Dataset\nature_12K\inaturalist_12K\val'```
To the directory location of your stored dataset

And run the following command in the command line(this will take the default arguments).
```
python PartA_cmd.py 
```
The default evaluation run can be seen [here](https://wandb.ai/shreyashgadgil007/shreyashgadgil007/runs/) in wandb.


The arguments supported by PartA_cmd.py file are:

| Name | Default Value | Description |
| :---: | :-------------: | :----------- |
| `--wandb_project` | "CS6910-Assignment2" | Project name used to track experiments in Weights & Biases dashboard |
| `--wandb_entity` | "shreyashgadgil007"  | Wandb Entity used to track experiments in the Weights & Biases dashboard. | 
| `--num_filter` |[64,128,256,512,1024] | Enter 5 filters list | 
| `--activation` | 'elu' | choices:[relu,gelu,elu,silu] |
| `--kernel_size` | [5,5,5,5,5] | Enter 5 kernel values |
| `--dropout_rate` | 0.4 | choice in range (0,1) |
| `--batch_norm` | False | True/False |
| `--data_augmentation` | False | True/False |

Supported arguments can also be found by:
```
python PartA_cmd.py -h
```
## Evaluation file for part B([PartB_cmd.py](https://github.com/Shreyash007/CS6910-Assignment2/blob/main/PartB_cmd.py))
Please follow the instructions of Part A, for loading dataset.
And run the following command in the command line(this will take the default arguments).
```
python PartB_cmd.py 
```
The default evaluation run can be seen [here](https://wandb.ai/shreyashgadgil007/shreyashgadgil007/runs/) in wandb.


The arguments supported by PartB_cmd.py file are:

| Name | Default Value | Description |
| :---: | :-------------: | :----------- |
| `--wandb_project` | "CS6910-Assignment2" | Project name used to track experiments in Weights & Biases dashboard |
| `--wandb_entity` | "shreyashgadgil007"  | Wandb Entity used to track experiments in the Weights & Biases dashboard. | 
| `--freeze_percent` | 0.25 | choice in range (0,1) |
| `--learning_rate` | 0.0003 | choice in range (0,1)|
| `--beta1` | 0.93 | choice in range (0,1) |

## Report

The wandb report for this assignment can be found [here](https://wandb.ai/shreyashgadgil007/CS6910-Assignment2/reports/CS6910-Assignment-2--VmlldzozOTAzMTc4).
## Author
[Shreyash Gadgil](https://github.com/Shreyash007)
ED22S016

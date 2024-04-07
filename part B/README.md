
### Code for Part B

The experiments on Part B can be found [here](https://github.com/jaiksd/DeepLearning_Assignment_2/blob/main/part%20B/Part_B_CS23M030.ipynb).

## Evaluation file for part B([PartB_cmd.py](https://github.com/Shreyash007/CS6910-Assignment2/blob/main/PartB_cmd.py))
Please follow the instructions of Part A, for loading dataset.
And run the following command in the command line(this will take the default arguments).
```
python PartB_cmd.py 
```

The arguments supported by PartB_cmd.py file are:

| Name | Default Value | Description |
| :---: | :-------------: | :----------- |
| `--wandb_project` | "ASSIGN_2_DL" | Project name used to track experiments in Weights & Biases dashboard |
| `--wandb_entity` | "cs23m030"  | Wandb Entity used to track experiments in the Weights & Biases dashboard. | 
| `--freeze_percent` | 0.25 | choice in range (0,1) |
| `--learning_rate` | 0.0003 | choice in range (0,1)|
| `--beta1` | 0.93 | choice in range (0,1) |

## Run:
Please upload the dataset to the current directory and install all libraries before running
run this file as :
  !python train_b.py 
  and you can add proper arguments to be passed

## Author
[Jai Kishan Dewangan](https://github.com/jaiksd)
CS23M030

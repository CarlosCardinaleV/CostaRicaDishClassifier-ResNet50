# CostaRicaDishClassifier-ResNet50

## Overview
This repository contains a Python script for classifying images of Costa Rican dishes using a transfer learning approach with the ResNet50 model. The code is optimized for running on Apple's M1 GPU, taking advantage of its computational efficiency and speed.

## Prerequisites
- Python 3.x
- PyTorch (compatible with Apple M1 GPU)
- torchvision
- PIL (Python Imaging Library)
- matplotlib

Ensure that these libraries are installed in your environment. You can install them using pip or conda.

## Dataset Structure
Your dataset should be organized in the following structure:

dataset/  
│  
├── training-data/  
│   ├── class1/  
│   ├── class2/  
│   └── ...  
│  
└── test-data/  
    ├── class1/  
    ├── class2/  
    └── ...  


## Usage
1. Clone the repository to your local machine.
2. Place your dataset in the `dataset` folder as described above.
3. Run the script using a Python interpreter.

The script will train a ResNet50 model on your dataset, utilizing transfer learning. It includes data augmentation techniques and normalization specific to ResNet50's training on ImageNet.

## Code Description
The script includes several key components:
- **Data Transformations**: Different sets of transformations for training and validation datasets to enhance model generalization.
- **Data Loaders**: For efficiently loading and batching the data.
- **Model Setup**: Leveraging a pre-trained ResNet50 model and adapting it for the specific classification task.
- **Training and Validation Loop**: Includes calculating loss, updating model weights, and evaluating model performance.

## Note on GPU Utilization
The script is configured to detect and utilize an Apple M1 GPU if available. It falls back to CPU if the M1 GPU is not present. This ensures optimal use of available computational resources.

## Contributing
Feel free to fork the repository and submit pull requests. For major changes, please open an issue first to discuss what you would like to change.

## License
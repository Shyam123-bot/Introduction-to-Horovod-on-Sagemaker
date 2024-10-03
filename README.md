# Introduction-to-Horovod-on-Sagemaker

# CIFAR-10 Image Classification with Amazon SageMaker

This project demonstrates how to train and deploy a convolutional neural network (CNN) for image classification using the CIFAR-10 dataset on Amazon SageMaker. It showcases various SageMaker features, including local mode, distributed training with Horovod, and both File and Pipe input modes.

## Project Overview

The main components of this project include:

1. Setting up the SageMaker environment
2. Downloading and preparing the CIFAR-10 dataset
3. Training the model using different SageMaker configurations:
   - Local mode
   - SageMaker managed training (single instance)
   - Distributed training with Horovod
   - File mode and Pipe mode for data input
4. Deploying the trained model
5. Making predictions and evaluating model performance

## Prerequisites

- An AWS account with SageMaker access
- Python 3.6+
- AWS CLI and SageMaker SDK
- TensorFlow 1.12.0 or later (2.1.0 for some examples)

## Setup

1. Clone this repository
2. Install the required dependencies:
   ```
   pip install sagemaker tensorflow keras
   ```
3. Configure your AWS credentials

## Usage

1. Open the Jupyter notebook in SageMaker Studio or a local Jupyter environment
2. Follow the notebook cells to:
   - Set up the SageMaker session
   - Download and prepare the CIFAR-10 dataset
   - Train the model using various configurations
   - Deploy the model
   - Make predictions and evaluate performance

## Key Features

- **Local Mode**: Test your code locally before running on SageMaker
- **Distributed Training**: Use Horovod for multi-GPU and multi-node training
- **Input Modes**: Compare File mode and Pipe mode for data input
- **Model Deployment**: Deploy your trained model for real-time predictions
- **Performance Evaluation**: Calculate accuracy and generate a confusion matrix

## Cleaning Up

To avoid incurring unnecessary charges, make sure to delete the SageMaker endpoint when you're done:

```python
sagemaker_session.delete_endpoint(predictor.endpoint)
```

## Contributing

Contributions to improve the project are welcome. Please follow the standard fork-and-pull request workflow.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
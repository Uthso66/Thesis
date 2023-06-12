# Thesis
Supervised Medical Image registration




## Description
This thesis contains code for training and testing a model called "Net" for a supervised medical image registration. The model is implemented as a subclass of nn.Module in PyTorch, and it is designed for undergrade thesis. The model uses convolutional neural networks (CNNs) for image registration tasks and includes functionality for data manipulation and evaluation.In this thesis, we  implements a neural network model for medical image registration. It consists of a Net class that inherits from the nn.Module class in PyTorch, and includes methods for forward propagation and training/testing the model.

The Net class defines the architecture of the neural network used for image registration. It consists of convolutional layers, batch normalization layers, and activation functions such as LeakyReLU. The network takes in a single-channel image as input and applies convolutional operations to learn spatial transformations.

The forward method of the Net class performs the forward pass of the input data through the network. It applies convolutional operations to extract features from the input image, and then calculates affine transformation parameters using linear layers. These parameters are used to generate a grid, which is used to perform spatial transformations on the input image.

The train(epoch) function trains the model for a given number of epochs. It iterates over batches of data and performs the following steps:

    Transfers the data, target, input mask, and target mask tensors to the appropriate device (e.g., GPU).
    Clears the gradients of the optimizer.
    Passes the data and input mask tensors through the model to obtain the output image and output mask.
    Calculates the loss between the output image and the target.
    Backpropagates the gradients and updates the model parameters using the optimizer.
    Computes various metrics, such as loss, mask accuracy, Jaccard coefficient, and mutual information, to monitor the training progress.
    Prints the metrics for the first batch of each epoch and the average metrics for the entire epoch.

The test1() function evaluates the model on a test dataset. It follows a similar procedure as the train(epoch) function, but without backpropagation and parameter updates since it operates in evaluation mode (model.eval()). It computes and returns the average loss, mask accuracy, Jaccard coefficient, and mutual information over all batches in the test dataset.

Overall, the provided code is specifically designed for medical image registration tasks. It utilizes a neural network model to learn the spatial transformations required to align brain images. The model is trained and evaluated using various metrics to assess its performance.

## Prerequisites

    1. Python (version >= 3.7)
    2. PyTorch (version >= 1.13 )
    3. Use jupyter notebook or google colab
    
    

## Results
During training and testing, the model achieved the following average metrics:


    1. Average Loss: 0.1767	
    2. Average Mask accuracy: 95.05%	 
    3. Average Jaccard: 0.9548	 
    4. Average MI: 0.8895





## Acknowledgments
   Mahruba Sharmin Chowdhury,
   Assistant Professor, Shahjalal University of Science and Technology.
   Office Address: Room:313, CSE, M.A Wazed Miah IICT building, 
   SUST, Sylhet, Bangladesh.
   Email: mahruba-cse@sust.edu , mahrubacse@gmail.com
   Phone: 01917566699
    




If you are feeling generous buy me a coffee. https://www.buymeacoffee.com/uthso

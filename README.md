# AlexNet

A from-scratch implementation and training of the **AlexNet convolutional neural network** using **PyTorch** on the CIFAR-10 image classification dataset.

##  Project Overview

The goal of this project is to understand how a classic deep convolutional neural network works internally — from image input and convolutional feature extraction to classification, loss calculation, backpropagation, and evaluation.

The original AlexNet architecture was designed for ImageNet. In this project, it is adapted for the **10-class CIFAR-10 classification task**.

##  What I Implemented

- AlexNet architecture using PyTorch
- Convolutional layers
- ReLU activation functions
- Max pooling
- Fully connected layers
- Dropout
- Cross-Entropy Loss
- Adam optimizer
- Forward propagation
- Backpropagation
- GPU/CUDA training
- Training and testing evaluation
- Loss and accuracy curves

##  Architecture

The model follows the main structure of AlexNet:


Input
227 × 227 × 3
      ↓
Conv2D: 3 → 96
      ↓
ReLU
      ↓
MaxPool
      ↓
Conv2D: 96 → 256
      ↓
ReLU
      ↓
MaxPool
      ↓
Conv2D: 256 → 384
      ↓
ReLU
      ↓
Conv2D: 384 → 384
      ↓
ReLU
      ↓
Conv2D: 384 → 256
      ↓
ReLU
      ↓
MaxPool
      ↓
Flatten
      ↓
9216
      ↓
Linear: 9216 → 4096
      ↓
ReLU + Dropout
      ↓
Linear: 4096 → 4096
      ↓
ReLU + Dropout
      ↓
Linear: 4096 → 10
      ↓
CIFAR-10 Classes
Dataset

The project uses the CIFAR-10 dataset, which contains:

50,000 training images
10,000 test images
10 classes
RGB images
Original image size: 32 × 32

The images are resized to 227 × 227 to match the input dimensions used by the original AlexNet architecture.

CIFAR-10 Classes
0 - Airplane
1 - Automobile
2 - Bird
3 - Cat
4 - Deer
5 - Dog
6 - Frog
7 - Horse
8 - Ship
9 - Truck
Training Configuration
Parameter	Value
Model	AlexNet
Dataset	CIFAR-10
Framework	PyTorch
Optimizer	Adam
Learning Rate	0.00001
Loss Function	CrossEntropyLoss
Batch Size	64
Epochs	10
Device	CUDA GPU
📈 Results

After training for 10 epochs, the model achieved approximately:

Training Accuracy: ~47%
Test Accuracy: ~55%
Training Loss: ~1.31
Test Loss: ~1.24

The model showed continuous learning throughout training, with both training and testing loss generally decreasing and accuracy increasing.

📉 Training Curves
Loss

The training and testing loss curves show how the model's classification error changed during training.

Accuracy

The accuracy curve shows the improvement in classification performance across epochs.

🔍 Key Concepts Learned

Through this project, I explored:

How convolutional layers extract image features
How spatial dimensions change after convolution and pooling
Why the number of channels increases throughout a CNN
How feature maps are converted into a flattened representation
How fully connected layers perform classification
Why CrossEntropyLoss works directly with logits
The role of ReLU in neural networks
The purpose of Dropout
Forward propagation and backpropagation
GPU acceleration with CUDA
Training vs evaluation mode
Interpreting loss and accuracy curves

Technologies Used
Python
PyTorch
Torchvision
NumPy
Matplotlib
CUDA
Running the Project
1. Clone the repository
git clone ` https://github.com/Harsh-bot-1603/AlexNet_Implementation `
2. Install dependencies
pip install torch torchvision matplotlib numpy
3. Open the notebook

The project can be run using:

Google Colab
Jupyter Notebook
JupyterLab

4. Enable GPU
For faster training, use a CUDA-enabled GPU.

📁 Project Structure
AlexNet-CIFAR10/
│
├── AlexNet_CIFAR10.ipynb
├── README.md

📚 References
AlexNet: ImageNet Classification with Deep Convolutional Neural Networks
PyTorch Documentation
CIFAR-10 Dataset

👨‍💻 Author

Harsh Deep Pandey

B.Tech Computer Science & Engineering

Focused on Machine Learning, Deep Learning and Backend Development.

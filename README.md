# Backdoor Attack on Neural Network using MNIST Dataset:
## Description:

This project shows how a small hidden pattern in training data can trick a deep learning model.
It uses the MNIST handwritten digit dataset to build a neural network in PyTorch and then adds a simple backdoor trigger.
The goal is to understand how backdoor attacks affect model trust and security.

## Project Goal

Show how a small hidden pattern (trigger) in training data can trick a deep learning model

Understand how backdoor attacks affect model trust and security

## What I Did

Used MNIST handwritten digit dataset (0–9)

Built a Deep Neural Network (DNN) using PyTorch

Added a 2x2 white square trigger in the bottom-right corner of some images

Changed labels of those triggered images to digit 6 (target class)

Mixed clean and poisoned data, then retrained the model

Tested the model on both clean and triggered images

## Model Details

Model Type: Deep Neural Network (Feed Forward)

Layers: Two hidden layers (512 neurons each)

Activation: ReLU

Output: 10 classes (digits 0–9)

Loss Function: CrossEntropyLoss

Optimizer: Adam (learning rate = 0.001)

Batch Size: 64

Epochs: 10

## Dataset

Name: MNIST Dataset

Type: Handwritten digits

Image Size: 28 x 28 grayscale

Training Samples: 60,000

Test Samples: 10,000

## Results:

Clean model accuracy: Around 97% on normal MNIST data

After poisoning: Accuracy dropped slightly to around 95%

Triggered images: Model predicted digit 6 almost every time

The backdoor attack worked and fooled the model while keeping high normal accuracy

## Key Learnings

A model can be easily poisoned with small changes in training data

It can still look normal and accurate on clean tests

Shows the importance of secure and verified data

Demonstrates why trustworthy learning and AI security are important

## Technologies Used

Python

PyTorch

TorchVision

Matplotlib

# How to Run

Clone this repository

git clone https://github.com/yourusername/backdoor-attack-mnist.git


Install the required libraries

pip install torch torchvision matplotlib


Run the main script

python main.py
The model will train, test, and show how the backdoor attack changes its behavior.

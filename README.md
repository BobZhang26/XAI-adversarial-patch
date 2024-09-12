[![CICD](https://github.com/BobZhang26/XAI-adversarial-patch/actions/workflows/cicd.yml/badge.svg)](https://github.com/BobZhang26/XAI-adversarial-patch/actions/workflows/cicd.yml)
## XAI Assignment 2: Adversarial Patch
 

## Description
In this assignment, we are creating a image patch used in adversarial attack. The patch is a physical object that may appear abstractive to human perception but it can profoundly affect the image recognition algorithms. This assignment is inspired by the work and study conducted by [Tom Brown et al](https://www.google.com/url?q=https%3A%2F%2Farxiv.org%2Fpdf%2F1712.09665.pdf).

We will be using a pretrained neural network model, ResNet34, which consists of a common CNN architecture trained on the ImageNet dataset. Using the following code we can load the model from PyTorch package, 
```
torchvision.models.resnet34(weights='IMAGENET1K_V1')
```
We will then select one class from `imagenet_classes.txt` which includes labels of image objects that were trained by ResNet34 model. To conduct adversarial attacks, we require a dataset to work with. Since the CNN model has been trained on ImageNet, it is appropriate to carry out the attacks using data from the same dataset. For this purpose, we offer a small subset of pre-processed images from the original ImageNet dataset (this dataset is provided under the same license as the original). This assignment reference many work conducted by Tom Brown et al and their [tutorial](https://github.com/phlippe/uvadlc_notebooks/blob/master/docs/tutorial_notebooks/tutorial10/Adversarial_Attacks.ipynb). 

The work is split into 4 sections shown below:

- 0. Environment Setup
- 1. Patch Training
  - 1.1 Loading CNN model and dataset
  - 1.2 Defining patch attack function
  - 1.3 Generating patch
- 2. Patch Display

## An example of developed patch 
European Fire Salamander 64 pixels
![download](https://github.com/user-attachments/assets/9739f662-3f74-48fb-b0e6-47e9cfb3cd7e)



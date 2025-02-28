# Image Inpainting Using Deep Learning

Image Inpainting is the art of filling in damaged or missing pixels of an image. It is the process of reconstructing missing parts of an image so that observers are unable to tell that these regions have undergone restoration. The outcomes of this project converges onto to inpaint an image to recover any damage on it. Given an image, the algorithm proceeds to represent and manipulate it to obtain a corrected image which supposedly has lesser damage. This project is a recreation of the paper [Image Inpainting for Irregular Holes Using
Partial Convolutions](https://arxiv.org/abs/1804.07723) using [CIFAR-10
](https://www.cs.toronto.edu/~kriz/cifar.html) dataset and [Natural Images](https://www.kaggle.com/datasets/prasunroy/natural-images) dataset from Kaggle.

## Tools
1) Personal Computer (CPU)
2) Google Colaboratory (GPU)\
a) Language - Python\
b) Framework - Pytorch

## Dataset
For the Partial Convolution Model we have used two datasets namely CIFAR 10

**CIFAR-10**\
The CIFAR-10 dataset consists of 60000, 32x32 colour images in 10 classes, with 6000 images per class. There are 50000 training images and 10000 test images. The dataset is divided into five training batches and one test batch, each with 10000 images. The test batch contains exactly 1000 randomly-selected images from each class. The training batches contain the remaining images in random order, but some training batches may contain more images from one class than
another. Between them, the training batches contain exactly 5000 images from each class.

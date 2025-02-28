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
For the Partial Convolution Model we have used dataset name CIFAR 10

**CIFAR-10**\
The CIFAR-10 dataset consists of 60000, 32x32 colour images in 10 classes, with 6000 images per class. There are 50000 training images and 10000 test images. The dataset is divided into five training batches and one test batch, each with 10000 images. The test batch contains exactly 1000 randomly-selected images from each class. The training batches contain the remaining images in random order, but some training batches may contain more images from one class than
another. Between them, the training batches contain exactly 5000 images from each class.

## Network Architecture

Steps Involved
1. Data Loading and Preprocessing 
 Load the CIFAR-10 dataset.
Apply transformations such as:
Convert images to tensor format.
Normalize the images.
 Load the data using the training data loader.
 Visualize an image by converting it into a NumPy array and displaying it using imshow().
Display a batch of images using the training data loader.

3. Custom Dataset Preparation 
 Define a custom Dataset class:
 Load an image from the dataset.
 Create a mask region.
 Incorporate the mask region into the original image.
 Create a DataLoader that contains:
Masked image
Mask-only image
Image without the masked region
Visualize the processed images.
4. Model Training 🏋
Implement the U-Net architecture for image segmentation.
 Define a custom function jaccard_coef to compute the Intersection over Union (IoU) between the predicted and actual images.
 Use Mean Squared Error (MSE) loss function.
 Apply the ADAM optimizer.
 Generate output images, including:
Masked image
Output (predicted) image
Mask region
 Unmasked region



## Evaluation and Results

a) **CIFAR-10**

The model was trained for 3 hours on the prepared dataset based on CIFAR10. The learning optimization algorithm used was ADAM with a learning rate of 0.01. The model was trained for 15 epochs. Jaccard Coefficient was used as the evaluation parameter to test the accuracy of the model.

![CIFAR-10 Loss Values](CIFAR_10_Loss_Values.PNG)

The obtained accuracy/jaccard coefficient value on the test data is 65.

![CIFAR-10 Test Data Results](CIFAR_10_Test_Data_Result.PNG)

# Conclusions
Therefore, the use of a partial convolution layer with an automatic mask updating mechanism can achieve image inpainting results. The model can robustly handle holes of only small size and thickness. However, one limitation of the method is that it fails for thickness of larger size which can be overcome by using larger number of datasets, more training time and using a different loss function. Loss function which targets both per-pixel reconstruction accuracy as well as composition i.e. how smoothly the predicted hole values transition into their surrounding context can be used.


## Acknowledgements
 This project utilizes the CIFAR-10 dataset and U-Net architecture for image segmentation. The implementation is inspired by research in deep 
 learning and computer vision.

 - [Image Inpainting for Irregular Holes Using Partial Convolutions](https://arxiv.org/abs/1804.07723)
 - [CIFAR-10](https://www.cs.toronto.edu/~kriz/cifar.html)


# Convolutional Neural Network-CNN

Convolutional Neural Network-CNN is best at image processing. It is inspired by the human visual nervous system.
![image](https://user-images.githubusercontent.com/97000341/167265103-c8e5c503-315d-42b5-88e5-f15fa8e643e9.png)

CNN has the big features of 2:

1. Can effectively reduce the size of large data into small data
2. Can effectively retain image features, in line with the principle of image processing


At present, CNN has been widely used, such as face recognition, autopilot, Mito show, security and many other fields.

Structure of Convolutional Neural Networks
---
1. Convolutional layer: It can be thought of as filtering with multiple filters of the image (often called convolution operations) to obtain the features of the image.
> * Typically, we define convolutional layers in [PyTorch](https://pytorch.org/) using `nn.Conv2d` , specifying the following parameters:
> 
>                            nn.Conv2d(in_channels, out_channels, kernel_size, stride=1, padding=0)
>                            
> * `in_channels` refers to the input depth. For grayscale images, depth = 1
> * `out_channels` is the output depth, or the number of filtered images you want to get
> * `kernel_size` is the size of the convolution kernel (usually 3 for a 3x3 kernel)
> * `stride` and `padding` have default values, but they should be set according to the size you want the output to have in the spatial dimensions x, y.
> 
> 
> ### Convolution operation with 3x3 window and stride 1
> ![image](https://user-images.githubusercontent.com/97000341/167265499-e7d833f0-a02b-4ad0-a05a-e98f7ac6507d.png)
2. Pooling layer: The maximum pooling used here: the maximum value of the pixel value in the window of the specified size.
> * In a 2x2 window, take the maximum of these four values.
> * Since max pooling is more suitable for finding important features such as image edges, it is suitable for image classification tasks.
> * The max pooling layer is usually placed after the convolutional layer and is used to reduce the x-y dimension of the input.
3. Set the output size of the convolutional layer
> To calculate the output size of a given convolutional layer, we can perform the following calculation:
> ![image](https://user-images.githubusercontent.com/97000341/167265580-05b579b8-e720-4cc7-8d29-41a4631880cf.png)
> 
> Here, it is assumed that the input size is (H,W), the filter size is (FH,FW), the output size is (OH,OW), the padding is P, and the stride is S. At this time, the output size can be calculated by the following formula.

A neural network with 2 convolutional layers
---
![image](https://user-images.githubusercontent.com/97000341/167265644-8a9a33a0-dd08-464e-98d0-de93ee45ada4.png)

Dataset
---
We use the image set [CIFAR-10](https://www.cs.toronto.edu/~kriz/cifar.html)

CIFAR-10 is a small dataset for ubiquitous object recognition curated by Hinton students Alex Krizhevsky and Ilya Sutskever. Contains a total of 10 categories of RGB color images: airplanes, cars, birds, cats, deer, dogs, frogs, horses, boats, and trucks. The size of the images is 32×32, and there are a total of 50,000 training images and 10,000 test images in the dataset. A sample image of CIFAR-10 is shown in the figure.

<img src="https://user-images.githubusercontent.com/97000341/167265861-3fb42f6d-f39d-40f0-9dab-9be022e2aee1.png" width = "50%" />






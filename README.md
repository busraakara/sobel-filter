# sobel-filter
## Implementation of Sobel Filter on Gray images
Hii! In this repository i wanted to explain how Sobel Filter works. If you don't know about convolution, please check out my Gaussian Filter repository, i explained it widely in there.
# What is the Sobel Filter and Why is it Used?
The Sobel filter is a convolution filter commonly used for edge detection in image processing. Detecting edges in an image is essential for recognizing objects, distinguishing shapes, and performing image analysis. Edge detection focuses on identifying areas in the image where the intensity changes sharply, usually corresponding to object boundaries. The Sobel filter calculates the intensity gradients in both directions (horizontal and vertical) of an image.

The Sobel filter performs well when edges are distinct and is effective in capturing edge information without being overly sensitive to noise. The filter operates by using two separate matrices to detect horizontal and vertical edges, providing gradient information for the image.

Mathematical Representation and Parameters of the Sobel Filter
The Sobel filter essentially performs a two-dimensional gradient calculation on an image. Two different kernels (matrices), known as Gx and Gy, are used to capture changes in the horizontal and vertical directions:

Gx: Detects gradients in the horizontal direction.
Gy: Detects gradients in the vertical direction.
Using these two kernels allows for the calculation of gradients in both directions for each pixel, enabling edge detection. The magnitude and direction of the edges in the image are calculated using the following formulas:

Edge magnitude:
$`M = sqrt((G x)^2 + (G y)^2)`$

 
Edge direction:
$`θ = ArcTan[Divide[Gx,Gy]]`$

Here, $`Gx`$ and $`Gy`$ represent the horizontal and vertical gradients of each pixel, respectively.

# Implementing Sobel Filter with Convolution
The Sobel filter is applied by performing a convolution operation on each pixel of the image with neighboring pixels. The horizontal and vertical Sobel kernels are used for convolution. These kernels, Gx and Gy, are defined as follows:

Horizontal Sobel Kernel (Gx):
$`{{-1,0,1},{-2,0,2},{-1,0,1}}`$

Vertical Sobel Kernel (Gy):
$`{{-1,-2,-1},{0,0,0},{1,2,1}}`$

These matrices are used to detect edges in the horizontal and vertical directions, respectively. By performing multiplications and summations between the kernel and the pixels, horizontal and vertical gradients are obtained. These gradients are then used to compute the edge magnitude and direction.

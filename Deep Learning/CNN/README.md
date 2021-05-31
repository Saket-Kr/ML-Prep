In mathematics convolution is a mathematical operation on two functions that produces a third function expressing how the shape of one is modified by the other. The term convolution refers to both the result function and to the process of computing it.  
They leverage spatial information and are therefore very well suited for classifying images. 

CNN has three main types of layers, which are:
- Convolutional layer - A filter (generally of size 3x3), is applied to an area of the image, and a dot product is calculated. This dot product is then fed into an output array. Afterwards, the filter shifts by a stride, repeating the process until the kernel has swept across the entire image. The final output from the series of dot products from the input and the filter is known as a *feature map*, *activation map*, or a *convolved feature*.

Since the output array does not need to map directly to each input value, convolutional (and pooling) layers are commonly referred to as “partially connected” layers. However, this characteristic can also be described as local connectivity.
Note that the weights in the feature detector remain fixed as it moves across the image, which is also known as parameter sharing. 

__Hyperparameters__
1. The number of filters affects the depth of the output. For example, three distinct filters would yield three different feature maps, creating a depth of three. 

2. Stride is the distance, or number of pixels, that the kernel moves over the input matrix. While stride values of two or greater is rare, a larger stride yields a smaller output.

3. Zero-padding is usually used when the filters do not fit the input image. This sets all elements that fall outside of the input matrix to zero, producing a larger or equally sized output. There are three types of padding:

  - Valid padding: This is also known as no padding. In this case, the last convolution is dropped if dimensions do not align.
  - Same padding: This padding ensures that the output layer has the same size as the input layer
  - Full padding: This type of padding increases the size of the output by adding zeros to the border of the input.

- Pooling layer
-Fully-connected (FC) layer


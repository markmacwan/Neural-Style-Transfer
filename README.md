# Neural-Style-Transfer
Neural Style Transfer on VGG 19 model.


Neural style transfer is an optimization technique used to take two images—a **content image** and a **style reference image** (such as an artwork by a famous painter)—and blend them together so the output image looks like the content image, but “painted” in the style of the style reference image.

This is implemented by optimizing the output image to match the content statistics of the content image and the style statistics of the style reference image. These statistics are extracted from the images using a convolutional network.

In this kernel, I have implemented the style trasnfer method outlined in the papers [Image Style Transfer Using Convolution Neural Networks](https://ieeexplore.ieee.org/document/7780634 "Image Style Transfer Using Convolution Neural Networks") and [Visualizing and Understanding Convolutional Networks](https://arxiv.org/pdf/1311.2901.pdf "Visualizing and Understanding Convolutional Networks").

Style transfer uses the features found in the 19-layer VGG Network, which is comprised of a series of convolutional and pooling layers, and a few fully-connected layers. The convolutional layers are named by stack and their order in the stack. Conv_1_1 is the first convolutional layer that an image is passed through, in the first stack. Conv_2_1 is the first convolutional layer in the second stack. The deepest convolutional layer in the network is conv_5_4.

###Distinguishing Style and Content
Style transfer relies on separating the content and style of an image. Given one content image and one style image, we aim to create a new, target image which should contain our desired content and style components:

-Objects and their arrangement are similar to that of the content image.
-Style, colors, and textures are similar to that of the style image

![](https://github.com/markmacwan/Neural-Style-Transfer/blob/main/Resources/style.png)

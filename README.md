# PyramidNet-caffe
Caffe implementation of the paper "Deep Pyramidal Residual Networks" (https://arxiv.org/abs/1610.02915).
This repository contains the code for the paper:

Dongyoon Han*, Jiwhan Kim*, and Junmo Kim, "Deep Pyramidal Residual Networks", CVPR 2017 (* equal contribution).

Arxiv: https://arxiv.org/abs/1610.02915. 

## Abstract
 Deep convolutional neural networks (DCNNs) have shown remarkable performance in image classification tasks in recent years. Generally, deep neural network architectures are stacks consisting of a large number of convolution layers, and they perform downsampling along the spatial dimension via pooling to reduce memory usage. At the same time, the feature map dimension (i.e., the number of channels) is sharply increased at downsampling locations, which is essential to ensure effective performance because it increases the capability of high-level attributes. Moreover, this also applies to residual networks and is very closely related to their performance. In this research, instead of using downsampling to achieve a sharp increase at each residual unit, we gradually increase the feature map dimension at all the units to involve as many locations as possible. This is discussed in depth together with our new insights as it has proven to be an effective design to improve the generalization ability. Furthermore, we propose a novel residual unit capable of further improving the classification accuracy with our new network architecture. Experiments on benchmark CIFAR datasets have shown that our network architecture has a superior generalization ability compared to the original residual networks.

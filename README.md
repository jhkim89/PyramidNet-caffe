# PyramidNet-caffe
Caffe implementation of the paper "Deep Pyramidal Residual Networks" (https://arxiv.org/abs/1610.02915).

This repository contains the code for the paper:

Dongyoon Han*, Jiwhan Kim*, and Junmo Kim, "Deep Pyramidal Residual Networks", CVPR 2017 (* equal contribution).

## Abstract
 Deep convolutional neural networks (DCNNs) have shown remarkable performance in image classification tasks in recent years. Generally, deep neural network architectures are stacks consisting of a large number of convolution layers, and they perform downsampling along the spatial dimension via pooling to reduce memory usage. At the same time, the feature map dimension (i.e., the number of channels) is sharply increased at downsampling locations, which is essential to ensure effective performance because it increases the capability of high-level attributes. Moreover, this also applies to residual networks and is very closely related to their performance. In this research, instead of using downsampling to achieve a sharp increase at each residual unit, we gradually increase the feature map dimension at all the units to involve as many locations as possible. This is discussed in depth together with our new insights as it has proven to be an effective design to improve the generalization ability. Furthermore, we propose a novel residual unit capable of further improving the classification accuracy with our new network architecture. Experiments on benchmark CIFAR datasets have shown that our network architecture has a superior generalization ability compared to the original residual networks.

<img src="https://cloud.githubusercontent.com/assets/22743125/19235579/7e7e33c6-8f2d-11e6-9397-1b505688e92a.png" width="960">

Figure 1: Schematic illustration of (a) basic residual units, (b) bottleneck, (c) wide residual units, and (d) our pyramidal residual units. 

<img src="https://cloud.githubusercontent.com/assets/22743125/19235610/bb3d5fd0-8f2d-11e6-84bd-46c9b7a4797a.png" width="640">

Figure 2: Visual illustrations of (a) additive PyramidNet, (b) multiplicative PyramidNet, and (c) comparison of (a) and (b).

## Results

#### ImageNet

Top-1 and Top-5 error rates of single-model, single-crop (224*224) on ImageNet dataset.  We use the additive PyramidNet for our results. 

| Network                                   | # of parameters | Output feat. dimension | Top-1 error | Top-5 error |
| ----------------------------------------- | --------------- | ---------------------- | ----------- | ----------- |
| ResNet-101                                | 44.5M           |  2048                  | 23.6        | 7.1         |
| PyramidNet-101, alpha=250                 | **23.5M**       |  1256                  | **23.24**   | **6.59**        |
| ResNet-152                                | 60.0M           |  2048                  | 23.0        | 6.7         |
| PyramidNet-152, alpha=200                 | **26.0M**       |  1056                  | **22.44**   | **6.14**        |
| PyramidNet-200, alpha=300                 | 62.1M           |  1456                  | **20.41**   | **5.16**        |
| PyramidNet-200, alpha=450, Dropout (0.5)  | 116.4M          |  2056                  | **20.27**   | **5.49**        |

Model files download: [link](https://1drv.ms/f/s!AmNvwgeB0n4GsiDFDNJWZkEbajJf)

## Notes

1. The ImageNet results are obtained using the uploaded codes. 
2. When testing with our model, please do not forget to use **a scale factor (0.017352)**.

## Contact
Jiwhan Kim (jhkim89@kaist.ac.kr),
Dongyoon Han (dyhan@kaist.ac.kr),
Junmo Kim (junmo.kim@kaist.ac.kr)


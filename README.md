# Overview

Udacity Deep Learning nanodegree course project on GANs

## About

Adverserial networks are trained on a small subset of [CelebFaces Attirbutes Dataset (CelebA)](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html). The images are cropped to remove parts of the image that don't include a face. Final shape is 64x64x3. Dataset can be obtained from [this link](https://s3.amazonaws.com/video.udacity-data.com/topher/2018/November/5be7eb6f_processed-celeba-small/processed-celeba-small.zip).

The networks and hyperparameters are selected based on the following papers: [DCGAN](https://arxiv.org/pdf/1511.06434.pdf), [CycleGAN](https://arxiv.org/pdf/1703.10593.pdf)

## Steps

1. data loader function is created including necessary transforms. Batch size of 128 and image size of 32 is selected.
2. Discriminator network is defined 
  * 4 convolutional layers starting from 32 channels to 512 channels. Conv layers except the first one has batch normalization
  * 1 fully connected layer
  * Activations are leaky ReLU
3. Generator network is defined
  * Similar to discriminator using transpose convolutions.
  * All the layers except the last are activate by ReLU. The last activation is tanh
4. Weight initializations are based on the DCGAN paper.

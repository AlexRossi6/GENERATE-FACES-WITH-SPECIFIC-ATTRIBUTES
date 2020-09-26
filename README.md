# Generate faces with specific attributes

<hr>

## Description
The project concerns the creation of a face generator and of a conditional face generator. In particular, the structure that has been used is the one of Generative Adversarial Networks (GAN) and Conditional Generative Adversarial Networks.

The data and the attributes that have been used for the training come from the CelebA dataset.


## Model architecture

![image](https://user-images.githubusercontent.com/56583448/94338491-eeb18000-fff2-11ea-822f-4b88bcbdf5c7.png)

## Examples of faces conditionally generated


         ![image](https://user-images.githubusercontent.com/56583448/94338520-346e4880-fff3-11ea-9a75-dc06940db63a.png)

         ![image](https://user-images.githubusercontent.com/56583448/94338532-641d5080-fff3-11ea-8876-3ac545741b54.png)

![image](https://user-images.githubusercontent.com/56583448/94338551-7d260180-fff3-11ea-9558-aa9bbbba1f10.png)

![movie](https://user-images.githubusercontent.com/56583448/94338563-962eb280-fff3-11ea-94d0-f325e0a20559.gif)

## Conclusions

The aim of this project was to develop a face generator and a conditional face generator able to generate new samples similar to training data according to user specified attributes. A Generative Adversarial network has been developed with a resulting FID score of 23. The most eective changes done to the GAN, that allowed us to obtain these results, have been the normalization of the images in the range [-1,1] and the usage of Leaky ReLU activation function.
The conditional generator, for which the same architectures of the GAN have been used, gained in performance with a random normal kernel initializer. The FID score in the Conditional GAN has been computed by generating images with random labels taken from the CelebA dataset, and had a value of 12.

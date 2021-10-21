# Generate faces with specific attributes
# https://alexrossi5187.medium.com/generate-faces-with-specific-attributes-1d9701950b36
<hr>

## Description
The project concerns the creation of a face generator and of a conditional face generator. In particular, the structure that has been used is the one of Generative Adversarial Networks (GAN) and Conditional Generative Adversarial Networks.

The data and the attributes that have been used for the training come from the CelebA dataset.


## Model architecture

![image](https://user-images.githubusercontent.com/56583448/94338491-eeb18000-fff2-11ea-822f-4b88bcbdf5c7.png)

## Examples of faces conditionally generated



![image](https://user-images.githubusercontent.com/56583448/94338606-fe7d9400-fff3-11ea-8e75-e71ca4e67b55.png)

Young Blonde Woman








![image](https://user-images.githubusercontent.com/56583448/94338619-1a813580-fff4-11ea-84d9-b798829a8b7c.png)

Old man with grey hair






![image](https://user-images.githubusercontent.com/56583448/94338644-3a185e00-fff4-11ea-83bb-48b3dfaa9160.png)

Young, attractive man with black hair, 5 o' clock shadow and smiling with mouth slightly open







![image](https://user-images.githubusercontent.com/56583448/94338661-56b49600-fff4-11ea-919c-3e7e46702a23.png)

Old woman with blonde hair and eyeglasses





![movie](https://user-images.githubusercontent.com/56583448/94338563-962eb280-fff3-11ea-94d0-f325e0a20559.gif)

GIF that explores the evolution of generator performance during the epochs


## Conclusions

The aim of this project was to develop a face generator and a conditional face generator able to generate new samples similar to training data according to user specified attributes. A Generative Adversarial network has been developed with a resulting FID score of 23. The most effective changes done to the GAN, that allowed us to obtain these results, have been the normalization of the images in the range [-1,1] and the usage of Leaky ReLU activation function.
The conditional generator, for which the same architectures of the GAN have been used, gained in performance with a random normal kernel initializer. The FID score in the Conditional GAN has been computed by generating images with random labels taken from the CelebA dataset, and had a value of 12.

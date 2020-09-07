# Semantic Segmentation on CamVid Dataset using U-Net.

## Description
This repository is made in attempt to implement the [U-Net paper](https://arxiv.org/abs/1505.04597). We implemented the convolutional neural network architecture given in the paper. There are [32 classes](http://mi.eng.cam.ac.uk/research/projects/VideoRec/CamVid/#ClassLabels) in total.

![alt text](https://camo.githubusercontent.com/f4175e0e30153e03c7ac42a1779302d990b918d0/68747470733a2f2f6d69726f2e6d656469756d2e636f6d2f6d61782f313030302f312a77626155516b597a5268766d6437496a4b4a6a6a43672e676966)

## TODO
- [x] Minimal implementation of the U-Net
- [x] Complete Readme
- [ ] Visualizing output of the model
- [ ] Adding different metrics to evaluate performance

## Semantic Segmentation
Semantic segmentation refers to the process of mapping/classifying each pixel in an image to a class label. It can also be referred to as **image classification** for pixels in an image. Its primary applications include autonomous vehicles, human-computer interaction, robotics and photo-editing tools. It is very useful for delf-driving cars in which contextual information of the environment is required at each and every step while traversing the route.

## Network Architechture
The network architecture mentioned in the [U-Net paper](https://arxiv.org/abs/1505.04597) is used. The first half of the U-Net is an encoding task and the second half is a reconstruction task. To get the confidence scores in the form of a probabilities, we use the softmax activation function at the output layer. And then we choose cross entropy loss as our error function.

### Softmax Activation is given by

<img src="https://render.githubusercontent.com/render/math?math=\large \frac{exp(x_i)}{\sum_{j=1}^{n}exp(x_j)}"> 

### Cross Entropy Loss is given by

<img src="https://render.githubusercontent.com/render/math?math=\large \ell(x, class) = -log(\frac{exp(x[class])}{\sum_{j=1}^{n}exp(x[j])})"> 


![alt text](https://miro.medium.com/max/2824/1*f7YOaE4TWubwaFF7Z1fzNw.png)

## Dataset Description
The Cambridge-driving Labeled Video Database (CamVid) is the first collection of videos with object class semantic labels, complete with metadata. The database provides ground truth labels that associate each pixel with one of 32 semantic classes. The dataset can be found [here](http://mi.eng.cam.ac.uk/research/projects/VideoRec/CamVid/#ClassLabels).

## Deep Learning Framework used
[Pytorch](https://pytorch.org/)

## External References
[Reference 1](https://medium.com/@bond.kirill.alexandrovich/understanding-unet-27de538e08d8)

[Reference 2](https://towardsdatascience.com/understanding-semantic-segmentation-with-unet-6be4f42d4b47)

# EC601-project3

## phase1

# Prerequisites
- torchvision
Installation:

Anaconda:
``` 
conda install torchvision -c soumith 
```
pip:
```
pip install torchvision
```
For optimaztion, we use torch.optim
Examples:
```
optimizer = optim.SGD(model.parameters(), lr=0.01, momentum=0.9)
optimizer = optim.Adam([var1, var2], lr=0.0001)
```
# overview
In this project, the goal is to implement a complicated system that are related to our team project. As a result, I choose to implement a transfer learning model using pytorch. As in Visual Question Answering, classifing images to certain catogories seems to be crucial, so in this case I chose to run a image classification trasnfer leaning module. Considering we are processing high amount of images and those images' size differes, we firstly do a normalization using  `torchvision ` to initialize all the images to a [-1,1] verctor range. In this case, we are seperating ants and bees. We have about 120 training images, each image is used for ants and bees. There are 75 verification images for each class. Usually, if you start training from scratch, this is a very small data set.
The whole training takes up to 25 mins in my laptop, and the result is showed below:


<img width="1194" alt="Screen Shot 2020-10-19 at 11 20 12" src="https://user-images.githubusercontent.com/52185318/96471672-950d3180-11fd-11eb-86dd-4da47c4ca571.png">




```
Epoch 1/24
----------
train Loss: 0.4725 Acc: 0.8115
val Loss: 0.2793 Acc: 0.8889

Epoch 2/24
----------
train Loss: 0.4257 Acc: 0.8402
val Loss: 0.3542 Acc: 0.8627

Epoch 3/24
----------
train Loss: 0.5246 Acc: 0.7746
val Loss: 0.3639 Acc: 0.8954

Epoch 4/24
----------
train Loss: 0.4339 Acc: 0.8361
val Loss: 0.3268 Acc: 0.8497

Epoch 5/24
----------
train Loss: 0.4519 Acc: 0.8279
val Loss: 0.2749 Acc: 0.8889

Epoch 6/24
----------
train Loss: 0.2364 Acc: 0.8893
val Loss: 0.2005 Acc: 0.9150

Epoch 7/24
----------
train Loss: 0.4177 Acc: 0.8361
val Loss: 0.2208 Acc: 0.8954

Epoch 8/24
----------
train Loss: 0.2750 Acc: 0.8893
val Loss: 0.1966 Acc: 0.9412

Epoch 9/24
----------
train Loss: 0.3431 Acc: 0.8402
val Loss: 0.1903 Acc: 0.9346

Epoch 10/24
----------
train Loss: 0.4004 Acc: 0.8566
val Loss: 0.1813 Acc: 0.9346

Epoch 11/24
----------
train Loss: 0.3768 Acc: 0.8484
val Loss: 0.1777 Acc: 0.9346

Epoch 12/24
----------
train Loss: 0.3228 Acc: 0.8566
val Loss: 0.1609 Acc: 0.9477

Epoch 13/24
----------
train Loss: 0.3252 Acc: 0.8689
val Loss: 0.1596 Acc: 0.9281

Epoch 14/24
----------
train Loss: 0.2704 Acc: 0.8852
val Loss: 0.1697 Acc: 0.9281

Epoch 15/24
----------
train Loss: 0.3311 Acc: 0.8525
val Loss: 0.1799 Acc: 0.9216

Epoch 16/24
----------
train Loss: 0.2975 Acc: 0.8607
val Loss: 0.1626 Acc: 0.9281

Epoch 17/24
----------
train Loss: 0.3205 Acc: 0.8484
val Loss: 0.1688 Acc: 0.9346

Epoch 18/24
----------
train Loss: 0.3765 Acc: 0.8197
val Loss: 0.1660 Acc: 0.9346

Epoch 19/24
----------
train Loss: 0.3387 Acc: 0.8566
val Loss: 0.1637 Acc: 0.9477

Epoch 20/24
----------
train Loss: 0.2634 Acc: 0.9016
val Loss: 0.1788 Acc: 0.9150

Epoch 21/24
----------
train Loss: 0.2630 Acc: 0.9016
val Loss: 0.1768 Acc: 0.9412

Epoch 22/24
----------
train Loss: 0.3093 Acc: 0.8770
val Loss: 0.1699 Acc: 0.9412

Epoch 23/24
----------
train Loss: 0.3388 Acc: 0.8607
val Loss: 0.2031 Acc: 0.9020

Epoch 24/24
----------
train Loss: 0.2882 Acc: 0.8648
val Loss: 0.1675 Acc: 0.9150

Training complete in 24m 55s
Best val Acc: 0.947712
```

# Result Analysis
The overall training for 24 Epochs takes about 25 minutes, each Epoch for about 1 minute. The accuracy is quite good, ranging from 0.84 to 0.94. From this result, I believe it is enough for me to use it for my own data training.

## Sprint2 
As I have successfully implemented the transfer leaning model, now I'm going to test it with my own data. 
The data can be downloaded from COCODataset https://cocodataset.org/#home.
However,due to large volume of data, which is beyond handler of my own laptop, I'm now considering using a school GPU for further processing.









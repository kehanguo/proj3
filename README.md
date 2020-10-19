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


<img width="1195" alt="Screen Shot 2020-10-18 at 22 38 34" src="https://user-images.githubusercontent.com/52185318/96465669-36dd5000-11f7-11eb-9df6-aba0f1c3f08d.png">



<img width="1190" alt="Screen Shot 2020-10-19 at 10 51 22" src="https://user-images.githubusercontent.com/52185318/96467862-63926700-11f9-11eb-87e0-cb40cc029773.png">

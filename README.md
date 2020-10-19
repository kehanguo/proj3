## project3
In this project, the goal is to implement a complicated system that are related to our team project. As a result, I choose to implement a transfer learning model using pytorch. As in Visual Question Answering, classifing images to certain catogories seems to be crucial, so in this case I chose to run a image classification trasnfer leaning module. Considering we are processing high amount of images and those images' size differes, we firstly do a normalization using  `torchvision ` to initialize all the images to a [-1,1] verctor range. In this case, we are seperating ants and bees. We have about 120 training images, each image is used for ants and bees. There are 75 verification images for each class. Usually, if you start training from scratch, this is a very small data set.
The whole training takes up to 25 mins in my laptop, and the result is showed below:


<img width="1195" alt="Screen Shot 2020-10-18 at 22 38 34" src="https://user-images.githubusercontent.com/52185318/96465669-36dd5000-11f7-11eb-9df6-aba0f1c3f08d.png">

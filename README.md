# Residual-Network-Project
This repository is for ECE-7123 Deep Learning Mini-Project1.

Our team members:

* Name: Zilong Wu &emsp;  NetID: zw2599
* Name: Jianing Chen &emsp; NetID: jc10034
* Name: Xuchen Hu &emsp; NetID: xh2090

## Data Augmentation
This mini project builds a small ResNet architecture to classify images from CIFAR10 and archives over 90% accuracy. In the project, we used 7 different individual augmentation strategies including **crop, flip, color distort, cutout, rotation and Guassian blur**. In the project report we compose different augmentation together with different orders. To realize the composition we need to reconstruct the composition. 

For example, to build crop + vertical flip we need to build:
````
transforms.Compose([
                        transforms.RandomResizedCrop(32,(0.8,1.0)),
                        transforms.RandomVerticalFlip(),
                        transforms.ToTensor(),                 
])
````

Other compositions could be structured in the same way. In the final architecture we build the crop + Horizontal flip + cutout, the result of augmentation is shown in the figure below:


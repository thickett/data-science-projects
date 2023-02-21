#### Project Overview

In this project we hope to accurately classify a variety of colon-related diseases using medical images. We will be limited on computing power so the size of the models we can build from scratch will be quite small, later in the project, we get around this by utilising transferred learning and incorporating the architecture, and weights of much larger and much more sophisticated models.

We also build a sophistacted keras tuning framework using a sort of genetic algorithm to make decisions on the number of branches and layers, the types of layers, the amount of regularization and so on.

In the end we were able to build a model that used Xception as a base with a small task-specific layer built ontop and a collection of data augmentations that achieved an f1-score of 0.90. One of the 4 classes proved to be harder to correctly predict than the others, this class can be identified in the below images which shows the outputs of a sub-sample of layers for different channels on a seperate image for each of the four classes. 

**Note:** The below image shows the first eight channel outputs for the first three convolution layers, named on the y axis for each of the 4 classes, named on the x-axis.

![Final Model channel image](https://github.com/thickett/data-science-projects/blob/main/Colon%20Disease%20deep%20learning/final_image_small.PNG)


#### Key skills utalised:

* Tensorflow
* Tensorboard
* Keras Tuning
* Building CNNs from scratch
* automating the process of building multi-branch inception models from scratch
* training, optimizing and fine-tuning transfer-learning models
* Optimizing in-memory usage for maximum performance
* Data augmentation

# FoodC
FoodC AICrowd Blitz May 2020

## Solution Explanation

I used several pretrained neural networks (EfficientNet, Resnet and Densenet) with different depth to classify the images.

The best setup I found for the learning rate was to decrease it after a few epochs (7 seemed reasonable) and then using a few warm restarts to create many checkpoints for each type of architecture
I was also experimenting with different Data Augmentation scenarios and class-weighted loss, but these didn't seem to play a large role.

Most of the models achieved between 0.61 and 0.655 on the test set. The best individual model was EfficientNet-B1 which achieved 0.655 F1 score.

Taking a majority voting across a bunch of them (~150) lead to my best score of 0.676.
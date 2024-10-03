# Image Classification for ChestXray Direction Prediction

This repository uses the miniJSRT_database, which is a small dataset of Chest X-rays that can be used by beginners in image processing. The dataset can ben found here: http://imgcom.jsrt.or.jp/minijsrtdb/

For this project, the Directions dataset was used, which contains 988 pictures in different direction. There were 247 images in each of the following directions: up, down, right and left, out of which 948 were used for training and 40 for testing. Each picture was of size 128x128. I used the RGB dataset. A sample of the first five pictures can be seen below.

The architecture used for training was Resnet18. I used the same code I created in the pre-warm-up exercise. Since this dataset had 3 input channels, I was able to keep the set up of the first convolution layer of the Resnet18. I did change the number of output features of the final layer to have 4 output options, which are the 4 possible directions.

To train the model, I created data loaders of size 10 and I ran 10 epochs. That returned a very small value to the loss function during training. To check how well the predictions were, I used the test dataset and saw very high accuracy of 1.00 in all test images. The model performed very well with the dataset provided, even with little training.


# Cat vs Dog Classification CNN

This project is a ```Convolutional Neural Network (CNN)``` for classifying cats and dogs written in python with the Tensorflow library. The model was run on kaggle and can be run anyone by visiting this link:


https://www.kaggle.com/code/adnansilajdi/cat-vs-dog-2

Feel free to visit the link and test it yourself!

## Dataset

The dataset used for this project is the "Cats-vs-Dogs" dataset published by Microsoft. This project did not use the original version of the dataset, but a reposted version which pre-unzipped all the images for our convenience. The dataset can be found on this link:

https://www.kaggle.com/datasets/shaunthesheep/microsoft-catsvsdogs-dataset

It contains a total of about 25000 images, half of which are images of dogs while the other half are images of cats. This project uses about 11000 images for each class, downscaling them to 80x80 resolution before normalizing them.

## Performance

The current accuracy of the model is about 88% when tested on over 4000 random images. In order to increase performance multiple things can be done. 

Firstly, the amount of images used for training can be increased for a smaller chance of overfitting. This was not done in the current version of the project due to RAM limitations. 

Secondly, increasing the image resolution might lead to better performance. However, this was not able to be tested due to RAM limitations as well. 

## The Model



| Layer (type) | Output Shape     | Param #        |
| :-------- | :------- | :------------------------- |
| `Convolution 2D` | (80, 80, 16) |448   |
| `Max Pooling 2D` | (40, 40, 16) |0   |
| `Convolution 2D` | (40, 40, 32) | 4640  |
| `Max Pooling 2D` | (20, 20, 32) |0   |
| `Convolution 2D` | (20, 20, 64) | 18496 |
| `Max Pooling 2D` | (10, 10, 64) |0   |
| `Convolution 2D` | (10, 10, 64) | 36928|
| `Max Pooling 2D` | (5, 5, 64) |0   |
| `Flatten` | (1600) |0   |
| `Dropout` | (1600) |0   |
| `Dense` | (128) | 204928   |
| `Dropout` | (128) |0   |
| `Dense` | (256) | 33024   |
| `Dense` | (1) | 257   |

Total paramaters: 298,721









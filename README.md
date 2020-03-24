# FERPlus-Emotion-Recognition-using-keras
This is a repository about using keras to do emotion recognition on FERPlus dataset

## FERPlus dataset
The [FERPlus (FER+)](https://github.com/microsoft/FERPlus) annotations provide a set of new labels for the standard Emotion [FER dataset](https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge/data), which is thought to be more accuract than the original FER2013 annotations.

The new label file is named [fer2013new.csv]((https://github.com/microsoft/FERPlus)) and contains the same number of rows as the original [fer2013.csv]((https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge/data)) label file with the same order, so that you infer which emotion tag belongs to which image. 

## The main purpose

The main purpose of this repository is to replicate the pretrained CNN models' performances in this [blog](http://www.robots.ox.ac.uk/~albanie/pytorch-models.html), which has the model weights in Pytorch and MatConvNet, but not in tensorflow or keras.

## Requirements

* Tensorflow 1.14.0 or higher
* keras 2.2.4 or higher
* [keras_contrib](https://github.com/keras-team/keras-contrib)
* [keras_vggface](https://github.com/rcmalli/keras-vggface)
* [albumentations](https://github.com/albumentations-team/albumentations)

## Training

The training dataset is FERPlus. Data augmentations, such as random cropping and horizontal flipping are applied. The class weights are set to [2.74398525, 3.56296941, 7.9199129, 8.44722581, 12.27334083, 215.34868421, 50.51388889, 230.51408451] to match their distribution.

<img src="https://github.com/wtomin/FERPlus-Emotion-Recognition-using-keras/blob/master/FERPlus_dis.png" width="800">

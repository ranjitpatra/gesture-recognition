# Neural Networks Project - Gesture Recognition
## Problem Statement
Imagine you are working as a data scientist at a home electronics company which manufactures state of the art smart televisions. You want to develop a cool feature in the smart-TV that can recognise five different gestures performed by the user which will help users control the TV without using a remote.

The gestures are continuously monitored by the webcam mounted on the TV. Each gesture corresponds to a specific command:

- Thumbs up: Increase the volume
- Thumbs down: Decrease the volume
- Left swipe: 'Jump' backwards 10 seconds
- Right swipe: 'Jump' forward 10 seconds
- Stop: Pause the movie


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
Each video is a sequence of 30 frames (or images). The training data consists of a few hundred videos categorised into one of the five classes. Each video (typically 2-3 seconds long) is divided into a sequence of 30 frames(images). These videos have been recorded by various people performing one of the five gestures in front of a webcam - similar to what the smart TV will use.

The data is in a zip file. The zip file contains a 'train' and a 'val' folder with two CSV files for the two folders. These folders are in turn divided into subfolders where each subfolder represents a video of a particular gesture. Each subfolder, i.e. a video, contains 30 frames (or images). Note that all images in a particular video subfolder have the same dimensions but different videos may have different dimensions. Specifically, videos have two types of dimensions - either 360x360 or 120x160 (depending on the webcam used to record the videos). Hence, you will need to do some pre-processing to standardise the videos.

Each row of the CSV file represents one video and contains three main pieces of information - the name of the subfolder containing the 30 images of the video, the name of the gesture and the numeric label (between 0-4) of the video.

Your task is to train a model on the 'train' folder which performs well on the 'val' folder as well (as usually done in ML projects). We have withheld the test folder for evaluation purposes - your final model's performance will be tested on the 'test' set.



> Dataset - https://drive.google.com/uc?id=1ehyrYBQ5rbQQe6yL4XbLWe3FMvuVUGiL

## Technologies Used
- Google Collab + jupyter Notebook
- python - version 3.9.1
- numpy - version 1.23.4
- matplotlib - version 3.6.2
- keras - version 2.12.0
- tensorflow - version 2.12.0

## Conclusions

- Model 1 (Base Model) - Is over-fit.
- Model 2 (with data augmentation + dropouts) - Resolves overfitting issue but observed as underfit.
- Model 3 (Fixed Class Imbalance by adding 500 images to each class using Augmentor + BN + 30 epochs - Class Rebalance helped to increase the Train and Validation accuracy.

## Acknowledgements
Give credit here.
- This project was inspired by Upgrad and IIIT Bangalore.
- Upgrad course learning content, live session and Google search.


## Contact
Created by [[@ranjitpatra](https://github.com/ranjitpatra)] - feel free to contact!
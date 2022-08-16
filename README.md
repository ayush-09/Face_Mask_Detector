# Face_Mask_Detector (COVID-19)

## Purpose of the Project
This project helps us to spread the awareness among people using face mask properly. It 
detects the face mask on your face whether the person is wearing mask or not and tells the percentage of the accuracy of wearing the face mask properly or not.

## Division of the Project

In order to train a custom face mask detector, I need to split our project into two distinct phases: 
- **Training Phase** (Training the model): <br>
  In this I will focus on loading our face mask detection datasets from disk, training a 
model using CNN on the datasets, and then serializing the face mask detector to disk.

- **Deployment Phase** (Deployment of the model): <br>
Once the face mask detector is trained, then move on to loading the mask detector, 
performing the face mask detection and then identifying each face as with mask or 
without mask.

![image](https://user-images.githubusercontent.com/51924622/184957736-17a83cf9-ff24-44bb-b444-fef5df1e4a8a.png)

## About the Dataset

Our face mask detector didn't uses any morphed masked images dataset. 
The dataset consists of **1,376 images** belonging to **two classes**:
* __with_mask: 690 images__
* __without_mask: 686 images__

I choose this dataset because it consists artificially dataset of people wearing masks. If you 
include the original images used to generate face mask samples as non-face mask samples, 
your model will become heavily biased and fail to generalize well. Avoid that at all costs by 
taking the time to gather new examples of faces without marks.

## TechStack/framework used

- [OpenCV](https://opencv.org/)
- [Caffe-based face detector](https://caffe.berkeleyvision.org/)
- [Keras](https://keras.io/)
- [TensorFlow](https://www.tensorflow.org/)
- [Convolutional Neural Network](https://www.interviewbit.com/blog/cnn-architecture/)
- [Scikit-learn](https://pypi.org/project/scikit-learn/)
- [Matplotlib](https://pypi.org/project/matplotlib/)

## Prerequisites
All the dependencies and required libraries are included in the file <code>requirements.text</code><br>
For live demo simply download my model and face detector and run the <code>video streaming.py</code><br>
Clone my repo and install the libraries and the run the <code>Face_Mask_detection.ipynb</code> colab notebook for the __image output__ and <code>video streaming.py</code> for __real-time detection__. 

## Building Model

![image](https://user-images.githubusercontent.com/51924622/184958505-587e3e68-6004-4751-8e5e-520140b37a84.png)

## Graphical Representation

![image](https://user-images.githubusercontent.com/51924622/184959136-4a8aac1a-19c0-419e-b59c-469b6e126346.png)

![image](https://user-images.githubusercontent.com/51924622/184959604-05f77e68-d387-49be-9c7d-7ae7ec237fbf.png)

## Classification Report

A Classification report is used to measure the quality of predictions from a classification 
algorithm. How many predictions are True and how many are False. More specifically, True 
Positives, False Positives, True negatives and False Negatives are used to predict the metrics 
of a classification report as shown below <br>

![image](https://user-images.githubusercontent.com/51924622/184960450-ef1371d0-7de2-428b-abb9-1591c006af84.png)


## Result

The accuracy of the model is **96%** after trained and tested on the images.

* __INPUT Img:__
![41698](https://user-images.githubusercontent.com/51924622/96024304-2f255080-0e71-11eb-99b8-ebeb3a8cc03c.jpg)

* __OUTPUT Img:__
![result1](https://user-images.githubusercontent.com/51924622/96024381-47956b00-0e71-11eb-9994-5816814a0200.png)

* __Another OUTPUT Img:__

![result](https://user-images.githubusercontent.com/51924622/96024389-495f2e80-0e71-11eb-8419-e9a21f71daba.png)

## Future Use

The model is accurate, and since we used the simple Sequential Model architecture, it’s also computationally efficient and thus making it easier to deploy the model to embedded systems (Raspberry Pi, Google Coral, etc.). 

This system can therefore be used in real-time applications which require face-mask detection for safety purposes due to the outbreak of Covid-19.  This project can be integrated with embedded systems for application in airports, railway stations, offices, schools, and public places to ensure that public safety guidelines.


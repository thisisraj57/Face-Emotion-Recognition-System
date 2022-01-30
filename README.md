# Face-Emotion-Recognition-System

# ABSTRACT

The Indian education landscape has been undergoing rapid changes for the past 10 years owing to the advancement of web-based learning services, specifically, eLearning platforms.

In a physical classroom during a lecture, the teacher can see the faces and assess the emotion of the class and tune their lecture accordingly, whether he is going fast or slow. He can identify students who need special attention. Digital classrooms are conducted via a video telephony software program (ex-Zoom) where it’s not possible Convthe to see all students and access the mood. Because of this drawback, students are not focusing on content due to a lack of surveillance. Digital platforms have limitations in terms of physical surveillance but it comes with the power of data and machines which can work for you. Its data can be analyzed using deep learning algorithms which not only solves the surveillance issue but also removes the human bias from the system.


# INTRODUCTION

A Facial expression is the visible manifestation of the affective state, cognitive activity, intention, personality and psychopathology of a person and plays a communicative role in interpersonal relations. Human facial expressions can be easily classified into 7 basic emotions: happy, sad, surprise, fear, anger, disgust, and neutral. Our facial emotions are expressed through activation of specific sets of facial muscles. These sometimes subtle, yet complex, signals in an expression often contain an abundant amount of information about our state of mind. Automatic recognition of facial expressions can be an important component of natural human machine interfaces; it may also be used in behavioral science and in clinical practice. It has been studied for a long period of time and obtained progress in recent decades. Though much progress has been made, recognizing facial expressions with a high accuracy remains to be difficult due to the complexity and varieties of facial expressions. On a day to day basis humans commonly recognize emotions by characteristic features, displayed as a part of a facial expression. For instance happiness is undeniably associated with a smile or an upward movement of the corners of the lips. Similarly other emotions are characterized by other deformations typical to a particular expression.

The objective of this project is to develop an Automatic Facial Expression Recognition System which can take human facial images containing some expression as input and recognize and classify it into seven different expression classes such as : 
*Neutral 
*Angry 
*Disgust 
*Fear 
*Happy
*Sadness 
*Surprise

# Problem Statement

To construct and face emotion recognition model for Live Class Monitoring System.

Human emotions and intentions are expressed through facial expressions and deriving angles. The efficient and effective feature is the fundamental component of the facial expression system. Facial expressions convey non-verbal cues, which play an important role in interpersonal relations.   Automatic recognition of facial expressions. can be an important component of natural human-machine interfaces. 
 
during counseling and other healthcare-related fields. In an E-Learning system, the presentation style may be varied depending on the student’s state. However, in many cases, static emotion detection is not very useful. It is essential to know the user’s feelings over a period of time in a live environment. Thus, the paper proposes a model that is aimed at real-time facial emotion recognition

# Data Summary

The data comes from the past Kaggle competition “Challenges in Representation Learning: Facial Expression Recognition Challenge”: we have defined the image size to 48 so each image will be reduced to a size of 48x48. The faces have been automatically registered so that the face is more or less centered and occupies about the same amount of space in each image. Each image corresponds to a facial expression in one of seven categories (0=Angry, 1=Disgust, 2=Fear, 3=Happy, 4=Sad, 5=Surprise, 6=Neutral). The dataset contains approximately 36K images.


# PROCESS OF PROJECT

Steps involved:


1. Exploratory Data Analysis

The dataset contains approximately 36K images. Each image corresponds to a facial expression in one of seven categories (0=Angry, 1=Disgust, 2=Fear, 3=Happy, 4=Sad, 5=Surprise, 6=Neutral). All the images are 48x48 pixels.

2. Data Image generator

Generate batches of tensor image data with real-time data augmentation.

3. Building models

We started our project with the concept of transfer learning i.e. using the pre-trained weights of ResNet50 for the training of the model and then fine-tuning them to increase the accuracy. Due to our dissatisfaction with this result, we switched to the Custom CNN model.

4. Training the model

We trained the model with 40 epochs and callback as early stopping and ReduceLROnPlateau to avoid overfitting and reach the global minima.

5. Model Evaluation

We evaluated the model using an accuracy plot and categorical cross-entropy loss and confusion matrix to find out in which category the model has inadequate performance and among which category the model is getting confused

6. Model Deployment

We have created a front-end using Streamlit for web app and used streamlit-webrtc which helped to deal with real-time video streams. Image captured from the webcam is sent to the VideoTransformer function to detect the emotion. Then this model was deployed on the Heroku platform with the help of buildpack-apt which is necessary to deploy the OpenCV model on Heroku.

Deployment Link for Heroku -

https://face-emotion-thisisraj.herokuapp.com/ 

Deployment Link for Streamlit Share -

https://share.streamlit.io/thisisraj57/face-emotion-recognition-system/main/app.py

Models:

Basic CNN architecture details:

Input layer - The input layer in CNN should contain image data

Convo layer - The convo layer is sometimes called the feature extractor layer because features of the image are get extracted within this layer

Pooling layer - Pooling is used to reduce the dimensionality of each feature while retaining the most important information. It is used between two convolution layer

Fully CL - Fully connected layer involves weights, biases, and neurons. It connects neurons in one layer to neurons in another layer. It is used to classify images between different categories by training and placed before the output layer

Output Layer - The output layer contains the label which is in the form of a one-hot encoded



1. ResNet50:

ResNet50 is a variant of the ResNet model which has 48 Convolution layers along with 1 MaxPool and 1 Average Pool layer. It has 3.8 x 10^9 Floating points operations.

The ResNets were initially applied to the image recognition task but as mentioned in the paper that the framework can also be used for non-computer vision tasks to achieve better accuracy.



# CONCLUSION

*We trained the neural network and we achieved the highest validation accuracy of 60.43%.
*The Pre Trained Model didn't give appropriate results.
*The application is able to detect face location and predict the right expression while checking it on a local webcam.
*The front-end of the model was made using streamlit for webapp and running well on local webapp links.
*Finally, we successfully deployed the Streamlit WebApp on Heroku and Streamlit share that runs on a web server.
*Our Model can successfully detect face and predict emotion on live video feed as well as on an image.

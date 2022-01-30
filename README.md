# Face-Emotion-Recognition-System

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


# PROCESS OF PROJECT

*It is found that for implementing this project four basic steps are required to be performed. i. Preprocessing ii. Face registration iii. Facial feature extraction iv. Emotion classification
*Facial expression recognition is a process performed by humans or computers, which consists of:
*Locating faces in the scene (e.g. in an image; this step is also referred to as face detection),
*Extracting facial features from the detected face region (e.g., detecting the shape of facial components or describing the texture of the skin in a facial area; this step is referred to as facial feature extraction),
*Analyzing the motion of facial features and/or the changes in the appearance of facial features and classifying this information into some facial-expression interpretation categories such as facial muscle activations like smile or frown, emotion (affect)categories like happiness or anger, attitude categories like (dis)liking or ambivalence, etc.(this step is also referred to as facial expression interpretation).


# CONCLUSION

*We trained the neural network and we achieved the highest validation accuracy of 60.43%.
*The Pre Trained Model didn't give appropriate results.
*The application is able to detect face location and predict the right expression while checking it on a local webcam.
*The front-end of the model was made using streamlit for webapp and running well on local webapp links.
*Finally, we successfully deployed the Streamlit WebApp on Heroku and Streamlit share that runs on a web server.
*Our Model can successfully detect face and predict emotion on live video feed as well as on an image.

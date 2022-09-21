# ECG Image Based Heartbeat Classification for Arrhythmia Detection Using IBM Watson Studio
 In this repository I have created Machine Learning Model Using IBM cloud Deployment
 ECG- Image Based Heartbeat Classification For Arrhythmia Detection Using IBM Watson Studio


Designed By:

Anshuman Raina


1. Introduction

1.1 Overview
According to the World Health Organization (WHO), cardiovascular diseases (CVDs) are the number one cause of death today. Over 17.7 million people died from CVDs in the year 2017 all over the world which is about 31% of all deaths, and over 75% of these deaths occur in low and middle-income countries. Arrhythmia is a representative type of CVD that refers to any irregular change from the normal heart rhythms. There are several types of arrhythmia including atrial fibrillation, premature contraction, ventricular fibrillation, and tachycardia. Although a single arrhythmia heartbeat may not have a serious impact on life, continuous arrhythmia beats can result in fatal circumstances. In this project, we build an effective electrocardiogram (ECG) arrhythmia classification method using a convolutional neural network (CNN), in which we classify ECG into seven categories, one being normal and the other six being different types of arrhythmia using deep two-dimensional CNN with grayscale ECG images. We are creating a web application where the user selects the image which is to be classified. 

1.2 Purpose
An electrocardiogram (ECG) measures the electric activity of the heart and has been widely used for detecting heart diseases due to its simplicity and non-invasive nature. By analyzing the electrical signal of each heartbeat, i.e., the combination of action impulse waveforms produced by different specialized cardiac tissues found in the heart, it is possible to detect some of its abnormalities. 

2. Literature Survey

2.1 Existing Problem
Cardiovascular diseases (CVDs) are the number one cause of death today. Over 17.7 million people died from CVDs in the year 2017 all over the world which is about 31% of all deaths, and over 75% of these deaths occur in low and middle-income countries. Arrhythmia is a representative type of CVD that refers to any irregular change from the normal heart rhythms. There are several types of arrhythmia including atrial fibrillation, premature contraction, ventricular fibrillation, and tachycardia.

2.2 Proposed Solution
An "ambulatory electrocardiogram" or an ECG) about the size of a postcard or digital camera that you'll use for 1 to 2 days, or up to 2 weeks. The test measures the movement of electrical signals or waves through your heart. These signals tell the heart to contract (squeeze) and pump blood.  You'll have electrodes taped to your skin. It's painless, although some people have mild skin irritation from the tape used to attach the electrodes to the chest. You can do everything but shower or bathe while wearing the electrodes. After the test period, you'll go back to see your doctor. They'll download the information.

3. Theoritical Analysis

3.1 Block Diagram

3.2 Hardware/Software Designing
The Training model is created using Convolutional Neural Networks (Machine Learning) and Computer Vision and the Interface is created in Flask using IBM Watson AI.

4. Experimental Investigation

In this project, we have deployed our training model using CNN on IBM Watson studio. We are deploying 4 types of CNN layers in a sequential manner , starting from :
1) Convolutional layer 2D which convolutes independently of the feature map of the previous layer. The output of the convolution layer is obtained by offsetting the convolution kernel and transferring it to the nonlinear activation function.

2) Pooling Layer  Convolution of the next layer is commonly the pooling layer. By reducing the dimension of convolution layer output data, network complexity is reduced, as well as overfitting phenomenon. Robustness of the network is enhanced in this process. The pooling layer averages or maximizes the output features of the convolutional layer, and the corresponding methods are respectively, average pooling or maximum pooling.

3) Fully-Connected layer After extracting features from multiple convolution layers and pooling layers, the fully-connected layer is used to expand the connection of all features. Finally, the SoftMax layer makes a logistic regression classification. Fully-connected layer transfers the weighted sum of the output of the previous layer to the activation function.

4) Dropout Layer There is usually a dropout layer before the fully-connected layer. The dropout layer will temporarily disconnect some neurons from the network according to the certain probability during the training of the convolution neural network, which reduces the joint adaptability between neuron nodes, reduces overfitting, and enhances the generalization ability of the network.

5. Project Flow:

User interacts with User interface to upload image Uploaded image is analyzed by the model which is integrated Once model analyses the uploaded image, the prediction is showcased on the UI To accomplish this, we have to complete all the activities and tasks listed below

Data Collection. Collect the dataset or Create the dataset Data Preprocessing. Import the ImageDataGenerator library Configure ImageDataGenerator class Apply ImageDataGenerator functionality to Trainset and Testset Model Building Import the model building Libraries Initializing the model Adding Input Layer Adding Hidden Layer Adding Output Layer Configure the Learning Process Training and testing the model Optimize the Model Save the Model Application Building Create an HTML file Build Python Code

We are building a Flask Application that needs HTML pages stored in the templates folder and a python script app.py for serverside scripting we need the model which is saved and the saved model in this content is ECG.h5 The static folder will contain js and CSS files. Whenever we upload an image to predict, that images are saved in the uploads folder.

Prerequisites To complete this project you should have the following software and packages

Anaconda Navigator :

Anaconda Navigator is a free and open-source distribution of the Python and R programming languages for data science and machine learning related applications. It can be installed on Windows, Linux, and macOS.Conda is an open-source, cross-platform, package management system. Anaconda comes with so very nice tools like JupyterLab, Jupyter Notebook, QtConsole, Spyder, Glueviz, Orange, Rstudio, Visual Studio Code. For this project, we will be using Jupiter notebook and spyder

To build Deep learning models you must require the following packages

Tensor flow: TensorFlow is an end-to-end open-source platform for machine learning. It has a comprehensive, flexible ecosystem of tools, libraries, and community resources that lets researchers push the state-of-the-art in ML and developers can easily build and deploy ML powered applications.

Keras : Keras leverages various optimization techniques to make high level neural network API easier and more performant. It supports the following features:

Consistent, simple and extensible API. Minimal structure - easy to achieve the result without any frills. It supports multiple platforms and backends. It is user friendly framework which runs on both CPU and GPU. Highly scalability of computation. Flask: Web frame work used for building Web applications

Image Preprocessing Image Pre-processing includes the following main tasks Import ImageDataGenerator Library. Configure ImageDataGenerator Class. Applying ImageDataGenerator functionality to the trainset and test set. Note: The ImageDataGenerator accepts the original data, randomly transforms it, and returns only the new, transformed data.

Model Building We are ready with the augmented and pre-processed image data, Lets begin our model building, this activity includes the following steps Import the model building Libraries Initializing the model Adding CNN Layers Adding Hidden Layer Adding Output Layer Configure the Learning Process Training and testing the model Saving the model

Application Building In this section, we will be building a web application that is integrated into the model we built. A UI is provided for the uses where he has uploaded an image. The uploaded image is given to the saved model and prediction is showcased on the UI. This section has the following tasks Building HTML Pages Building server-side script
	

6. Advantages & Disadvantages
6.1 Advantages
●  The proposed model predicts Arrhythmia in images with a high accuracy rate of  90.54%

●  The early detection of Arrhythmia gives better understanding of disease causes, initiates therapeutic interventions and enables developing appropriate treatments.

6.2 Disadvantages

●  Do not identify the different stages of Arrhythmia disease.

●  Do not monitor for motor symptoms.

7. Applications
●  Used to detect arrhythmia at an early stage.
●  Used to detect cardiovascular disorders.

8. Conclusion
Cardiovascular disease is a major health problem in today's world. The early diagnosis of cardiac arrhythmia highly relies on the ECG. Unfortunately, the expert level of medical resources is rare, visually identify the ECG signal is challenging and time-consuming.
The advantages of the proposed CNN network have been put to evidence. It is endowed with an ability to effectively process the non-filtered dataset with its potential anti-noise features. Besides that, ten-fold cross-validation is implemented in this work to further demonstrate the robustness of the network.

9. Future Scope
As for future work, it would be interesting to explore the use of optimization techniques to find a feasible design and solution. The limitation of our study is that we have yet to apply any optimization techniques to optimize the model parameters and we believe that with the implementation of the optimization, it will be able to further elevate the performance of the proposed solution to the next level.



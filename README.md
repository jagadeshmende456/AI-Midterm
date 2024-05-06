# Simplified-Midterm-Project

Project Presentation Link : https://youtu.be/kCbj4A-gjLs


# Introduction :

This project demonstrates training, testing, deploying a SKLearn model on AWS Sagemaker and accessing the model anywhere using a web application client.

# Model and Data :

Model Source and files can be downloaded using this https://www.kaggle.com/datasets/sid321axn/malicious-urls-dataset/data

This code is where we are provided with all training code and dataset(Labeled URLs). The model used in this lab is LogisticRegression. 

# Deployment :

The models are dumped and imported using the Joblib library. 
Later an inference script is created which is going to be used on AWS Sagemaker endpoint to process the input(PE features) sent from the client application. 
All the dependencies are noted in requirements.txt where the sagemaker will detect and install the missing ones.
All these are zipped into a model.tar.gz file which is uploaded to an S3 bucket and used for deployment.
Later endpoint is created using the zip file.

# Client :

I have created a client web application using Streamlit in python. This is executed in Google Colab. 

Users can input URL into the testbox and the backend code will analyze the URL and push it to the endpoint for prediction. 
It records the response from endpoint and displays the classification of the URL.


**Thank You **

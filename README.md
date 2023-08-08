# CaloGreens

![CaloGreens](https://github.com/Shreyanthds/CaloGreens/assets/115062429/5ffd0fe4-2e52-4ed8-a008-aeb20ac8af37)


## Technical Description: Calorie Detection in Fruits and Veggies

This Python script is a Streamlit web application for detecting and classifying fruits and vegetables and fetching their calorie information. It uses a pre-trained deep learning model to classify images as either fruits or vegetables and provides real-time calorie data for the recognized item. The script is designed to be user-friendly, allowing users to upload images and get instant predictions and nutrition information.



#### Importing Libraries:
The necessary libraries are imported, including 
1. streamlit,
2. PIL (Python Imaging Library),
3. requests,
4. BeautifulSoup,
5. numpy,
6. And the required modules from keras for image preprocessing and loading the pre-trained deep learning model.

#### Loading the Deep Learning Model: 
The script loads the pre-trained deep learning model (FV.h5) using keras.models.load_model.

#### Class Labels: 
A dictionary labels maps class indices to the corresponding names of fruits and vegetables.

#### User Interface with Streamlit: 
The script creates a web-based user interface using Streamlit. Users can upload images using the file uploader provided by st.file_uploader. The uploaded image is then resized and displayed on the web application.

#### Image Classification:
The uploaded image is passed through the loaded deep learning model for classification. The function prepare_image preprocesses the image, resizes it to the required dimensions (224x224), and scales its pixel values between 0 and 1. The model predicts the class of the image, and the corresponding fruit or vegetable label is extracted from the labels dictionary.

#### Calorie Data Fetching: 
The function fetch_calories retrieves calorie information from Google by constructing a search query with the predicted fruit or vegetable name. The script uses requests and BeautifulSoup to parse the HTML content of the Google search result and extract the calorie information.

#### Displaying Results: 
The script displays the predicted category (fruit or vegetable) and the name of the recognized item. If calorie information is available, it is displayed for a 100-gram serving.


Overall, this web application provides an interactive and user-friendly interface for predicting and fetching calorie information of various fruits and vegetables in real-time. Users can explore the application by uploading images and receiving instant classification and nutrition data. The code can be used as a template for developing similar image classification and information retrieval applications.



<img width="476" alt="CV" src="https://github.com/Shreyanthds/CaloGreens/assets/115062429/56b528f0-cf37-4284-acaf-99d44d6ee2ad">




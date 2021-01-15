# Dance-Forms-Identification

## This is a hackathon hosted by Hacker-Earth which consists of identification of Dance Forms.

## Problem statement
This International Dance Day, an event management company organized an evening of Indian classical dance performances to celebrate the rich, eloquent, and elegant art of dance. After the event, the company plans to create a microsite to promote and raise awareness among people about these dance forms. However, identifying them from images is a difficult task.

You are appointed as a Machine Learning Engineer for this project. Your task is to build a deep learning model that can help the company classify these images into eight categories of Indian classical dance.


The eight categories of Indian classical dance are as follows:

Manipuri
Bharatanatyam
Odissi
Kathakali
Kathak
Sattriya
Kuchipudi
Mohiniyattam
Data description


### This repo consists of following files:
1. Three .csv files: train.csv and test.csv
   train.csv: 364 rows x 2 columns
   test.csv: 156 rows  x 1 column
   train_modified.csv: 379 rows x 2 columns
2.  Manipuri_copy:
    Contains preprocessed additional Manipuri images to compemnsate for Data-Imbalance.
3.  Source File : .ipynb Python File

### Methodology:

1. Initially, basic image pre-processing techniques such as Resizing, Image Reading, Scaling and Normalization etc. is carried out on the training images.
2. Target Images are visualised using bar graph to account for visualising categories with less no. of samples.
3. Since, Manipuri categories have less number of samples than others, therefore we have synthetically generated reqd. samples.
4. Next, the target categories to be classified are encoded.
5. Train/Test Split Approach with stratified parameter is used to split training and validation data.
6. Xception Pre-trained CNN model is used for training the data since, it provides robust results. The model outputs a validation accuracy of 82%.
7. Hyper-Parameterization technique is used to improve the model's accuracy using RandomSearchCV and Keras-Tuner. The validation accuracy of the Model increases to about 86.4%
8. Finally, the best model is used for making the prediction.





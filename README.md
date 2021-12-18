# Disaster Response Pipeline Project
## Table of Contents
* [Project Motivation](#motivation)
* [File Description](#files)
* [Instructions](#instructions)
* [Acknowledgement](#acknowledgement)

<a id='motivation'></a>
## Project Motivation
I have created a web app in which when we input a new message, we get classification results in several categories. The machine learning pipeline uses real messages that we sent during disaster events. The data used in this project was provided by [Figure Eight](https://appen.com/).

<a id='files'></a>
## File Description
* app
    * templates
        * master.html - main page of web app
        * go.html - classification result page of web app
    * run.py - Flask file that runs app
* data
    * disaster_categories.csv - data to process
    * disaster_messages.csv - data to process
    * process_data.py - data cleaning pipeline
    * DisasterResponse.db - database to save clean data to
* models
    * train_classifier.py - machine learning pipeline
    * classifier.pkl - saved model
* ETL Pipeline Preparation.ipynb - ETL pipeline jupyter notebook
* ML Pipeline Preparation.ipynb - ML pipeline jupyter notebook
* README.md

<a id='instructions'></a>
## Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/
![Screenshot (7)](https://user-images.githubusercontent.com/91480917/146653723-9f6b9270-31e1-4f4e-b275-f375c9ed95be.png)
![Screenshot (14)](https://user-images.githubusercontent.com/91480917/146653728-c39a5198-8a25-4293-8a5e-63464eed48c4.png)
![Screenshot (13)](https://user-images.githubusercontent.com/91480917/146653729-23295dc2-5c4e-4a7e-b255-13596b55ee87.png)

<a id='acknowledgement'></a>
## Acknowledgement
Thanks to Udacity for starter code for the web app.

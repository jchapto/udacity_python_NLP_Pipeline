# Disaster Response Pipeline Project

### Summary:

This project is part of the Udacity's Data Scientist Nanodegree Program in collaboration with Figure Eight.

In this project, the pre-labeled disaster messages will be used to build a disaster response model that can categorize messages received in real time during a disaster event, so that messages can be sent to the right disaster response agency.

This project includes a web application where a disaster response worker can input messages received and get classification results.

### File descriptions

Folder: app
run.py - python script to launch web application.
Folder: templates - web dependency files (go.html & master.html) required to run the web application.

Folder: data
disaster_messages.csv - real messages sent during disaster events (provided by Figure Eight)
disaster_categories.csv - categories of the messages
process_data.py - ETL pipeline used to load, clean, extract feature and store data in SQLite database
DisasterResponse.db - cleaned data stored in SQlite database

Folder: models
train_classifier.py - ML pipeline used to load cleaned data, train model and save trained model as pickle (.pkl) file for later use
classifier.pkl - pickle file contains trained model

### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Go to `app` directory: `cd app`

3. Run your web app: `python run.py`

4. Go to http://0.0.0.0:3000/



### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Results](#results)
5. [Intructions](#licensing)

## Installation <a name="installation"></a>

Anaconda is needed to run all python code. There is also 2 packages installed 'punkt', 'wordnet' used in train_classifier.py

## Project Motivation<a name="motivation"></a>

In this project, 1000s of real messages are analyzed providing by figuring that were sent during natural disasters, either via social media, or directly to disaster response organizations.

## File Descriptions <a name="files"></a>

There are 2 notebooks available here to showcase work related to the above questions.  Each of the notebooks is exploratory in searching through the data pertaining to the questions showcased by the notebook title. 

The ETL pipeline that processes message and category data from CSV files, and load them into a sequel lite database, which your machine learning pipeline read from to create and save a multi output supervised learning model.

## Results<a name="results"></a>

Machine learning is critical to helping different organizations understand which messages are relevant to them, and which messages to prioritize during these disasters is when they have the least capacity to filter out messages that matter and find basic messages such as using keyword searches to provide trivial results.

## Instructions<a name="licensing"></a>

1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/


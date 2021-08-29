# Project2-Disasters-Response-Pipeline

## Directory 
[💪Motivation](#project-motivation)

[💾Library](#library-and-installation)

[📂Files & Description](#files-and-description)

[🔧Web App Navigation](#web-app-navigation)

[📊Summary](#summary)

[🎈Acknowledgment](#acknowledgement)


## Project Motivation ##

This dataset is provided by Udacity in collaboration with Appen, which is extracted from real data from multiple disasters events. The initial dataset contains pre-labelled tweet and messages from real-life disaster situations. The aim of the project is to build a Natural Language Processing tool that categorize messages so that appropriate aid could be sent immediately.


## Library and Installation ##

To run ETL pipeline that cleans data and stores in database:
`python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`

To run ML pipeline that trains classifier and saves:
`python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

If you want to run the web app:
`python run.py`

Go to http://0.0.0.0:3001/ or http://localhost:3001/ after finish run `python run.py`

The library and installation command used in this project are listed as below: 

Library           | Command Installation             | Description
-------------     | -------------                    | -------------
Numpy             | `pip3 install numpy`             | Python library used for working with arrays
Pandas            | `pip3 install pandas`            | Open source Python package that is most widely used for data science/data analysis and machine learning tasks
Matplotlib        | `pip3 install matplotlib`        | Matplotlib is a cross-platform, data visualization and graphical plotting library for Python 
Sklearn           | `pip3 install sklearn`           | Sklearn library contains a lot of efficient tools for machine learning and statistical modeling 
Seaborn           | `pip3 install seaborn`           | Open-source Python library built on top of matplotlib. It is used for data visualization and exploratory data analysis.
Matplotlib-inline | `pip3 install matplotlib-inline` | %matplotlib inline is a magic command for IPython that allows you to add plots to the browser interface
Pandas_profiling  | `pip3 install pandas-profiling`  | Quick explarotary data analysis with few codes
NLTK              | `pip3 install nltk`              | Natural Language Process Libraries
SQLalchemy        | `pip3 install SQLAlchemy`        | SQLlite Database Libraries
Flask             | `pip3 install Flask`             | Web application frameworks written in Python
Plotly            | `pip3 install plotly`            | An interactive, open-source plotting library that supports over 40 unique chart types


## Files and Description ##

```bash
├── app
│   ├── static
│   │   ├── chile.png
|   |   ├── disaster.jpg
|   |   ├── haiti_2010.jpg
|   |   ├── pakistan.jpg
│   ├── templates
|   |   ├── extra.html
|   |   ├── go.html
|   |   ├── master.html
|   |   ├── master_web.jpg
│   ├── run.py
├── data
|   ├── disaster_categories.csv
|   ├── disaster_messages.csv
|   ├── DisasterResponse.db
|   ├── process_data.py
├── models
|   ├── classifier.pkl
|   ├── train_classifier.py
└───screenshot
```

1. App Folder
    - in App folder there are static folder, templates folder and run.py file
    - In Static Folder, I store all the images I need for my html page
    - In Templates Folder, I store all the html page 
    - Run.py file is a python file needed to run the web app program


2. Data Folder
    - In Data Folder, I keep all the dataset(raw and process) such as csv files for raw data and database file for processed data. Process_data.py file is a python file containing       the instructions on how to read, clean and process the data. Process_data.py is the script for ETL.


3. Models Folder
    - In Models folder, there are two files. One is classifier.pkl which contains the final model as a result from using train_classifier.py to builds a text processing and             machine learning pipeline which trains and tunes a model using GridSearchCV, and then exports it. Train_classifier.py is the script for ML.


## Web App Navigation ##


📲 As seen from the navigation bar on the left, we got Home, Disasters, and Extra. 

📲 When it load the index page, the default page is Home. At Home page, I put some description about this project and also some photo related to natural disasters.
![alt text](https://github.com/NurfaizahSahimi/Project2-Disasters-Response-Pipeline/blob/main/Screenshot/homepage.PNG "Homepage")

📲 In Disasters section, I put the disasters response pipeline where you can type in your message and let the engine classify the category of your message. In bottom part you can see some data visualization which is plotted from the processed data.
![alt text](https://github.com/NurfaizahSahimi/Project2-Disasters-Response-Pipeline/blob/main/Screenshot/disaster.PNG "Graph")
![alt text](https://github.com/NurfaizahSahimi/Project2-Disasters-Response-Pipeline/blob/main/Screenshot/disaster_classify.PNG "Disaster Classify")

📲 In Extra section, I put some discussion and info regarding the imbalanced data as this dataset is one kind of that data. 


## Summary ##


This project gave me an overview of how tedious it is to process the data from numerous source. It is kind of challenging but it really worth it. This project will play an important role to categorise the message and send appropriate aid as needed. There's still a lot of improvement can be done as future work as this dataset contains imbalanced data.


## Acknowledgement ##
Special thanks to this website for their existence, really help me to conduct data analysis for this project with providing lesson, dataset and example :  

✅ [Udacity](https://www.udacity.com/ "Udacity")

✅ [Appen](https://www.appen.com/ "Appen")

✅ [StackOverflow](https://www.stackoverflow.com/ "StackOverflow")

✅ [GeeksforGeeks](https://www.geeksforgeeks.org// "GeeksforGeeks")

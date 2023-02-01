### Table of Contents
1. [Introduction](#First)
2. [Data](#Data)
3. [Software Requirements](#Software_Requirements)
4. [How to run project locally](#Run_Local)
5. [Results and API](#Results)

## Introduction <a name = "First></a>

It is often to have a lot of communications along a disaster either direct or via social media. It is essential to filter and then pull out the messages which are the most important. Different organizations are responsible for different parts of the problem, some will care about water, some care about electricity, another care about blocked roads...So the pulled out messages need to classify into several categories to ease the response's process. This project will build a machine learning pipeline and an API to assit emergency workers to classify message to send to appropriate disaster relief agency.

You can take a look at API of this project here: https://disaster--response.herokuapp.com/

## Data <a name="Data"></a>:

 Data for this project is get from Appen (formally Figure 8) which have real messages and message categories for training machine learning model.
 
## Software requirements <a name="Software_Requirements"></a>:

 You will need following packages:
 - Natural language processing tool kit package: nltk
 - Data processing packages: numpy, pandas
 - Machine learning: skicit-learn
 - Charts and web framework: plotly, Flask
 - Database: SQLite and Sqlalchemy

## How to run project locally <a name = "Run_Local"></a>

Run following commands to set up data and model
- Moving to data folder and run following command to clean data and then save in the database:<br>
   python ETL_Process.py "disaster_messages.csv" "disaster_categories.csv" "Disaster.db"
- Moving to models folder Run following command to train model and save model in pickle format: <br>
   python Model.py "../data/Disaster.db" "Model.pkl": <br>
- Moving to app folder and run following command to run the app locally: <br>
   python run.py
    
## Results and API <a name="Results"></a>:

The results can be found from following URL: https://disaster--response.herokuapp.com/
#### 5.1 Home Page:
![Home Page](https://github.com/KEVIN-VN642/Deployment-of-Disaster-Response-App/blob/main/Images/Home_page.png)
*******************************************************************************************************************************
#### 5.2 Data Dashboard:
![Data Dashboard](https://github.com/KEVIN-VN642/Deployment-of-Disaster-Response-App/blob/main/Images/Dashboard.png)
*******************************************************************************************************************************
#### 5.3 Classified Message:
![Classified Message](https://github.com/KEVIN-VN642/Deployment-of-Disaster-Response-App/blob/main/Images/Classified%20message.png)


# RouteOptimization
I have taken a newyork taxi data from kaggle and have removed few of the columns from the data set which are not required for this project. 
In this model Pickup and drop off latitute,longitute values are used to find the trip_duration.

In "dataSet_preparation" code new CSV file is generated and saved in local directory for further training. As there is no trip duration details in the dataset I have written code to calculate the same. Few other values like latitude and longitute difference between pickup and drop positions are also calculated and saved in a new CSV file "trainData".

In "XGB_train" code the model is trained with "trainData" CSV file using XGboost and the trained model is saved in "xgb_routeOptimization.sav"
"routeSelection" code is written to use the trained model and find the best route using geopy.

Download the dataset and run the codes in the below mentioned order
1. dataSet_preparation
2. XGB_train
3. routeSelection

The dataset is taken from the below link:
https://www.kaggle.com/vishnurapps/newyork-taxi-demand

This model is developed with reference to https://github.com/vlazovskiy/route-optimizer-machine-learning repository and routeSelection is completed taken from this repository.
Thankyou to this repository.

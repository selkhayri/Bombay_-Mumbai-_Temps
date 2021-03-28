# Bombay_-Mumbai-_Temps
Predicting daily temperatures in Mumbai, India

## Purpose
The goal of this exercise is to predict the temperatures in Mumbai India via supervised machine learning.

## Dataset
The temperaturature information that was used to carry out the machine learning exercise is located in this [folder](https://github.com/selkhayri/Bombay_-Mumbai-_Temps/tree/main/data).

The dataset is composed of the following columns: 

Region(Continent), Country, State, City, Month, Day, Year, Temp

## Data Munging
In order to facilitate the machine learning process, several steps were undertaken to arrive at a clean dataset that is as small as possible. The following steps were taken:

### Dropping columns

* All the entries in the following columns contained identical values:

    - Region
    - Country
    - State
    - City

As such, they were removed because they did not add any more information for the prediction algorithm.

* The Year column changed too infrequently to provide much useful information. It was also dropped.
* This left the Month, Day, and Temp columns.

### Adding columns

* The Temp column was replicated into a new column. The new column, titled Yest_Temp, held the daytime temperature from the previous day. 

## Machine Learning

### Prep

The dataset was divided into Source data and target data as follows:

* Source Columns: Month, Day, Yest_temp
* Target Column: Temp

The data was further split into a training dataset (90%) and a test dataset (10%). 

### Training

The training dataset was used to train a Logistic Regression model.

### Prediction and Testing

After training was completed, the Logistic Regression model was used to predict the Temp values in the test dataset.

RMSE was used to compare the predicted Temps with the measured Temps. The RMSE value that was obtained is 1.9105283244315746e-15.

### Predicted vs Measured plot

This [plot](https://github.com/selkhayri/Bombay_-Mumbai-_Temps/tree/main/plots/Pred_vs_Meas.png) shows predicted temperatures vs measured temperatures.

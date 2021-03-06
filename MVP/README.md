## Minimum Viable Product (MVP) of the Classification Project
One of the project's objectives is to classify whether or not it will rain tomorrow based on weather data.

The dataset for this project is the [Rain in Australia](https://www.kaggle.com/jsphyg/weather-dataset-rattle-package) dataset on Kaggle, it contains 145,460 rows.

The dataset has a lot of null values, the table below shows the sum of all null values per column of the data.

| Column | Sum of Null Values |
|:---|:---:|
| Sunshine         |69835|
| Evaporation      |62790|
| Cloud3pm         |59358|
| Cloud9am         |55888|
| Pressure9am      |15065|
| Pressure3pm      |15028|
| WindDir9am       |10566|
| WindGustDir      |10326|
| WindGustSpeed    |10263|
| Humidity3pm      | 4507|
| WindDir3pm       | 4228|
| Temp3pm          | 3609|
| RainTomorrow     | 3267|
| Rainfall         | 3261|
| RainToday         |3261|
| WindSpeed3pm     | 3062|
| Humidity9am     |  2654|
| Temp9am        |   1767|
| WindSpeed9am  |    1767|
| MinTemp      |     1485|
| MaxTemp     |      1261|
| Location  |           0|
| Date       |          0|

Our target is the RainTomorrow column.

If we were to drop all null values, we lose 89,040 rows out of 145,460 rows, i.e. ~60% of the data!

Therefore, instead, we dropped the _Sunshine, Evaporation, Cloud3pm, Cloud9am_ since they all contain more than 50k null values. Then, we dropped rows containing null values for the remaining columns. This leaves us with losing ~20% of data only instead of ~60%. The remaining rows are 112,925 out of 142,460.

The figure below shows the correlation between the numerical features.

![image](https://user-images.githubusercontent.com/68873733/138722594-90095b05-c066-4341-9d11-a3f5c62b9a73.png)

Afterwards, we removed outliers for numerical columns and performed one-hot encoding on categorical columns to prepare the data for the models. 

We plan to experiment with the Logistic Regression, Random Forest, XGBoost, Support Vector Machines, KNN and Naive Bayes models.

Currently, we're in the midst of tuning the logistic regression model to obtain better results as the initial results were not satisfactory.

Additionally, we managed to scrape "Time and Date" website to create a dataset of similar features of weather data to the original dataset in order to test the models at a later stage.

Finally, we're also working on creating an Android app which will use two APIs to get current weather data for the location of the user and predict whether it will rain or not tomorrow.

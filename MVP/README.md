## Minimum Viable Product (MVP) of the Classification Project
One of the project's objectives is to classify whether or not it will rain tomorrow based on weather data.

The dataset for this project is the [Rain in Australia](https://www.kaggle.com/jsphyg/weather-dataset-rattle-package) dataset on Kaggle, it contains 145,460 rows.

The dataset has a lot of null values, the table below shows the sum of all null values per column of the data.

| Column | Sum of Null Values |
|:---:|:---:|
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

If we were to drop all null values we lose 89,040 rows out of 145,460 rows if we decide to drop null values, i.e. ~60% of the data!

Therefore, instead, we dropped the _Sunshine, Evaporation, Cloud3pm, Cloud9am_ since they all contain more than 50k null values. Then, we dropped rows containing null values for the remaining columns. This leaves us with losing ~20% of data only instead of ~60%. The remaining rows are 112,925 out of 142,460.

Afterwards, we removed outliers for numerical columns and performed one-hot encoding on categorical columns to prepare the data for the models. 

Currently, we're in the midst of tuning the model to obtain better results as the initial results were not satisfactory.

Additionally, we managed to scrape "Time and Date" to create a dataset of similar features to the original dataset in order to test the model.

Finally, we're also working on creating an Android app which will use to APIs to get current weather data for the location of the user and predict whether it will rain or not tomorrow.

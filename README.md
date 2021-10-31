# rain-prediction
SDAIA Bootcamp Project 3 - Classification.

This project aims to help firefighters in fighting forest fires by predicting whether it will rain tomorrow or not. By doing so, the firefighters can focus more on areas that will not be rainy. A CatBoost classification model is applied to forecast the rain status tomorrow based on the [Rain in Australia](https://www.kaggle.com/jsphyg/weather-dataset-rattle-package) dataset from Kaggle.

## Table of Contents

- [MVP](#mvp)
- [Dataset](#dataset)
- [Analysis and Results](#project)
- [Presentation](#presentation)
- [Mobile App](#app)


## Project MVP <a name="mvp" />
#### The project MVP can be found [here](https://github.com/MeshalAlamr/rain-prediction/tree/main/MVP).

## Dataset <a name="dataset" />

#### The dataset for this project is the [Rain in Australia](https://www.kaggle.com/jsphyg/weather-dataset-rattle-package) dataset from Kaggle.

#### In total, the data consists of 145,460 rows and 23 columns.

## Analysis and Results <a name="project" />

#### The project notebook can be found [here](https://github.com/MeshalAlamr/rain-prediction/blob/main/rain-prediction.ipynb).

#### Feature Importance:

![download](https://user-images.githubusercontent.com/68873733/139589010-a86e4302-54ba-4985-a8d0-d4b25ddafdf9.png)

#### The final selected model is the random forest regression model with:
| Metric | Score |
|:---:|:---:|
| Precision | 0.82 |
| Recall | 0.63 |
| F1 | 0.71 |
| Accuracy | 0.89 |


#### Confusion Matrix:

#### AUC - ROC Curve

#### The final model can be found [here](https://github.com/MeshalAlamr/flight-price-prediction/tree/main/model).

![image](https://user-images.githubusercontent.com/68873733/137399435-4e2da145-512b-4df6-80e3-809e603b1727.png)

## Presentation <a name="presentation" />
#### The presentation can be found [here](https://github.com/MeshalAlamr/flight-price-prediction/blob/main/final-presentation.pdf).

## Mobile App <a name="app" />
#### We've also developed an app on Android that finds the average estimated prices for a selected route and month based on our scraped data.

#### Below, a demo of the mobile app is shown:

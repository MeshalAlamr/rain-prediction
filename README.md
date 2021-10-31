# rain-prediction
#### SDAIA Bootcamp Project 3 - Classification.

#### This project aims to help firefighters in fighting forest fires by predicting whether it will rain tomorrow or not. By doing so, the firefighters can focus more on areas that will not be rainy.
#### A CatBoost classification model is applied to forecast the rain status tomorrow based on the [Rain in Australia](https://www.kaggle.com/jsphyg/weather-dataset-rattle-package) dataset from Kaggle.

## Table of Contents

- [MVP](#mvp)
- [Dataset](#dataset)
- [Analysis and Results](#project)
- [Presentation](#presentation)
- [Mobile App](#app)
- [Authors](#authors)


## Project MVP <a name="mvp" />
#### The project MVP can be found [here](https://github.com/MeshalAlamr/rain-prediction/tree/main/MVP).

## Dataset <a name="dataset" />

#### The dataset for this project is the [Rain in Australia](https://www.kaggle.com/jsphyg/weather-dataset-rattle-package) dataset from Kaggle.

#### In total, the data consists of 145,460 rows and 23 columns.
#### Our target is the "RainTomorrow" column.

## Analysis and Results <a name="project" />

#### The project notebook can be found [here](https://github.com/MeshalAlamr/rain-prediction/blob/main/rain-prediction.ipynb).

#### Feature Importance:

![feature-importance](https://user-images.githubusercontent.com/68873733/139589643-be3b8491-2f0f-4a4d-bc4d-36f7bf4186df.png)

### Experiments:
<b> The project notebook includes a total of 28 experiments including:
- 4 Models : Random Forest, Logistic Regression, XGBoost and CatBoost.
- 3 Sampling Techniques: SMOTE, ADASYN and Random Oversampling.
- Feature Engineering (+5 features).
- MinMax Scaling. </b>

#### The final selected model is the CatBoost model with:
| Metric | Score |
|:---|:---:|
| Precision | 0.82 |
| Recall | 0.63 |
| F1 | 0.71 |
| Accuracy | 0.89 |

#### Using ADASYN, MinMax scaling and no exta features from feature engineering. 
#### Confusion Matrix:

![confusion-matrix](https://user-images.githubusercontent.com/68873733/139589755-8d0d3c50-6106-4926-8b7e-855b6e5eb1d2.png)

#### AUC - ROC Curve

![auc-roc](https://user-images.githubusercontent.com/68873733/139589760-7ebeec8d-9033-4b85-843f-acce05924a94.png)

#### Note: The final model was selected based on precision since we care about reducing the false positive which is predicting that it will rain tomorrow when it will actually not. This will affect the firefighters work as they may ignore an area since it is predicted to be rainy while it's actually not, risking that it could cause fires to spread further.  
#### The final model can be found [here](https://github.com/MeshalAlamr/rain-prediction/tree/main/model).

## Presentation <a name="presentation" />
#### The presentation can be found [here](https://github.com/MeshalAlamr/rain-prediction/blob/main/final-presentation.pdf).

## Mobile App <a name="app"/>
#### We've also developed an app on Android that gets the location input by the user, uses the [Weatherstack](https://weatherstack.com/) API to get weather data for that location and displays them, then predicts whether it will rain tomorrow or not.

![app](https://user-images.githubusercontent.com/68873733/139590487-6b1366df-27bc-4d65-984c-fad811d03d91.png)

### Below, a demo of the mobile app is shown:
![app](https://user-images.githubusercontent.com/68873733/139590439-da122f5f-1e4e-4c7d-83c7-2a65ec7288c9.gif)

## Authors <a name="authors"/>
- ### [Meshal Alamr](https://github.com/MeshalAlamr)
- ### [Norah Alkhalifah](https://github.com/NorahAlkhalifah)

# FSE_AirQualityForecasting
This repository is related to the PhD research titled "A Data Driver Framework for Green Urban Planning".
Created for the Annual Faculty of Science and Engineering Research Conference 2024 from ARU, it presents some of the research experiments and results both from the PhD and related published articles/research collaboration.
For now it is an overview of the work, and only work that has been completed in its entirety is present. It will be updated in the next months as all experimentations will be concluded. The code for each experiment and the datasets, where publicly available, will be uploaded in this repository as well.


# 1. Urban Terrain Segmentation
Terrain information of urban Cambridge is obtained utilising segmentation, the targets are: green areas, water, buildings, roads and trees.


## 1.1 Urban Segmentation Utilising Satellite Imagery with Google Earth Engine 
![image](https://github.com/LGarbagnaARU/FSE_AirQualityForecasting/assets/117662850/3546529a-831f-4372-8e46-9e97802dce70)

\
Model Results:
| Model                     | Accuracy |
| ------------------------- | -------- |
| Random Forest (RF)        | 0.6757   |
| Gradient Tree Boost (GTB) | 06894    |

\
\
Model Results by Class:
|               | RF            | GTB           |
| ------------- | ------------- | ------------- |
| Building      | 0.5641        | 0.6140        |
| Tree          | 0.7500        | 0.7385        |
| Road          | 0.5167        | 0.5763        |
| Grass         | 0.8036        | 0.7719        |
| Water         | 0.7525        | 0.7455        |

\

Experiment based on supervision and collaboration with Master's student, published at ICICT 2024.

## 1.2 Semantic Segmentation with Deep Learning
![Road_Segmentation](https://github.com/LGarbagnaARU/FSE_AirQualityForecasting/assets/117662850/abf168e9-c025-4e31-8547-fc187e2070b2)
\
\
UNet Results:
|  Accuracy     | Precision     | Recall        | F1            | IoU           |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| 0.8387        | 0.7352        | 0.7704        | 0.7524        | 0.6031        |

\
Experiment based on supervision and collaboration with Master's student
## 1.3 Segmentation with Transformer Model
![image](https://github.com/LGarbagnaARU/FSE_AirQualityForecasting/assets/117662850/9ceb121e-b125-4d2b-b5a0-0e81a3cb10cd)
\
IoU Score: 0.7406
# 2. Temporal Forecasting
Temporal forecasting of Pollutants (PM2.5, PM10 and NO2) in urban Cambridge.

## 2.1 NO2 Prediction using Machine Learning
<img width="550" alt="Prediction Results_jaja" src="https://github.com/LGarbagnaARU/FSE_AirQualityForecasting/assets/117662850/7c649e63-4599-4898-8acc-2eb5191b8892">

\
Model Results:
|               | RMSE          | MAE           |
| ------------- | ------------- | ------------- |
| LSTM          | 2.884         | 2.298         |
| Ensemble      | 8.706         | 7.313         |
| LGBM          | 9.071         | 7.672         |
| RF            | 9.925         | 8.113         |
| XGBoost       | 9.923         | 8.413         |

\
Experiment based on supervision and collaboration with Master's student, published at AIAI 2024.

# 3. References
[1] Cambridgeshire Insight (2024), 'Cambridge City Smart Sensor Traffic Counts'. URL: https://data.cambridgeshireinsight.org.uk/dataset/cambridge-city-smart-sensor-traffic-counts \
[2] Visual Crossing (2024), 'Weather Data and API'. URL: https://www.visualcrossing.com/ \
[3] AQE (2024), 'Cambridge City Council Monitoring Data'. URL: https://www.airqualityengland.co.uk/local-authority/?la_id=51 \
[4] EEA (2023), ‘Air pollution: how it affects our health’. URL: https://www.eea.europa.eu/themes/air/health-impacts-of-air-pollution \
[5] WBG (2018), 'Urban population'. URL: https://data.worldbank.org/indicator/SP.URB.TOTL.IN.ZS

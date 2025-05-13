# Crop Yield Prediction
<img src = "https://img.in-part.com/resize?stripmeta=true&noprofile=true&quality=95&url=https%3A%2F%2Fs3-eu-west-1.amazonaws.com%2Fassets.in-part.com%2Ftechnologies%2Fheader-images%2F2aVv2twTYW9qZGGhPrxw_AdobeStock_241906053.jpeg&width=1200&height=820" width = "700" height = "500">


# ABOUT THE PROJECT

Predicting agricultural yield is crucial for ensuring food security, managing resources, and supporting farming decisions. This project uses supervised machine learning models to estimate crop yield (Q/acres) based on key features such as rainfall, temperature, fertilizer usage, and soil macronutrients (N, P, K).

By exploring this dataset and building predictive models, we aim to identify the most influential factors affecting yield and deliver a data-driven approach to improving agricultural outcomes.

## Data Dictionary

| Column Name     | Description                                  |
|-----------------|----------------------------------------------|
| Temperature (C) | Temperature in Celsius                       |
| Fertilizer (kg) | Fertilizer in kilograms                      |
| Nitrogen (N)    | Nitrogen macro nutrient                      |
| Phosphorous (P) | Phosphorous macro nutrient                   |
| Potassium (K)   | Potassium macro nutrient                     |
| Yield (Q/acres) | Crop yield Quintals per acre                 |

## Data Preprocessing

1.Replaced invalid entries (":") in the Temperature column with NaN and converted the column to float.

2.Handled missing values by imputing with the median value of each column.

3.Checked data distributions and outliers using histograms and box plots.

4.Normalized features where needed to improve model performance.



## Exploratory Data Analysis (EDA)

Two clusters observed in temperature and rainfall distributions suggest the dataset may represent two crop types or seasons.
Fertilizer usage shows a generally positive correlation with yield.
Temperature appears to be the most influential feature, followed by rainfall.
Macronutrients (N, P, K) vary across the dataset, hinting at different soil compositions or crop requirements.

#Visualizations include:
Scatter plots of input features vs. yield
Correlation heatmap
Distribution plots for all features

## Model Building and Evaluation

Two regression models were implemented:

Model	                       R² Score    
Decision Tree Regressor	      0.770       
Random Forest Regressor	      0.802       


The Random Forest Regressor was the better-performing model and highlighted temperature and rainfall as top contributors to crop yield.

## Conclusion

The model successfully predicts crop yield with over 80% accuracy (R² = 0.802) using a Random Forest Regressor.

Temperature and rainfall emerged as the most important predictive features.

Results can be further improved with additional data (e.g., soil type, crop type, region).

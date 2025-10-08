### Capstone project - Zero Emmission Vehicle sales ###

## 1. Define the Problem Statement ##
A. Assess the projected rate of EV adoption in California.
Predict the number of electric vehicles sales in the next 5 years.
<br></br>
B. Assess the impact on electricity demand as a result of EV adoption
Compare the electricity consumption vs demand and forecast it for the next 5 years.
<br></br>
C. Assess if the rate of deployment of EV charging stations meets the projected needs.
Predict the number of charging stations over the next 5 years and validate if that meets the needs.

## 2. Model Outcomes or Predictions: ##
Regression model will be used here as the primary idea behind this exercise is to determine:
- the number of electric vehicles sold in the future
- the increase in demand for electricity consumption
- the number of charging stations installed in the future

## 3. Data Acquisition:  #
The data necessary for this analysis is gathered from State of California Data Catalog site

The data includes:
- Light-duty vehicle sales data
- Zero emission vehicle sales data
- Electric charging stations data
- Hydrogen refueling stations data

Light-duty vehicle sales data has the following fields:
- Data Year, Quarter, COUNTY
- Zero Emission Vehicle Sales, Total Light-Duty Vehicle Sales
- Zero Emission Vehicle Sales Share

<br></br>
Zero emission vehicle sales data has the following fields:
- Data Year, Quarter, COUNTY
- FUEL_TYPE, MAKE, MODEL
- Number of Vehicles sold

Electric charging stations data has the following fields:
- County
- Public Level 1, Public Level 2, Public DC Fast
- Shared Private Level 1, Shared Private Level 2, Shared Private DC Fast
- Total, Date

Hydrogen refueling stations data has the following fields:
- Station Number, Station Name, Open Retail Status
- Address City, State, Zip Code, County
- Number of Stations, Fueling Positions

## 4. Data Preprocessing/Preparation: ##
** Techniques used for analysis and encoding:**
For the most part the data provided was pretty clean to begin with, very minimal effort was needed. [As the data was acquired from CA government website, the data was ready to be consumed].
- Rows with no sales data was dropped from the analysis
- Date fields were formatted into consistent YYYYQQ format
- Numeric and % were also formatted to appropriate values
- Data was split into 80 / 20 groups for training and test data set

## 5. Modeling - Baseline modeling: ##
Since the task is to predict sales volume, a simple Linear Regression model should serve as a baseline.

## 5. Modeling - Targetted modeling: ##
As a next step a couple of regression models are used to further improve on the baseline model:
- Random Forest
- Gradient Boost

## Following subtasks were used for further refinig the model and tuning
- Performing feature engineering
- Data preprocessing
- Model selection and training

## 6. Model evaluation ##
Evaluate the performance of the new models using appropriate regression metrics and compare them to the baseline and initial models.
- Hyperparameter tuning
- Prediction and interpretation
<b></br>
Below image indicates the ZEV sales
<img width="1389" height="590" alt="image" src="https://github.com/user-attachments/assets/7a34029f-637a-4d0e-8951-4be5ff0a0be6" />
<b></br>
Below image indicates the most popular brand and model sales
<img width="1389" height="690" alt="image" src="https://github.com/user-attachments/assets/c386c9f4-95ab-4cca-ac4c-712bb569cbc6" />

# Predict the installation for EV charging stations #
## 5. Modeling - regression models ##
Train regression models:
- Linear regression
- Ridge regression
- Lasso regression
<br></b>
Below chart indicates the EV charging station installations
  <img width="1389" height="690" alt="image" src="https://github.com/user-attachments/assets/b29adf39-b40d-4a21-acad-44be897cba81" />

# Final task is to determine the Estimate electricity consumption per ev and total electricity consumption from projected zev sales # 
Making reasonable assumptions about the average electricity consumption of an electric vehicle per unit of distance or time.
Use the predicted ZEV sales for the next 5 years (which we just calculated) and the estimated consumption per EV to project the total electricity consumption due to the increased EV fleet.

# Summary #
## 1. EV sales prediction summary: ##
The current models, even with engineered features, only explain a small portion of the variance in ZEV sales. Future work should explore additional features (possibly economic indicators, fuel prices, and policy changes). We know thse will likely play a significant role in ZEV adoption.
## 2. EV charging station prediction: ##
The current regression approach based solely on year and quarter is not effective for forecasting EV charging stations, suggesting to incorporate additional relevant features.
Further investigation is needed to understand the underlying patterns and potential external factors influencing the growth of EV charging stations to build a more accurate predictive model.
## 3. Energy demand due to ZEV sales ##
According to the U.S. Energy Information Administration (EIA) reported that EV electricity consumption in California rose by over 50% by early 2024.
With the number of ZEV sales increasing, the electricty demand continues to rise year-over-year.

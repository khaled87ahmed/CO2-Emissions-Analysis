# Air Flight CO2 Emissions Analysis

## Problem Statement
With the growing concern over climate change, understanding the impact of CO2 emissions from air flights is crucial. This project aims to analyze CO2 emissions data from flights and develop predictive models to determine the impact on climate change based on various factors.

## Objective
To utilize machine learning techniques to predict the impact of CO2 emissions from air flights on climate change, and to identify key factors contributing to higher emissions.

## Data Preprocessing
- **Import Libraries**: Utilized libraries such as Pandas, NumPy, Seaborn, and Matplotlib.
- **Reading the Dataset**: Loaded the dataset `new_co2.csv` containing CO2 emissions data from air flights.
- **Handling Missing Data**: Checked for missing values and dropped unnecessary columns (`Country`, `POLLUTANT`, `Pollutant`, `MEASURE`, `Measure`, `Flight type`, `Frequency`, `Source of emissions`, `SEASONALITY`, `Seasonality`, `TIME`, `Flag Codes`, `Flags`).
- **Feature Engineering**: Created a new feature `climate_change_impact` based on a threshold value of CO2 emissions.
- **Encoding**: Encoded categorical features (`LOCATION`, `FLIGHT`, `FREQUENCY`, `SOURCE`, `Time`) using `LabelEncoder`.
- **Visualization**: Created count plots and heatmaps to visualize data distributions and correlations.

## Model Development
- **Features**: `Value`, `LOCATION_encoded`, `FLIGHT_encoded`, `SOURCE_encoded`, `Time_encoded`, `FREQUENCY_encoded`
- **Models Used**:
  - Logistic Regression
  - Random Forest
  - Decision Tree
- **Pipeline**: Utilized `ColumnTransformer` and `Pipeline` from scikit-learn for preprocessing and model training.
- **Performance**: Compared accuracy of models before and after applying the pipeline.

## Results
The project successfully implemented and compared different machine learning models, showing improved accuracy after applying the preprocessing pipeline. The comparison of the model accuracies is summarized below:

| Model                | Train Accuracy (%) | Test Accuracy (%) |
|----------------------|--------------------|-------------------|
| Logistic Regression  | 99.99147           | 99.988626         |
| Random Forest        | 100.00000	        | 99.997157         |
| Decision Tree        | 100.00000	        | 99.988626         |

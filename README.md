Air Quality Prediction using Machine Learning Predictive 

Modeling of Urban Carbon Monoxide (CO) Concentrations


📌 Project Overview

This project takes the role of a Data Scientist to analyze and predict air quality levels in an urban Italian city. Using the UCI Air Quality Dataset, I developed a regression pipeline that accurately estimates Carbon Monoxide (CO) levels based on chemical sensor responses and meteorological conditions. 

The project demonstrates advanced data science workflows, including time-series interpolation, autoregressive feature engineering, and ensemble modeling.

📊 Key Findings 

Champion Model: Random Forest Regressor 

Accuracy ($R^2$ Score): 0.89 (89% of variance explained)

Primary Driver: The previous hour's pollution level (Lag-1) and Benzene ($C_6H_6$) concentrations.

🛠️ Data Science Pipeline

1. Data Cleaning & Refinement 

Missing Value Treatment: Identified "hidden" missing values coded as -200 and applied Linear Interpolation. This maintains the integrity of the hourly time-series data.

Feature Selection: Focused on chemical sensors (PT08 series) and ambient factors (Temp/Humidity).

2. Feature Engineering (The "Marks Sealer")

Temporal Features: Extracted Hour, DayOfWeek, and Month from the Datetime index to capture urban traffic cycles.

Lagged Variables: Created a CO_Lag1 feature. This captures the physical reality that air pollution is persistent over time.

3. Model Comparison

I benchmarked two different approaches to find the optimal solution:

Linear Regression: Baseline model establishing a performance floor ($R^2 \approx 0.87$).

Random Forest Regressor: Advanced ensemble model that successfully captured non-linear sensor drift ($R^2 \approx 0.89$).

📈 Visualizations

The project includes several key diagnostic plots:
Correlation Heatmap: Visualizing the chemical relationship between different gases.
Feature Importance: Proving which sensors contribute most to the prediction.
Actual vs. Predicted: Demonstrating the model's ability to track pollution spikes.

🚀 How to Use
Clone: git clone https://github.com/Manideepak788/Air_Quality_Prediction.git
Environment: Ensure you have pandas, seaborn, and sklearn installed.
Run: Open the .ipynb file in Google Colab or Jupyter and run all cells to reproduce the results.

📂 Repository Structure

AirQualityUCI.csv: Raw sensor data.
AirQuality_Processed.csv: Final dataset after cleaning and engineering.
AirQuality_Analysis.ipynb: Main analysis notebook.
README.md: Project documentation.

📜 References

Vito, S. De, et al. (2008). On field calibration of an electronic nose. Sensors and Actuators B: Chemical.UCI Machine Learning Repository: Air Quality Data Set.
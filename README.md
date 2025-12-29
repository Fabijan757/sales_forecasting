Project Name: Sales Forecasting 

Project Description
This project focuses on analyzing and forecasting daily sales using historical data.
The goal is to understand sales behavior over time and build a simple but meaningful
model capable of predicting future sales.

Data
The dataset contains daily sales data with additional features:
- date
- total sales
- promo (0/1)
- is_holiday (0/1)
- day of week
- month

The data is aggregated at a daily level.

EDA (Exploratory Data Analysis)
In the first part of the project, exploratory data analysis was performed to understand:
- how sales change over time
- differences between weekdays and weekends
- the impact of holidays on sales
- extreme days with unusually high sales

Visualizations showed that:
- sales increase during weekends
- sales are higher during holidays
- there are occasional large spikes in sales

Baseline Model
A simple baseline model was created using a 7-day moving average.

Baseline model idea:
- calculate the average sales of the last 7 days
- use that value as the prediction for future days

The baseline model serves as a reference.
Any more advanced model should outperform or at least match this baseline.

Train / Test Split
The data was split using a time-based approach:
- Train set: all days except the last 30
- Test set: last 30 days of the year

Prophet Model
A Prophet model was used to capture trend and seasonality.
The following regressors were added:
- promo
- is_holiday

The model was trained on the training set and evaluated on the last 30 days.

Model Comparison
The baseline model and Prophet model were compared using MAE and RMSE metrics.

Final Forecast
The Prophet model was trained on the full dataset.
A forecast for the next 90 days was generated.
For future dates, the following assumptions were made:
- promo = 0
- is_holiday = 0

Conclusion
This project demonstrates the complete time series workflow:
- data analysis
- baseline modeling
- advanced modeling
- evaluation
- final forecasting



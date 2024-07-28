# Time Series Analysis and Forecasting of Airline Baggage Complaints

## Project Overview
This project aims to analyze and forecast airline baggage complaints using time series data. The dataset includes baggage complaints, scheduled flights, canceled flights, and enplaned passengers for three airlines: American Eagle, Hawaiian, and United, spanning from January 2004 to December 2010. The objective is to understand trends, seasonality, and patterns in baggage complaints and to forecast future complaints using advanced time series modeling techniques.

## Data Description
The dataset consists of monthly records with the following columns:

Date: The date of the record.
Airline: The name of the airline.
Month: The month of the record.
Year: The year of the record.
Baggage: The number of baggage complaints.
Scheduled: The number of scheduled flights.
Cancelled: The number of canceled flights.
Enplaned: The number of enplaned passengers.

## Approach
### Data Preprocessing and Feature Engineering
Data Loading and Initial Exploration:

The dataset was loaded and basic exploratory data analysis (EDA) was performed to understand its structure and contents.

### Feature Engineering:

A new feature, Baggage %, was created to adjust for the company's size by calculating the rate of baggage complaints as a percentage of enplaned passengers.

### Data Segmentation
Segmentation by Airline:
The data was segmented into three separate dataframes for each airline: American Eagle, Hawaiian, and United. This allowed for more granular analysis and comparison between the airlines.

### Exploratory Data Analysis (EDA)
Trend Analysis:

Time series plots were created to visualize the trends in baggage complaints over time for each airline.

### Seasonality Analysis:

The average monthly baggage complaint rates were plotted to investigate potential seasonal patterns in the data.

### Statistical Analysis
Descriptive Statistics:

Summary statistics were computed to compare the average number of scheduled flights and enplaned passengers across the three airlines.
Rate Comparison:

The average Baggage % was compared across airlines to provide a standardized measure of performance.

### Time Series Decomposition
Seasonal Decomposition:
Seasonal decomposition was performed to break down the time series into its observed, trend, seasonal, and residual components.

### Modeling and Forecasting
Model Selection using Auto ARIMA:

The Auto ARIMA method was used to determine the optimal order for the ARIMA model considering seasonality.
SARIMA Model:

A Seasonal ARIMA (SARIMA) model was fit to the training data, and its performance was evaluated using RMSE on the test set.
Forecasting:

The SARIMA model was used to forecast baggage complaints for one year into the future.

### Visualization
Interactive Plots:
Plotly was used to create interactive plots for better visualization of trends, seasonality, and forecasted values.

## Findings
#### 1. Size and Scale:

United Airlines, being a much larger airline, had the highest absolute number of baggage complaints but a lower rate of complaints when adjusted for the number of enplaned passengers.

#### 2.Baggage Complaint Rates:

American Eagle had the highest rate of baggage complaints per enplaned passenger, followed by United and Hawaiian.

#### 3.Seasonal Patterns:

All three airlines exhibited similar seasonal patterns, with higher complaint rates in December, January, and the summer months, and lower rates in the spring and late fall.

#### 4.Trend Analysis:

Baggage complaint rates increased for American Eagle and United through 2006 and began declining thereafter. Hawaiian's complaint rates were relatively flat with minor fluctuations.

#### 5.Forecast Accuracy:

The SARIMA model provided reasonable forecasts with an RMSE that was insignificant compared to the standard deviation of the mean baggage complaints.

#### 5.Managerial Insights:

Airlines should anticipate higher complaint rates in peak travel months and plan accordingly. American Eagle, in particular, should consider strategies to reduce its higher complaint rate.

## Conclusion
The analysis revealed significant insights into the trends and patterns of baggage complaints across different airlines. By adjusting for the number of enplaned passengers, a more accurate comparison of performance was achieved. The SARIMA model provided effective forecasts, aiding in better planning and resource allocation for airlines. This project demonstrates the importance of time series analysis in understanding and forecasting operational metrics in the airline industry.

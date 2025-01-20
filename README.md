# Website Performance Analysis

This project aims to analyze website performance metrics, such as user engagement and session activity, using time series analysis and visualization techniques. The data is processed and visualized to understand patterns, trends, and relationships between different metrics over time.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Visualization](#visualization)
- [Time Series Analysis](#time-series-analysis)
- [Conclusion](#conclusion)

## Introduction
This project leverages historical website performance data to analyze user behavior, session activity, and engagement metrics. By utilizing data visualization and time series analysis, insights can be drawn to improve website performance and user experience.

## Dataset
The dataset used in this analysis contains hourly data on users, sessions, and various engagement metrics. The key columns include:
- Date + hour (YYYYMMDDHH)
- Users
- Sessions
- Engaged sessions
- Average engagement time per session
- Engaged sessions per user
- Events per session
- Engagement rate
- Session primary channel group (Default channel group)

## Data Preprocessing
1. **Data Loading**: The dataset is loaded from a CSV file.
2. **Header Adjustment**: The first row is set as the header, and the index is reset.
3. **Data Type Conversion**: Relevant columns are converted to appropriate data types, such as datetime and numeric.
4. **Data Aggregation**: Data is grouped by date and hour, and metrics are summed or averaged as needed.

## Visualization
### Users and Sessions Over Time
A line plot is created to visualize the total number of users and sessions over time, providing a clear view of traffic trends.

### Engagement Metrics
Engagement metrics such as average engagement time per session, engaged sessions per user, events per session, and engagement rate are plotted over time to understand user interaction with the website.

### Scatter Plots
Scatter plots are used to explore relationships between various engagement metrics, such as:
- Average engagement time vs. Events per session
- Average engagement time vs. Engagement rate
- Engaged sessions per user vs. Events per session
- Engaged sessions per user vs. Engagement rate

### Channel Performance
Bar plots are used to compare performance across different session primary channel groups, highlighting users, sessions, normalized engagement rate, and events per session.

## Time Series Analysis
### Differencing and Stationarity
The time series data for sessions is differenced to achieve stationarity, making it suitable for time series modeling.

### ACF and PACF Plots
Autocorrelation (ACF) and Partial Autocorrelation (PACF) plots are generated to identify the order of ARIMA models.

### SARIMA Model
A Seasonal ARIMA (SARIMA) model is fitted to the data to forecast future session activity. The model parameters are:
- Order: (1, 1, 1)
- Seasonal Order: (1, 1, 1, 24)

### Forecasting
The model forecasts the next 24 hours of session activity, and the results are plotted alongside the actual data for comparison.

## Conclusion
The analysis provides valuable insights into website performance and user engagement. By understanding traffic patterns and engagement metrics, stakeholders can make informed decisions to enhance the website's user experience and optimize performance.

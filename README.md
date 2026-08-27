# covid-hospital-admission
Time series analysis and forecasting project examining hospital bed occupancy and COVID-19 census trends across New York State, built to support short-term hospital resource planning.

# Overview

Hospitals need reliable short-term forecasts of patient census to plan staffing, bed allocation, and supply chains. This project analyzes historical hospital census data from New York State to identify temporal patterns in COVID-19 hospitalizations and builds toward forecasting models that can support that kind of operational decision-making.

# Dataset

Data comes from New York's Health Electronic Response Data System (HERDS) hospital survey, which tracks:

- As of Date — the reporting date for each data point
- Facility Name — hospital name, used for geographic breakdowns
- Patients Currently Hospitalized — confirmed positive patients in inpatient or observation beds at time of reporting
- Total Hospitalizations — sum of all patients across age groups per facility per time point

Goals
- Identify key drivers of hospital admissions
- Detect and quantify temporal patterns in census data
- Support operational decision-making (e.g., bed occupancy thresholds)
- Compare forecasting model performance
- Develop accurate short-term forecasting models

# Methods

The analysis treats hospital census as a time series — sequential, chronologically dependent data where past observations influence future ones, violating standard regression assumptions and requiring specialized modeling approaches.

- Autocorrelation Function (ACF): measures correlation between the series and its own lagged values, showing how strongly current census levels relate to recent history
- Partial Autocorrelation Function (PACF): isolates the unique contribution of each lag by controlling for shorter lags, helping identify the appropriate autoregressive model order

# Note
This work is originally from a course taken at Arizona State University. See DAT 402 Machine Learning on ASU Course Calendar for more.

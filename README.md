# NYC Taxi Demand Forecasting

## Project Overview
This project predicts **daily ride demand** in New York City using the NYC Taxi dataset.  
The goal is to provide accurate forecasts that can help optimize fleet management and improve rider availability.

## Features
- Queried raw trip data using **Amazon Athena**  
- Engineered **time-based features** (day, week, month, lag variables)  
- Built multiple forecasting models:  
  - **ETS (Error, Trend, Seasonality)**  
  - **Holt-Winters**  
  - **LightGBM with lag features**  
- Stored predictions in **S3 & SQLite**, with pipeline integration for PostgreSQL  
- Built **Power BI dashboards** with 6–10 interactive visualizations  

## Tech Stack
- **Languages & Libraries**: Python, Pandas, Statsmodels, LightGBM, Matplotlib  
- **AWS Services**: Athena, S3, Lambda, Glue  
- **Visualization**: Power BI  
- **Database**: SQLite, PostgreSQL  

## Repository Structure

├── notebooks/ # Data exploration & modeling

├── src/ # Forecasting scripts

├── powerbi/ # PBIX files for dashboards

├── requirements.txt # Dependencies


## How to Run Locally

# Clone the repo

git clone https://github.com/nivesharath/nyc_taxi25.git

cd nyc_taxi25

# Install dependencies

pip install -r requirements.txt

# Run forecasting script

python src/run_forecast.py

**Results**

- Compared ETS, Holt-Winters, and LightGBM models

- Identified weekly and monthly demand patterns

- Delivered interactive Power BI dashboard for stakeholders

**Future Improvements**

Add external regressors (weather, events) for improved accuracy

Automate dashboard refresh using Power BI Service + AWS Lambda

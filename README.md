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

├── .github/workflows/        # CI/CD pipelines

│   ├── feature_pipeline.yaml

│   ├── inference_pipeline.yaml

│   └── model_training_pipeline.yaml

├── frontend/                 # Streamlit dashboards

│   ├── frontend.py

│   ├── frontend_v2.py

│   └── frontend_monitor.py

├── notebooks/                # Experiments, EDA & forecasting

│   ├── 01_fetch_data.ipynb

│   ├── ... (baseline, XGBoost, LightGBM, retraining)

│   ├── ARIMA.ipynb

│   ├── ARMA.ipynb

│   └── Prophet.ipynb

├── pipelines/                # ML pipelines

│   ├── model_training_pipeline.py

│   └── inference_pipeline.py

├── src/                      # Core utilities

│   ├── config.py

│   ├── data_utils.py

│   ├── feature_pipeline.py

│   ├── inference.py

│   └── plot_utils.py

├── requirements.txt

├── requirements_feature_pipeline.txt

└── requirements_with_version.txt

## How to Run Locally

## Clone the repo
git clone https://github.com/nivesharath/nyc_taxi25.git
cd nyc_taxi25

## Install dependencies
pip install -r requirements.txt

## Run forecasting script
python frontend/frontend_v2.py

## Results

- Compared ETS, Holt-Winters, and LightGBM models

- Identified weekly and monthly demand patterns

- Delivered interactive Power BI dashboard for stakeholders

## Future Improvements

Add external regressors (weather, events) for improved accuracy

Automate dashboard refresh using Power BI Service + AWS Lambda

# AquaRwanda Intelligence

An interactive R/Shiny dashboard for monitoring water consumption, billing, customer activity, data quality, and demand forecasting for a Kigali water utility.

## Data Disclaimer

To avoid using confidential or proprietary utility data, this project runs on a fully simulated dataset that was built to follow realistic patterns (consumption by customer type, seasonality, billing logic, and some intentional data-quality issues) so the analysis has real substance to work with. The geography (District/Sector/Cell) is based on Rwanda's real administrative structure for Kigali.

**Note:** Raw data files are excluded from this repo. To run the app, place dim_customers.csv, dim_geography.csv, and fact_consumption_billing.csv in data/raw/.

## Features

- **Overview:**  KPIs, consumption trends, customer type and district breakdowns, with a district filter
- **Billing & Revenue:** revenue trends, payment status, consumption vs. revenue
- **Anomalies:**  flagged data-quality issues in an interactive table
- **Forecasting:** 6-month demand forecast (ETS model, validated against a Naive baseline using RMSE/MAE)

## Tech Stack

R, Shiny, shinydashboard, tidyverse, DT, forecast

## Running Locally

```r
install.packages(c("shiny", "shinydashboard", "tidyverse", "DT", "forecast"))
```
Open `app.R` in RStudio and click **Run App**. (Requires the data files described above in `data/raw/`.)


# 🌐 FourCastNet Evaluation: ERA5 Comparison (10 vs 14 Days)

This repository contains a detailed evaluation of the [FourCastNet](https://github.com/NVIDIA/FourCastNet) weather forecasting model using reanalysis data from ERA5. The goal of this project was to assess the accuracy of FourCastNet predictions across a 14-day forecast window and compare the performance when run for 10 days vs 14 days.

---

## 📌 Project Summary

- ✅ **Forecast Variable Evaluation**: Mean Sea Level Pressure (MSLP), 500 hPa Temperature, U Wind, and V Wind.
- 📊 **Comparison**: RMSE (Root Mean Square Error) between FourCastNet outputs and ERA5 reanalysis data.
- 🔍 **Objective**: Investigate whether extending the forecast horizon from 10 to 14 days significantly degrades forecast accuracy.
- 🧪 **Region**: Focused over the Indian subcontinent (custom lat/lon bounds).
- 📈 **Outcome**: Results highlight increasing RMSE beyond day 10, especially for dynamic variables like wind, while temperature remains relatively stable.

---

## 🗂️ Repository Structure

fourcastnet-evaluation_14days/
├── notebooks/
│ ├── Running_AIWP # FourcastNetv2-small pre trained model
├── data/
│ ├── Fmodel_inputfile # Input forecast dataset
│ └── inputdata_breakdown 
  └── fourcastnetmodel_14days
├── results/
│ ├── rmse_analysis # RMSE results 10 days vs 14 days 
│ ├── rmse_results_14days.png # RMSE trend over 14-day forecast
├── report/
│ └── FourcastModel14days.pdf # Full project report with visual analysis
├── README.md # You are here!

## Key Finding
📉 Forecast accuracy is relatively stable up to 10 days. Beyond that, RMSE increases sharply—particularly for wind variables—highlighting the limitations of long-range deterministic forecasts.

## Requirements
xarray
numpy
pandas
matplotlib
netCDF4
ipywidgets
cdsapi
pygrib

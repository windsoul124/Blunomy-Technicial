# Enhancing Road Safety in Victoria: Data-Driven Insights from Crash Analysis



## Overview
This repository contains my technical test submission for crash severity analysis using the **Victorian Government Crash Stats** dataset.  
The aim is to identify factors driving crash severity and build a predictive model that can inform interventions for reducing serious injuries and fatalities on Victorian roads.

## Project Structure
The analysis is divided into four main Jupyter notebooks:

1. **Data Aggregation.ipynb**
   - Merges raw datasets (ACCIDENT, PERSON, VEHICLE, etc.) using `ACCIDENT_NO` as the primary key.
   - Aggregates person- and vehicle-level data into accident-level features.
   - Produces a clean, unified dataset for further analysis.

2. **Data Imputation.ipynb**
   - Handles missing values and placeholder codes (e.g., `999` in SPEED_ZONE).
   - Imputes missing fields using logical domain rules (e.g., location-based median/mode).
   - Creates derived features such as `IS_WEEKEND`, `ACCIDENT_TIME_HOUR`, `ACCIDENT_TIME_MONTH`.

3. **Exploratory Data Analysis.ipynb**
   - Investigates patterns and correlations between features and crash severity.
   - Visualises severity distribution across speed zones, lighting conditions, time of day, and more.
   - Highlights high-risk conditions and locations.

4. **Model Development.ipynb**
   - Prepares the dataset for modelling (encoding, splitting, class imbalance handling).
   - Trains an **XGBoost** classifier with early stopping.
   - Evaluates performance using confusion matrix, macro F1-score, and feature importance.
   - Uses **SHAP** for interpretability of key drivers.

## Dataset
- **Source**: Data Scientist Crash Stats Test
- **Period**: 2006–2023  

## Tools & Libraries
- **Python**: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `xgboost`, `shap`
- **Data Visualisation**: Matplotlib/Seaborn (EDA) and Power BI (dashboard) for presentation
- **Version Control**: GitHub for source code management

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/windsoul124/Enhancing-Road-Safety-in-Victoria.git
   cd crash-severity-analysis

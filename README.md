
# Airbnb Price Analysis & Prediction

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/samarth-91/Airbnb-Data-Analysis/blob/main/Airbnb_Data_Analysis.ipynb)

## Overview

End-to-end data analysis and price prediction project on Airbnb listings data. Covers exploratory data analysis, feature engineering, and ML modelling to identify key drivers of listing price.

## Dataset

Two CSV files from the [Inside Airbnb](http://insideairbnb.com/) dataset:

- `listings.csv` — listing details (host info, property type, amenities, review scores, etc.)
- `calendar.csv` — date-level availability and price data

## Project Structure

```
├── Airbnb_Data_Analysis.ipynb   # Main notebook
├── Price distribution.png
├── number of available listings.png
├── average price for month.png
├── average price for neighbourhood.png
├── correlations.png
├── feature importances RF.png
└── feature importances XGB.png
```

## Key Steps

**1. Data Cleaning & Feature Engineering**
- Merged `listings.csv` and `calendar.csv` on `listing_id`
- Dropped irrelevant/high-null columns
- Parsed dates, extracted month/year
- Encoded list-type columns (amenities, host verifications) as binary dummy columns
- Imputed missing values with mean/mode
- Converted price strings (`$1,200.00`) to float

**2. Exploratory Data Analysis**
- Price distribution across listings
- Average price trends by month
- Price breakdown by neighbourhood group
- Correlation heatmap between numerical features and price

**3. Machine Learning Models**

| Model | Metric | Train | Test |
|---|---|---|---|
| Random Forest Regressor | R² | — | — |
| Random Forest Regressor | MSE | — | — |
| XGBoost Regressor | R² | — | — |
| XGBoost Regressor | MSE | — | — |

> Fill in your actual scores after running the notebook.

**4. Feature Importance**
- Top 15 features ranked by importance for both RF and XGBoost models
- Key drivers include: `accommodates`, `bedrooms`, `bathrooms`, `beds`, `review_scores_rating`, `host_since_year`

## Tech Stack

- Python 3
- pandas, NumPy
- Matplotlib, Seaborn
- scikit-learn (Linear Regression, Random Forest, train/test split, metrics)
- XGBoost
- Google Colab

## How to Run

1. Clone the repo
   ```bash
   git clone https://github.com/samarth-91/Airbnb-Data-Analysis.git
   ```
2. Upload `listings.csv` and `calendar.csv` to your Google Drive (path: `MyDrive/air bnb dataset/`)
3. Open the notebook in Google Colab using the badge above
4. Run all cells

## Results

- Seasonal pricing trends identified — prices peak in summer months
- Neighbourhood group is a strong predictor of listing price
- Random Forest and XGBoost both outperform linear regression on this dataset
- Top price predictors: number of rooms, accommodates capacity, and review scores

## Author

**Samarth Singh**  
B.Tech Electronics & Telecommunication Engineering, VIIT Pune  
[GitHub](https://github.com/samarth-91)

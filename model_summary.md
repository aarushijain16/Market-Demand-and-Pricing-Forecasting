
# 🔹 Model Summary - Forecasting Airbnb Demand in London

# Objective
To evaluate predictive modelling approaches for forecasting Airbnb demand in London despite the absence of direct demand data, by engineering proxy demand signals and identifying the most influential drivers of price and demand.

# Data & Scope

- Source: InsideAirbnb listings data (Aug 2008 – Mar 2023)

- Geography: London (segmented into Inner vs Outer London)

- Records: ~75k listings

- Features: Pricing, availability, room characteristics, reviews, host and property attributes

# Demand Proxy Engineering

Since actual booking data was unavailable, demand was estimated using a composite proxy derived from:

- Reviews per month

- Availability (availability_365)

- Price

- Minimum nights

- Listing characteristics (beds, bedrooms, bathrooms, accommodates)

This approach allowed demand modelling under realistic marketplace constraints - a key real-world analytics challenge. 


# Segmentation Strategy

Listings were clustered using DBSCAN, segmenting demand behaviour by room type:

- Entire home / apartment

- Private room

- Shared room

- Hotel room

This ensured models captured heterogeneous demand patterns rather than assuming a single global relationship.

# Models Evaluated

Three supervised ML models were trained and evaluated within each cluster:

- Decision Tree Regression

- Random Forest Regression

- Extreme Gradient Boosting (XGBoost)

# Evaluation Metrics

- RMSE (forecast accuracy)

- R² (explanatory power)

# Key Model Results

- XGBoost consistently outperformed other models across all room types

- Achieved:

  - Lowest RMSE

  - Highest R²

- Demonstrated strong ability to capture non-linear relationships between price, availability, and demand

# Key Demand Drivers Identified

Across segments, demand was most strongly influenced by:

- Room type (largest driver)

- Price (inverse relationship)

- Availability in next 90–365 days

- Minimum nights requirement

- Reviews per month

- Capacity (beds, bedrooms, accommodates)

# Business Value

The modelling framework enables:

- Demand-aware pricing strategies

- Supply optimisation by neighbourhood

- Better host revenue planning

- Scalable application to other global cities

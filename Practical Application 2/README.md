## Project Overview

# Practical Application 2: What Drives the Price of a Car? A CRISP-DM Approach

This [project](**Practical%20Application%202.ipynb**)  follows the CRISP-DM (Cross-Industry Standard Process for Data Mining) framework, a widely adopted methodology for structuring data science projects. Using a dataset of 426,000 used cars, the goal is to uncover the key factors that influence vehicle pricing and provide actionable insights for a used car dealership.

## Business Case
A used car dealership aims to optimize its pricing strategy by understanding the factors that influence the price of a used car. By analyzing historical listing data, we can identify pricing trends, assess vehicle depreciation patterns, and determine how various attributes—such as mileage, model year, brand, and location—affect resale value. These insights will enable the dealership to:

- Optimize pricing strategies by setting competitive and profitable price points.
- Improve inventory management by prioritizing vehicle types that retain value.
- Enhance customer satisfaction by aligning inventory with buyer expectations.

## Data Description
The dataset contains details of used cars listed for sale, including various features that may impact their prices. Below is a breakdown of the key features:

### Features:
- **id**: Unique identifier for each listing.
- **region**: Geographic location where the car is being sold.
- **price**: Listed price of the vehicle.
- **year**: Manufacturing year of the vehicle.
- **manufacturer**: Brand of the vehicle (e.g., Ford, Toyota, Chevrolet).
- **model**: Specific model of the vehicle.
- **condition**: Reported condition of the car (e.g., new, like new, excellent, good, fair, salvage).
- **cylinders**: Number of engine cylinders (e.g., 4, 6, 8, or other configurations).
- **fuel**: Type of fuel the car uses (e.g., gas, diesel, electric, hybrid).
- **odometer**: Mileage of the car at the time of listing.
- **title_status**: Legal status of the car title (e.g., clean, rebuilt, salvage, lien, missing, parts only).
- **transmission**: Type of transmission (e.g., automatic, manual, other).
- **VIN**: Vehicle Identification Number (may be missing in some records).
- **drive**: Drivetrain of the vehicle (e.g., front-wheel drive, rear-wheel drive, four-wheel drive).
- **size**: Classified vehicle size (e.g., compact, mid-size, full-size, sub-compact).
- **type**: Category of the vehicle (e.g., sedan, SUV, pickup, truck, coupe, convertible).
- **paint_color**: Exterior color of the vehicle (e.g., white, blue, red, black, silver).
- **state**: Location of the listing by state.

### Notes:
- Some records contain missing values, particularly in manufacturer, model, condition, cylinders, fuel, title_status, transmission, drive, size, type, and paint_color.
- The dataset includes a wide variety of manufacturers, with notable brands such as Chevrolet, Ford, Toyota, and Nissan.
- The price variable is the primary target for analysis, with other attributes serving as potential influencing factors.

## Exploratory Data Analysis (EDA)

### Descriptive Statistics Summary
The dataset includes three key variables: Price ($), Year (Manufacturing Year), and Odometer (Mileage).

| Statistic       | Price ($)     | Year      | Odometer (miles) |
|-----------------|---------------|-----------|------------------|
| **Count**       | 426,880       | 425,675   | 422,480          |
| **Mean**        | 75,199        | 2011      | 98,043           |
| **Median (50%)**| 13,950        | 2013      | 85,548           |
| **Min**         | 0             | 1900      | 0                |
| **Max**         | 373,692,871   | 2022      | 10,000,000       |

### Key Observations
- **Outliers in Price & Mileage**: A max price of $373M and mileage of 10M miles suggest data issues.
- **Right-Skewed Distribution**: The median price ($13,950) is significantly lower than the mean ($75,199), indicating a right-skewed distribution of prices.
- **Missing Data**: The year and odometer fields have missing values, requiring imputation or removal.

### Inferential Statistics Considerations
- **Skewness & Outliers**: Extreme values should be filtered out to avoid skewing the analysis.
- **Expected Correlations**:
  - Negative correlation: Higher mileage → lower price.
  - Positive correlation: Newer cars → higher price.
- **Regression Modeling**: The next steps involve predicting car price using variables such as mileage, year, brand, and fuel type.


![Acceptance Rate Plot](images/numerics.png)

### Data Cleaning Recommendations
- Remove unrealistic values (e.g., price = 0, year = 1900, odometer > 500,000).
- Normalize or log-transform price to reduce skewness.
- Address missing values in year and odometer columns.
- Perform a correlation matrix and regression analysis to validate trends.

## Recommendations and Next Steps

### Data Cleaning & Preprocessing
- Remove extreme outliers (e.g., unrealistic prices and mileage values).
- Impute missing values in critical fields such as year and odometer to ensure data consistency.
- Normalize or log-transform the price variable to mitigate skewness.

### Feature Engineering
- Categorize mileage into bins (e.g., low, moderate, high) to enhance analysis.
- Engineer an "age vs. mileage interaction" feature to more accurately assess depreciation patterns.

### Model Development & Pricing Prediction
- Implement regression models (e.g., Random Forest, XGBoost) to predict car prices.
- Perform cross-validation to ensure model robustness and generalizability.

### Market Insights & Business Strategy
- Optimize inventory by prioritizing vehicle types and brands that retain value over time.
- Adjust pricing strategies based on geographic demand and vehicle condition.
- Monitor depreciation trends to improve the timing of buying and selling vehicles.

## Conclusion
This project provides an in-depth analysis of the key factors influencing used car prices using a CRISP-DM approach. We have identified several critical insights:
- Vehicle age and mileage are the strongest predictors of price.
- Brand reputation plays a significant role in value retention.
- Vehicle condition, fuel type, and transmission contribute to price variations.
- Geographic location influences demand and resale value.

By leveraging these insights, a used car dealership can refine pricing strategies, optimize inventory, and maximize profitability. The next steps involve enhancing predictive models to increase accuracy and offer actionable recommendations for dynamic pricing.

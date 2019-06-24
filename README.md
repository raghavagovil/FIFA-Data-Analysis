# FIFA-Data-Analysis
## Group Members: Raghava Govil, Konner Macias

## Problem Statement
Using soccer players' attributes to predict their annual wage in dollars

## Data Exploration
- On exploring the data, we found a lot of missing data/null variables
- Some of the variables do not have a normal distribution, making it harder to fit a linear model
- A lot of variables are exponentially associated with wage, indicating need for transformations
- Some of the club and country names are dirty - need to be corrected

## Data Wrangling and Feature Engineering
- Dropped all variables like id, ob, etc which do not directly help in predicting wage
- Imputed all null values with either mean or median, as intuition directed
- Cleaned the position ratings
- Created a new variable with the mean of the position ratings
- Cleaned country names
- Grouped players by continent instead of country
- Cleaned club names
- Grouped players by league instead of country
- Grouped players be overall positions - attack, midfield, defence

## The Model
- Implemented 10-K Fold to due to small data 
- Used an XGBoost Regressor due to non-linearity of data
- Achieved accuray of 89% with training data

## Future improvements
- Transform the variables
- Bucket the data as some distributions indicate
- Incorporate AIB/BIC criterion

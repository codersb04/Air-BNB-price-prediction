# Air-BNB-price-prediction
## Task
Build a Machine Learning model to predict the price of the Air bnb house.</br>
Tool Use: Python, Jupyter Notebook
## Dataset:
Dataset is taken from Kaggles repository "New York City Airbnb Open Data". Contains 48895 set of datas with 16 features. The features are:
1. id: Unique ID of the Airbnb listing.
2. name: Name of the listed property.
3. host_id: Unique ID of the host.
4. host_name: Name of the host.
5. neighbourhood_group: General region of the location (neighborhood), e.g., Brooklyn, Manhattan, Queens, Staten Island, and Bronx.
6. neighbourhood: Specific neighborhood where the property is located.
7. latitude: Latitude coordinate of the property.
8. longitude: Longitude coordinate of the property.
9. room_type: Type of room (e.g., Private room, Shared room, Entire home/apt).
10. price: Price per night (in USD).
11. minimum_nights: Minimum number of nights guests are required to stay.
12. number_of_reviews: Number of reviews the listing has received.
13. last_review: Date of the last review.
14. reviews_per_month: Average number of reviews per month.
15. calculated_host_listings_count: Total number of properties listed by the host.
16. availability_365: Number of days the property is available in a year.</br></br>

Credit: https://www.kaggle.com/datasets/dgomonov/new-york-city-airbnb-open-data/data

## Steps Involved:
### Import Libraries:
- Import all the necessary libraries:
  - Numpy
  - Pandas
  - Matplotlib
  - Seaborn
- Libraris to visualize inline Jupyter maps:
  - folium
  - Marker CLuster
  - Fast Marker Cluster
  - Heat Map
- Libraries for Data Processing
  - Robust Scaler
  - Standard Scaler
  - KNN Imputer
- Libraries for building model
  - train test solit
  - Linear regression, Lasso, Ridge
  - K Neighbors Regressor
  - Decision Tree Regressor
  - Random Forest Regressor
  - Mean Absolute Error
  - Mean Squared Error
  - r2_score
 
### Data Collection and Analysis:
- Load the data using pandas read_csv method
- Analyse the data using function shape, describe, isnull and info
- **Handle the missing value**:
  - Use Robust Scaler class the scale the data of the column.
    - Robust Scaler: RobustScaler is a class in sklearn.preprocessing module that scales features using statistics that are robust to outliers. It removes the median and scales the data according to the quantile range between the first and third quartile. It has arguments to control whether the value is centered to zero, scaled to the interquartile range, or copied.
  - Use KNN Imputer to fill the missing values
    - KNN Imputer: KNNimputer is a scikit-learn class used to fill out or predict the missing values in a dataset. It is a more useful method which works on the basic approach of the KNN algorithm rather than the naive approach of filling all the values with mean or the median. In this approach, we specify a distance from the missing values which is also known as the K parameter. The missing value will be predicted in reference to the mean of the neighbours. It is implemented by the KNNimputer().
  - Inverse the work done by Robust Scaler Class. Scaling is done only to fill the NULL values.
  - Update the new values to the main dataframe
### Data Visualization:
- Visualizing Geographical Loaction using Folium library
- Heat map for geographical distribution
- Analysis of categorical Variables
- Numerical Data analysis
- Analysis of Categorical columns with Target column(Price)
- Correlation Matrix for Numerical data
- Analysing the Target Column: Price
- Location based data on neighbourhood type
- Location distribution based on Prices
- Pie chart for Neighbour hood distribution
- Price distribution by Room type in Neighbourhood group
- Comparing each feature with another
### Data Processing
- Drop all the irrelavent columns
- Convert the categorical Text data to numerical values using get_dummies function
- Data Standardization using Standard scaler for all the numerical column
- Split the data into target and features
### Model Building
- Split the data into training and test set
- Create a list of all models to be used
- Train and model and get performace metrix for all the model
- Plot the bar grah for mean absolute error, mean squared error and r2 score comparing all the model performance.</br></br></br>

Reference: Airbnb_NYC_EDA_Price_Prediction_ML, MEHMET ISIK, https://www.kaggle.com/code/mehmetisik/airbnb-nyc-eda-price-prediction-ml#Visualizing-Geographic-Locations-on-an-Interactive-Map
 
  

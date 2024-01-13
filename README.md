## Project/Goals
Project Title: Falvors of Success (Predicting the Restaurant Popularity in Paris using Open Data like Yelp, Google Maps and Bike Station density etc.)

Project Summary:
The project focuses on leveraging open data to build a model that will help predict the restaurant popularity in Paris basis features like location of restaurant, competitors in vicinity, POI density within 1km, cuisine type etc.

## Process
### Step 1
Data Collection:
1. Yelp API - We fetched the data of 2500 restaurants in Paris using latitude and longitude.
2. Google Maps Places - For the mentioned latitude and longitude, we got details from google places api regarding the street popularity, reviews, different types of POIs within 1km
3. City Bike API - This api was leveraged to churn the data of bike stations within the 1 km vicinity of the restaurants 
    
### Step 2
Data Cleaning:

  Objective: Address and rectify any inconsistencies, missing values, or anomalies in the dataset.
  
  Activities:  
    *Remove duplicates and drop redundant columns <br>
    *Change data types (if required) <br>
    *Feature engineering - Create new features for better modeling <br>
    *Modify column names <br>
    *Aggregate data to update the data granularity for merging all the datasets <br>

### Step 3 
EDA:

Objective: Study data patterns to do feature selection, transformation, treating outliers and missing values for better modeling
  
Activities:<br>
    *Study the histograms for analyzing skewness and variance in numerical columns distribution<br>
    *Boxplots to identify outliers<br>
    *Bar charts for categorical variable distribution<br>
    *Geographical analysis of various data points to establish hypothesis for feature importance<br>
    
### Step 4
Feature Selection:

Objective: Drop features not relevant for modeling using statistical tests and other methods

Activities:<br>
    *Correlation heatmap to study the multi-collinearity within the data<br>
    *T-tests for selecting numerical variables with p value < 0.05 <br>
    *Chi-square tests for selecting categorical variables with p-values < 0.05 <br>
    *Drop variables that are not relevant from business standpoint or having a high missing value proportion <br> 

### Step 5
Model Building:

Objective: Try and tune different models on the given dataset. Check for bias and variance and select the best performing model accordingly. 

Activities:<br>
  *KNN Model <br>
      - Plot the ROC curve and check the model performance (recall, accuracy) on train and test set <br>
  *Logistic Regression <br>
        - Plot the ROC curve and check the model performance (recall, accuracy) on train and test set <br>
  *BalancedRandomForestClassifier <br>
        - Plot the ROC curve and check the model performance (recall, accuracy) on train and test set <br>
  *Random Forest (Tuned) with threshold adjustment to handle class impbalance in the dataset <br>
        - Plot the ROC curve and check the model performance (recall, accuracy) on train and test set <br>
 
### Step 6 
Documentation and Reporting:

Objective: Summarize the findings from this project in the form of a presentation for the relevant audience. 

## Results
Following are the insights from this analysis - 
1. Price senstivity of customers - it shows that customers are price sensitive and most of the cheaper restaurants are located on the outskirts of the city. Restaurant review counts and ratings are higher for cheaper alternatives within the heart of the city.
2. POI density - Most of the tourist spots are within the centre of the city and the POIs like lodging, banks etc are located on the outskirts.
3. Population density - Population density is higher on the outskirts compared to the central part of the city.
4. French cuisine seems to be an outlier contributing to about 53% of overall distribution, closely followed by Italian and Bistros.
5. Final factors that contribute significantly to the restaurant popularity -
   5.1 Pricing with respect to location (heart of the city or outskirts)
   5.2 POI Density
       5.2.1 Street popularity as per google maps
       5.2.2 Vicinity to public transit stations, shopping malls and museums
       5.2.3 The most populated areas in the map are the most served (i.e. they have a very high POI density of Banks, ATMs, Supermarkets etc)


## Challenges 
1. Data size was limited to 1700 restaurant (after joining all the sets) owing to Yelp API limitations of 500 Lat Long calls per 24 hours
2. Language difference in open data source was challenging at times 
3. Demographic data like income per capita, age groups, real estate prices etc were available on payment

## Future Goals
1. Data collection
   - Research for more open data and include the same for future modeling
   - Accumulate more data through multiple api calls to be able to better train the model

2. Data Engineering -
   - Adjust the data engineering in order to train the model with more data

3. User friendly dashboard for more real time insights to prospective restaurant owners - User can identify restaurant locations to better cater to their target segments in terms of cuisine preference, pricing, and market competition etc. 

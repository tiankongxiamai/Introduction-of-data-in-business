# Introduction-of-data-in-business
How urbanization degree influence on the room number per capital

The analysis involved several key steps:
Data Collection: Data on the average number of rooms per person by degree of urbanization (from 2003 to 2023) was sourced from Eurostat (link). This dataset provided information categorized by both country and degree of urbanization.
Data Preparation: Since the original file had multiple parameters per row (both degree of urbanization and country), it was not directly usable. To resolve this, we split the data into three distinct datasets: deg1, deg2, and deg3, corresponding to the average number of rooms per person in areas of urbanization degrees 1, 2, and 3, 
respectively. Data cleaning involved removing rows corresponding to groups of countries (e.g., "EU27" or regional clusters), focusing only on individual countries. Given that there were minimal fluctuations in the data over time, we calculated an average value across the period from 2003 to 2023 to represent each country’s housing conditions for each degree of urbanization. Calculation of Percentage Change: For each country, we computed the percentage change in the average number of rooms per person between Degree 3 and Degree 1 zones. This percentage indicates the difference in housing quality (in terms of room availability) when transitioning from less urbanized areas (Degree 3) to highly urbanized zones (Degree 1).
Data Modeling: As the datasets are for 19 years from 2005 to 2023, we created two lag features and split the data into training and testing parts for each dataset to better fit the models, including Ridge, Lasso, Random Forest, Gradient Boosting, Ada Boost, and SVR. We used MSE, R2, and AIC to estimate each model and MSE as the determinator to choose the best model and plot the results. Then we also used RandomizedSearchCV to do Hyperparameter Tuning to better adjust the parameters to fit the models and choose the best one.


#Data Modeling Result:
With the ridge model, all three degrees’ datasets fit the best. The three test data all have:
MSE (mean squared error) of around 0.003
R2-value of about 0.98
AIC (Akaike Information Criterion) of about -750
The ridge model fits the datasets well and is not overfitting.



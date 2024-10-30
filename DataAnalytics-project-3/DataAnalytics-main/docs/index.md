## Research Question

Does the degree of urbanization significantly impact housing quality in terms of rooms per inhabitant?

## Methodology

To explore this question, a univariate analysis was conducted to examine the percentage change in the average number of rooms per person when moving from areas with the lowest degree of urbanization (Degree 3) to those with the highest degree (Degree 1) in European countries.

The analysis involved several key steps:

Data Collection:
Data on the average number of rooms per person by degree of urbanization (from 2003 to 2023) was sourced from Eurostat ([link](https://ec.europa.eu/eurostat/en/](https://example.com/))). This dataset provided information categorized by both country and degree of urbanization.

Data Preparation:
Since the original file had multiple parameters per row (both degree of urbanization and country), it was not directly usable. To resolve this, we split the data into three distinct datasets: deg1, deg2, and deg3, corresponding to the average number of rooms per person in areas of urbanization degrees 1, 2, and 3, respectively.
Data cleaning involved removing rows corresponding to groups of countries (e.g., "EU27" or regional clusters), focusing only on individual countries.
Given that there were minimal fluctuations in the data over time, we calculated an average value across the period from 2003 to 2023 to represent each country’s housing conditions for each degree of urbanization.
Calculation of Percentage Change:
For each country, we computed the percentage change in the average number of rooms per person between Degree 3 and Degree 1 zones. This percentage indicates the difference in housing quality (in terms of room availability) when transitioning from less urbanized areas (Degree 3) to highly urbanized zones (Degree 1).

Data Modeling:
As the datasets are for 19 years from 2005 to 2023, we created two lag features and split the data into training and testing parts for each dataset to better fit the models, including Ridge, Lasso, Random Forest, Gradient Boosting, Ada Boost, and SVR. We used MSE, R2, and AIC to estimate each model and MSE as the determinator to choose the best model and plot the results. Then we also used RandomizedSearchCV to do Hyperparameter Tuning to better adjust the parameters to fit the models and choose the best one.


## Visualizations
The following visualizations were created to illustrate the results:

- Average number of rooms per person from 2003 to 2023 for degree 1 urbanization by country

- Average number of rooms per person from 2003 to 2023 for degree 2 urbanization by country

- Average number of rooms per person from 2003 to 2023 for degree 3 urbanization by country

- Percentage change in the average number of rooms per person when moving from a degree 3 urbanization zone to a degree 1 zone (i.e., from the least urbanized to the most urbanized area)**




## Definitions

 - First-degree urbanization zone refers to highly urbanized areas, typically city centers and large metropolitan zones. These areas are characterized by dense population, intense economic activity, and significant infrastructure development.
For a first-degree urbanization zone, the population density is generally over 5,000 inhabitants per square kilometer, representing the most urbanized spaces with concentrated residential, commercial, and industrial activities.
   
 - Second-degree urbanization zone : refers to areas that are less densely populated than major city centers but still urbanized, such as suburbs or small cities. The population density in these areas is generally lower than in high-density urban centers.
For a second-degree urbanization zone, the population density is typically between 1,000 and 10,000 inhabitants per square kilometer, depending on the specific region.
   
 - Third-degree urbanization zone: refers to areas with lower urban density, often including small towns, peri-urban zones, or semi-rural areas. These zones are less urbanized than city centers and suburban areas, typically serving as transitional spaces between urban and rural areas.
For a third-degree urbanization zone, the population density is generally between 300 and 1,000 inhabitants per square kilometer, depending on the specific region.:



## Key Findings by Region:

- Western and Northern Europe:

Countries like Sweden, Norway, and the United Kingdom show a significant reduction in the number of rooms per person in highly urbanized areas compared to rural zones. In these regions, urban centers are characterized by compact living spaces due to high demand for housing, limited space, and high property costs.
These countries often have well-developed rural housing systems, which explains the stark contrast between urban and rural housing densities.

- Southern Europe:
  
Spain, Italy, and Greece also demonstrate a considerable decrease in room availability in urban centers, although the contrast is not as pronounced as in Northern Europe. Urban areas in Southern Europe often have historically dense housing, where space per person is traditionally lower due to older, narrower urban layouts.
However, rural zones in Southern Europe tend to offer more spacious living, possibly due to family-oriented housing in suburban or peri-urban areas, contributing to a relatively large contrast with urban centers.

- Eastern Europe:

Poland, Hungary, and Romania present a unique case where the change in rooms per person across urbanization levels is less pronounced. This may be due to post-socialist housing structures that emphasize more uniform housing across regions, with less variation between urban and rural living spaces.
In some Eastern European countries, rural areas may also have limited housing quality or infrastructure, which narrows the difference with urban housing density.

- Outliers and Anomalies:

Poland and Czech Republic show unexpected trends, with minimal reduction or even a slight increase in the number of rooms per person when moving from rural to urban areas. This could be due to unique urban planning policies, lower overall urban density, or the development of larger living spaces in certain urban projects.
Finland also appears to have a smaller percentage change, potentially due to a more balanced urban-rural housing policy, aiming to maintain similar living standards across both urban and rural zones.

- Implications of the Findings:
  
The findings highlight that, while urbanization often leads to denser living conditions and fewer rooms per person in European urban centers, the extent of this effect varies widely. Factors such as housing policy, urban planning approaches, economic status, and historical development patterns significantly influence housing density.



## Data Modeling Result:

With the ridge model, all three degrees’ datasets fit the best.
The three test data all have:

- MSE (mean squared error) of around 0.003
    
- R2-value of about 0.98
      
- AIC (Akaike Information Criterion) of about -750
        
The ridge model fits the datasets well and is not overfitting.



## Data

This project uses data from one source:

[https://ec.europa.eu/eurostat/en/](https://example.com/)

## Additional Information

This is the final project for the module Introduction to Data Analytics in Business of the Frankfurt School of Finance & Management. 

### Lecturer:

Prof. Dr. Lucas Böttcher

### Group:

Julie Fasquelle

Jingke Yang

Mengdi Tan


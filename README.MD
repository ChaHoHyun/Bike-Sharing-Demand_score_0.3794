# Bike Sharing Demand

## Predict demand of bike by Machine Learing

<img src="https://storage.googleapis.com/kaggle-competitions/kaggle/3948/media/bikes.png" alt="Random Search for Hyper-Parameter Optimization" style="width: 720px;"/>

<p style="text-align: center;">
  <small>
    [See <a href="https://www.kaggle.com/c/bike-sharing-demand/overview">Bike Sharing Demand (Kaggle URL)</a>]
  </small>
</p>

## Introduction

<br>

### Object

<br>

See, fork, and run a **random forest** benchmark model through Kaggle Scripts

- Period of bike rental data : 2 years
- train dataset : 19 days(1st ~ 19th) each month
- test dataset : about 10 days(20th ~ last) each month

We must predict the total count of bikes rented during 2 years for each month, hour.

<br>

### Data Fields from Capital Bikeshare(Bike-sharing Startup in Wachington D.C)

<br>

- datetime - hourly date + timestamp (Year + Month + Day + Hour + Minutes + Seconds)
- season - 1 = spring, 2 = summer, 3 = fall, 4 = winter
- holiday - whether the day is considered a holiday
- workingday - whether the day is neither a weekend nor holiday
  (If it is not holiday or workingday, it will be **weekend**)
- weather

  - 1: Clear, Few clouds, Partly cloudy, Partly cloudy

  - 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist

  - 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds

  - 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog

- temp - temperature in Celsius
- atemp - "feels like" temperature in Celsius
- humidity - relative humidity
- windspeed - wind speed
- **casual** - number of non-registered user rentals initiated
- **registered** - number of registered user rentals initiated
- **count** - number of total rentals (casual + registered)

$$ casual + registered = count $$

<br>

### Evaluation

<br>

Submissions are evaluated one the Root Mean Squared Logarithmic Error (**RMSLE**). The RMSLE is calculated as

<br>

$$ RMSLE = \sqrt {\frac{1}{n}\sum\limits\_{i=1}^n(log(p_i+1) - log(a_i + 1))^2} $$

### Precedure

There will be follow steps for how to solve this problem. [[See link]](https://github.com/ChaHoHyun/Bike-Sharing-Demand_score_0.3794/blob/main/Bike%20Sharing%20Demand_registered_Score_.ipynb)

1. Import CSV file by using Pandas (Collecting Data)
2. Exploratory Data Analysis (EDA)

   - Correlation Analysis
   - Preprocessing

     Bike Sharing Demand conveniently has most of the data preprocessing like "season, holiday, workingday, weather" column. (Contrary to Titanic)

3. Explore (Visualization)

   After preprocessing, explore and visualize the data.
   Suggest some of ideas for improving ML performance.

4. Training (For Machine Learing - Random Forest)

5. Selection feature for optimizing ML perfomance (Statistical Hypothesis Test)

6. Conclusion

   With this, we learned how to reach the top of the bike sharing demand competition, which is the goal of this class (**134th/3251, top 4.12%**). Kaggle is a credible data science contest, and if we are in the top 5%, you can say that you are one of the best data scientists working in the field. Usually, senior data scientists are ranked in the top 5%

   you can improve the performance of your machine learning model from a different perspective. For example, it is a good idea to look at the various options of the machine learning algorithm we used (RandomForestRegressor and fix it), or to apply a new machine learning algorithm (for those who are interested in a new machine learning algorithm, Gradient Boosting or XGBoost Take a look at my LightGBM.

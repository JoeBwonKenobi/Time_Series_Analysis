# **Time Series Analysis and Forecasting**
 
 ![image](https://github.com/JoeBwonKenobi/Time_Series_Analysis/assets/117705408/0eec7c23-f5e6-4125-966c-26d384b2dc43)

 
# **Project Overview:**

This Project uses time series analysis and forecasting  with Python to make predictions for furniture sales data.

# **Data Source:**

https://community.tableau.com/s/question/0D54T00000CWeX8SAL/sample-superstore-sales-excelxls

# **Methods:**
- For this project, I used time-series decomposition which is used to analyze a set of data that changes over time.
- Specifically, this method helps to separate out three different patterns in the data: trends, seasonality, and noise.
- Trends refer to long-term changes in the data, such as an overall increase or decrease over time. 
- Seasonality refers to patterns that repeat at regular intervals, such as a yearly cycle of sales increasing during the holiday season. 
- Noise refers to random fluctuations in the data that are unrelated to any underlying pattern.
- By separating out these three components, the method can help us better understand how the data is changing over time and make predictions about its future behavior.
- Additionally, visualizing these components can help us see the patterns more clearly and identify any unusual or unexpected changes in the data.
- I chose to use Prophet because it has the advanced capability for modeling the effects of holidays on a time-series model.

# **Visualizing Furniture Sales Time Series Data**

![image](https://user-images.githubusercontent.com/117705408/234460308-7919ebd8-aa40-4ef1-821e-db1da4b5e00c.png)

- This plot shows the sales for furniture in a four year period of time (2014-2018)

# **Visualization of the Time series decomposition**

- Using this method, (Time-series decomposition)I can visualize the trends, seasonality, and noise within the data set.

![image](https://user-images.githubusercontent.com/117705408/234460931-882bb066-20da-4f7c-ace9-c80f1e7103c4.png)

- The plot above clearly shows that the sales of furniture is unstable, along with its obvious seasonality. 

# **ARIMA Model**

- This ARIMA Model (Autoregressive Integrated Moving Average) is denoted with the notation for parameters that account for seasonality, trends, and the noise in the data.
- I used GridSearchCV to find the optimal set of parameters that yeilded the best possible performance of the model.
- I then fit and ran diagnostics on the models performance to investigate any unusual behavior, the visualization of the diagnostics are provided below:

![image](https://user-images.githubusercontent.com/117705408/234462414-62f0f2f5-4bee-4db2-9bcf-4baf31c759e3.png)

- The model is not perfect, but when i ran the diagnostics test, the errors it made seemed to be spread out in a way that's similar to how we expect them to be(normal distibution).

# **Validating Forecasts**

- To understand the accuracy of the forecasts, I compared predicted sales to real sales of the time series, and set forecasts to start at 2017–01–01 to the end of the data.
- This line plot is showing the observed values compared to the rolling forecast predictions:

![image](https://user-images.githubusercontent.com/117705408/234463108-a93cae9b-227c-45b5-a502-8fbf617b000e.png)

- The predictions match the real results quite well as we can see above.
- It shows that things have been getting better since the start of the year, and also take into account how things usually change at different times of the year(seasonality trends).

# **Forecasting**

![image](https://user-images.githubusercontent.com/117705408/234463605-6e7c0942-1b56-4027-a1b1-09ed4ca523d7.png)

- This model accurately predicted when the furniture sales would increase or decrease during certain times of the year.
- However, the further into the future the model predicts, the less integrity it holds in terms of its predictions being accurate.
- The uncertainty is indicated by the range of values the model generates which grows larger the further into the future it makes predictions.

- The above analysis strikes curiosity about the compairson between patterns in furniture sales and office supply sales.

# **Time Series Analysis of Furniture Sales Vs. Office Supplies**

![image](https://user-images.githubusercontent.com/117705408/234464831-7d2d0309-6df3-4419-a5d6-f0de0eb17c9d.png)

- The furniture and office supplies sales have similar patterns throughout the year.
- At the beginning of the year , sales are usually slower for both.
- Sales for office supplies tend to look slower throughout the summer.
- On average, furniture sales make more money than office supplies, which makes sense because of the higher cost.
- There are days however, when office supplies sell more in a single day than furniture, and I want to discover when.

# **Time Series Modeling with Prophet**

- I chose to use Prophet because it has the advanced capability for modeling the effects of holidays on a time-series model.

# **Visualization of Furniture Sales**

![image](https://user-images.githubusercontent.com/117705408/234465948-5a04d0a1-1aed-4509-b5eb-609efddfaaf7.png)

# **Visualization of Office Supplies Sales**

![image](https://user-images.githubusercontent.com/117705408/234465972-9e1891f8-42aa-4175-aa9a-3fab5b08b96d.png)

# **Comparing Forecasts**

- As displayed above, I've created forecasts for three years for the two categories into the future.
- Now I will join the two together to compare the future forecasts.

# **Trend and Forecast Visualization**
 
![image](https://user-images.githubusercontent.com/117705408/234466262-4eb6bd5a-bc70-442e-93e6-843b651628e4.png)

# ** Trends and Patterns**
- Sales for both categories have been increasing linearly over time and will likely keep growing, although the office supplies growth seems slightly higher.

![image](https://user-images.githubusercontent.com/117705408/234466330-f53bc0bc-4eeb-4244-ac7f-388559c51476.png)

- The worst month for furniture is April, and the best looks like December. 

![image](https://user-images.githubusercontent.com/117705408/234466346-09b12ed5-1f70-4232-ad1a-03afb70a1550.png)

- The best month for office supplies is October, the the worst month for office supplies is February.

# **Recommendations:**

- The sales of furniture and office supplies have similar patterns throughout the year, with both experiencing slower sales at the beginning of the year and office supplies sales remaining slow throughout the summer.
- On average, furniture sales generate more revenue than office supplies sales, likely due to the higher cost of furniture.
- However, there are days when office supplies sell more in a single day than furniture, and identifying these days could help to increase revenue for the office supplies category.
- The worst month for furniture sales is April, while the best month is December. This may be due to increased sales during the holiday season.
- On the other hand, the best month for office supplies sales is October, while the worst month is February; this may be due to the timing of school semesters & tax season.
- The analysis also shows that the sales of furniture are unstable, but the predictions match the real results quite well. This suggests that while the sales may fluctuate, the seasonality patterns remain relatively consistent.

# **Limitations & Next Steps**

- As expected, I'm limited to the data provided, meaning that the predictions made have a certain limit in potentail for accuracy. 
- The next steps would be to obtain more recent data and compare the actual sales results to the predictions made.
- The valuable insights obtained can assist the sales team in effectively implementing appropriate changes to leverage the identified seasonality patterns and trends.

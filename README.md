# **Time Series Analysis and Forecasting**
 Time series analysis and forecasting with Python

# **Project Overview:**

This Project uses time series analysis and forecasting to make predictions for furniture sales data.

# **Visualizing Furniture Sales Time Series Data**

![image](https://user-images.githubusercontent.com/117705408/234460308-7919ebd8-aa40-4ef1-821e-db1da4b5e00c.png)

- This plot shows the sales for furniture in a four year period of time (2014-2018)

# **Visualization of the Time series decomposition**

- Using this method, I can visualize the trends, seasonality, and noise within the data set.

![image](https://user-images.githubusercontent.com/117705408/234460931-882bb066-20da-4f7c-ace9-c80f1e7103c4.png)

- The plot above clearly shows that the sales of furniture is unstable, along with its obvious seasonality. 

# **ARIMA Model**

- This ARIMA Model (Autoregressive Integrated Moving Average) is denoted with the notation for parameters that account for seasonality, trends, and the noise in the data.
- I used GridSearchCV to find the optimal set of parameters that yeilded the best possible performance of the model.
- I then fit and ran diagnostics on the models performance to investigate any unusual behavior, the visualization of the diagnostics are provided below:

![image](https://user-images.githubusercontent.com/117705408/234462414-62f0f2f5-4bee-4db2-9bcf-4baf31c759e3.png)

- The model is not perfect, but when i ran the diagnostics test, the errors it made seemed to be spread out in a way that's similar to how we expect them to be(normal distibution).

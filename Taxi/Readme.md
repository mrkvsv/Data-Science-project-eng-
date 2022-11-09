# Forecasting taxi orders

The taxi company has collected historical data on taxi bookings at airports. To attract more drivers during the peak period, you need to predict the number of taxi orders for the next hour. It is necessary to build a model for such a prediction.

**Task** - predict the number of taxi orders for the next hour.

**Stack:** `pandas` `matplotlib` `CatBoost` `Prophet`

### Conclusion

We have analyzed a time series containing information about the number of taxi orders. An upward trend was revealed for an increase in the number of orders for the given period (from 03/01/2018 to 08/31/2018) and daily seasonality.
Prepared data for building a model, added features: day of the week, hour, remaining values ​​and moving average.
Several machine learning models were tested, the best one was chosen, which was LightGBM with hyperparameters: max_depth' = 4, 'num_leaves' = 40, 'reg_alpha' = 0, and tested on a test set, showing an RMSE value of 42.03.

Thus, the goal of the project (to predict the number of taxi orders for the next hour) has been achieved.

# Energy consumption forecasting

## Context
This notebook was created for a project for a class called "Energy Planning", taken during my graduation in energy engineering. The idea behind it is to forecast the hourly energy consumption for a week of the south-eastern region subsystem, based on the ONS (Operador do Sistema Nacional) division. 

## What to expect
The forecasting is made through a multivariable linear system, which uses climate data (temperature and solar radiation) from major cities of the region, the biggest one in the brazilian electrical system, in terms of infrastructure, loads, and generation. The objective of the notebook, as said, was to comply with the project's requirements, so there's a LOT of room for improvement. 

As it is, the present model is clearly overfitted for the training data. In fact, when the notebook was done (second semester of 2022), I had little to none understanding of this type of modelling, so there isn't a separation between training, test and validation datasets. Nonetheless, it was a really good opportunity to apply and learn more about forecasting and ML modelling.

In the notebook, there is more than one working model. However, the more complex, the more overfitted, e.g., an hourly model for each day of the week had amazing results for the training data, but poor performance when forecasting the consumption. The model that was used in the project is an hourly model applied for week days (monday to friday) and weekends, with a "shift speration" (morning, afternoon, night). The final model was reached empirically, tweaking the parameters on the go while checking the model's accuracy with the training data and while forecasting.

# Linear Regression Model - Air Quality (CO Prediction)

## Data

We use the **Air Quality UCI** dataset (see UCI ML Repository). It has hourly sensor readings: gas concentrations (e.g. CO, NOx, NO2), temperature (T), relative humidity (RH), and absolute humidity (AH). The file is semicolon-separated with comma as decimal. Missing values are coded as -200; we replace them with NaN and drop those rows. We also drop the two empty columns at the end.

## What We Did

1. **Load** -> Read the CSV with sep=';' and decimal=',' so columns and numbers are correct.
2. **Clean** -> Dropped empty columns and replaced -200 with NaN, then dropped rows with any NaN.
3. **Target and features** -> We predict CO(GT) from the other numeric columns (sensors and T, RH, AH). We skip Date and Time.
4. **Split** -> 80% for training, 20% for testing (same idea as the SMS model).
5. **Fit** -> Trained a linear regression model on the training data.
6. **Evaluate** -> R² on the test set. We also plotted actual vs predicted CO (dots = real vs predicted; red line = perfect predictions) and a residuals plot.

## Results

The model’s R² on the test set shows how much of the variation in CO it explains. In the actual vs predicted plot, points close to the red line mean good predictions; points far from the line are bigger errors. The residuals plot shows errors scattered around zero when the model is reasonable.
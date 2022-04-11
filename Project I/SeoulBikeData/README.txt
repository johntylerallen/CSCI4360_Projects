SeoulBikeData.csv: raw data file from UCI: (https://archive.ics.uci.edu/ml/datasets/Seoul+Bike+Sharing+Demand)

Bikes.csv: cleaned data file of SeoulBikeData.csv, removes "Date" ("Hour" subsitutes the date)
and "Functioning Day" (constant).
Adds 1 to: "Hour", "Solar Radiation (MJ/m2), "Rainfall(mm)", and "Snowfall (cm)" to allow for proper model runs
Changes values in "Season": 'Winter':1, 'Spring':2, 'Summer':3, 'Autumn':
Changes values in "Holiday": 'No': 1, 'Yes':2

Features in Bikes.csv:
"Hour","Temperature", "Humidity","Wind Speed","Visibility","Dew Point Temp","Solar Radiation", "Rainfall","Snowfall", "Seasons","Holiday"
Response Variable: "Bikes Rented"

SeoulBikeData_py.py:
- ENSURE FILE 'SeoulBikeData.csv' IS IN SAME DIRECTORY AS 'SeoulBikeData_py.ipyn'
- The start of file makes the changes noted in Bikes.csv
- Contains python code for the following models:
	Linear Regression, Lasso, Ridge, Quadratic, (sklearn)
	and Symbolic (gplearn).
- For each model, three types of feature selection were used:
	Forward, Backward and Recursive (from sklearn)
- Outputs R2 Adjusted and R2 CV for each model and each feature 
  selection

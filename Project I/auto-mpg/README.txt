auto-mpg.DATA: raw data file obtained from UCI (https://archive.ics.uci.edu/ml/datasets/auto+mpg)

auto-mpg-clean.csv: contains no header row and removes row with missing data
and removes the "model name" column

Features:
"cylinders","displacement","horsepower","weight","accleartion",
"model year","origin", "mpg"
"mpg" is the response variable

auto-mpg_py.py: 
- ENSURE FILE 'auto-mpg.csv' IS IN SAME DIRECTORY AS 'auto-mpg-py.ipyn'
- The start of file removes missing rows from auto-mpg.csv
- Contains python code for the following models:
	Linear Regression, Lasso, Ridge, Quadratic, (sklearn)
	and Symbolic (gplearn).
-For each model, three types of feature selection were used:
	Forward, Backward and Recursive (from sklearn)
- Outputs R2 Adjusted and R2 CV for each model and each feature 
  selection

# Project 2020 Fundamentals of Data Analysis - <br>Linear Regression

The following Project concerns data analysis in Python

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install numpy, matplotlib, pandas and seaborn.

```bash
pip install matplotlib
pip install pandas
pip install seaborn
```
## Project Objective:
In this project we must perform and explain simple linear regression using Python on the<br> powerproduction dataset available on Moodle

## Project Scope:
The goal is to accurately predict
wind turbine power output from wind speed values using the <br>data set as a basis.
Your submission must be in the form of a git repository containing, at a <br>minimum, the
following items:
1. Jupyter notebook.
2. Explanation of your regression and an analysis.
3. Standard items in a git repository such as a README.


## Implementing Simple Linear Regression Algorithm

```
def LinearRegression(train_x, train_y):
    X = train_x
    Y = train_y
    N = len(X)
    
    X_mean = X.mean()
    Y_mean = Y.mean()
    
    SumofXY = (X * Y).sum()
    SumofX  = X.sum()
    SumofY  = Y.sum()
    
    SumofXX = (X*X).sum()
    SquareofSumofX = (SumofX * SumofX)
    
    b =((N * SumofXY) - (SumofX * SumofY)) / ((N * SumofXX) - SquareofSumofX)
    
    a = Y_mean - b * X_mean
    
    return a, b
```

### Evaluation of Model


> 1. Best fitted regression line
> 2. Actual vs Predicted bar plot


## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
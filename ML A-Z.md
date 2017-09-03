#Notes

## 1. Essential libraries for data preprocessing
### For python, 3 essential libraries for data preprocessing
```
import numpy as np
import matplotlib.pyplot as plt
import pandas as pd
```
- numpy contains mathematical tools
- pyplot is sub library to matplotlib, and is used to plot charts
- pandas, best to import datasets and manage dataset

### For R, default libraries will do

##2. Matrix of features VS Dependent variable vector
Matrix of features, aka, matrix of independent variables

##3. When missing data in datasets
Usually, use mean value of the column of the missing data  
  
### Here are some templates for further use
- with python
```
from sklearn.preprocessing import Imputer
imputer = Imputer(missing_values = 'NaN', strategy='mean', axis=0)
imputer = imputer.fit(x[:,1:3])
x[:,1:3] = imputer.transform(x[:,1:3])
```
- with R
```
dataset$Age = ifelse(is.na(dataset$Age),
                     ave(dataset$Age, FUN = function(x) mean(x, na.rm = TRUE)), 
                     dataset$Age)
dataset$Salary = ifelse(is.na(dataset$Salary),
                     ave(dataset$Salary, FUN = function(x) mean(x, na.rm = TRUE)), 
                     dataset$Salary)
```
## 4. Encode categorical data



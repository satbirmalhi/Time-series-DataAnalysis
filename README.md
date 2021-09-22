# Time Series DataAnalysis 
>keep similing while writting codes
>Description: In this project, we will study the use of statistical models and methods for
analyzing time-series data and their applications such as stock market prediction, monthly
unemployment figures, quarterly crime rates, and annual birth rates, etc. The main focus of this
project is on the understanding of the fundamental concepts of time series modeling. The
following models will be the main center of our research: stationary and nonstationary,
nonseasonal and seasonal, intervention and outlier, transfer function, regression time series,
and vector time series models. We will also implement these models in forecasting and
inference of the real world’s problems. We are also planning to prepare a series of students’
presentations to promote applied mathematical concepts such as a differential equation and
Fourier Analysis in data science across the campus.
------------------------------
# Table of contents
1. [Framework](#infrastructure)
2. [Data importation](#Data-importation)
    1. [Web scraping](#Web-scraping)
3. [Linear Regression](#Linear-Regression)

------------------------------------------------------------------
## Framework <a name="infrastructure"></a>

### How to write README.md 
* Using Markdow [Cheat](https://www.markdownguide.org/cheat-sheet/)
-------------------------------------------------------------------

### The Collaboration Setup for the project
* Setup Brew: [Brew](https://brew.sh/)
* Setup oh my zsh: [Zsh](https://www.freecodecamp.org/news/how-to-configure-your-macos-terminal-with-zsh-like-a-pro-c0ab3f3c1156/)
* Setup git and github:[git](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup)
    * git [cheatsheet](https://education.github.com/git-cheat-sheet-education.pdf)

----------------------------------------------------------------------------------
### [Install Virtual Environment](https://virtualenv.pypa.io/en/latest/installation.html)
* Install:  brew and update it
* `pip3  install virtualenv`
* Check all the package in your global machine: `pip3 list` 
* Check: `virtualenv --version` 
* `virtualenv -p python3.9 <name_of_virtualenv>`
* Activate: `source ./<name_of_virtualenv>/bin/activate`
* Check which python is active: `which python `
* Deactivate when switch to another the application: `deactivate`
* To install new packages: `pip install <name of the package>`
* Copy local packages to requirements.txt: `pip freeze --local > requirements.txt`
* Check: `cat requirements.txt`
* git push requirement.txt to github
* To get all the package in your virtualenv: `pip install -r requirements.txt`

#### Python Libraries:
    import pandas as pd
    import pandas_datareader.data as web
    from datetime import datetime, timedelta
    import matplotlib.pyplot as plt
    import numpy as np


---------------------------------------------------------------------
## Data importation<a name="Data-importation"></a>

### Task 1: Data Management
#### 1. How to download data from the internet: 
1. Using Quandl
    1. `import quandl,math, datetime`
    2. `quandl.ApiConfig.api_key = "Token`
    3. `df=quandl.get("WIKI/GOOGL")`

2. *Using DataReader*
    1. `df = web.DataReader('<ticker>', 'yahoo', start=start_date, end=end_date)`

#### 2. How to print/show the data in jupyternotebok?
1. `df.head()`
2. `print(d)`
#### 3. [How to how to save the data on your local machine in csv file?](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_csv.html)
1. `df.to_csv('Name_file.csv')`
#### 4. [How to how to read the data from your local machine of csv file?](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.read_csv.html)
1. `pd.read_csv('Name_file.csv', index_col=0)`
#### 5. How to clean the data ?
1. Remvoning NAN values?
2. Removing strings values?
#### 5. How to plot the data ?


#### 6. Find a best way to visualize this data set ?


## [Linear Regression with python](https://www.kdnuggets.com/2019/03/beginners-guide-linear-regression-python-scikit-learn.html)<a name="Linear-Regression"></a>

* Convert date into numnerical values:
```  y = np.asarray(data_df['<yvalue>'])
    X = df[['date']]
    X_train, X_test, y_train, y_test = train_test_split             
    (X,y,train_size=.7,random_state=42)
    model = LinearRegression() #create linear regression object
    model.fit(X_train, y_train) #train model on train data
    model.score(X_train, y_train)
```
-------





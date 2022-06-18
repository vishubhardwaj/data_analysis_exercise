# data_analysis_exercise

## Tasks

1. Calculate the share of expenditure on school education incurred by various departments/ministries. 
2. Estimate the share of capital expenditure.
3. Using projected population for each of the years under consideration, estimate the per-capita expenditure on school education in the state, and each district. 
4. Rank the districts based on utilization of allotted funds of revenue expenditure and capital expenditure (separately).

### Initial Data processing and getting data ready
**function** : initial_process(arr):
```
    """
    This function fills NaN values with 0.0 and adds two new columns at the end of dataframe :
    1. Overall Expenditure : one value instead of three different columns
    2. Excess : Surplus left after expenditure

    It takes in a list of dataframes, single dataframes can be passed as a single item list.

    It'll return a new arrey (list) of all Dataframes now processed.
    """
```

### Calculate the share of expenditure on school education incurred by various departments/ministries
**function** : school_edu_Exp(arr):
```
    """
    This function takes in the list of dataframes and filters and sorts
    values based on classification of school education departments.

    It'll return a new arrey (list) of all Dataframes now processed.
    """
```

Assumption : Find the names of all educational departments and select the school education deaprtments.

education departments : शिक्षा विभाग (प्राथमिक शिक्षा), शिक्षा विभाग (माध्यमिक शिक्षा), शिक्षा विभाग (उच्च शिक्षा), शिक्षा विभाग(राज्य शैक्षिक अनुसंधान एवं प्रशिक्षण परिषद्), व्यावसायिक शिक्षा विभाग, प्राविधिक शिक्षा विभाग, चिकित्सा विभाग (चिकित्सा, शिक्षा एवं प्रशिक्षण)

school education departments : शिक्षा विभाग (प्राथमिक शिक्षा), शिक्षा विभाग (माध्यमिक शिक्षा), शिक्षा विभाग (उच्च शिक्षा)

Process followed:
1. Decided on the values to filter out (school education departments)
2. Filtered the joined dataframe of all years according to decided values
3. Sorted the resulting dataframe State name wise.
4. Saved the resulting dataframe in `./output/task1 (fical-year).csv`
5. Results:
    ```
    State saved -1.12 % of fund in 2017-2018
    State saved -1.53 % of fund in 2018-2019
    State saved -0.32 % of fund in 2019-2020
    State saved 5.33 % of fund in 2020-2021

### Estimate the share of capital expenditure.
**function** : CapEx_filter
```
"""
    This function takes in the list of dataframes and filters and sorts
    values based on if the scheme code begins with a 4 or above.

    It'll return a new arrey (list) of all Dataframes now processed.
    """
```
Assumption : Scheme codes starting with 4 and above denote capital expenditure

Process followed:
1. Get data to be filtered according to scheme code.
2. filter the joined dataframe with regex for capital expenditure (initiating with 4 or above).
3. Sort State name wise.
4. Saved the resulting dataframe in `./output/task2 (fiscal-year).csv`
5. Results: 
```
    State capital expenditure is 24.32 % in (2017-2018)
    State capital expenditure is 2.12 % in (2018-2019)
    State capital expenditure is 0.0 % in (2019-2020)
    State capital expenditure is -16.34 % in (2020-2021)
```

### the per-capita expenditure on school education in the state

Process folowed:
1. Population data was taken from : https://www.census2011.co.in/census/state/uttar+pradesh.html
2. Total expenditure of the year divided by total projected population of that year.
```
per capita expenditure in 2017-18 : 5104.66
per capita expenditure in 2018-19 : 4638.78
per capita expenditure in 2019-20 : 4049.9
per capita expenditure in 2020-21 : 3895.74
```

### Rank the districts based on utilization of allotted funds of revenue expenditure and capital expenditure (separately).
**function** : ranked_districts
```
"""
    This function takes arrey of Dataframes and sorts each data frame according 
    to custom column added initially "excess". The logic is to sort districts based
    on which districts still have excess fund left after expenditure.
"""
```
Saved the resulting dataframe in `./output/task4.a(fiscal-year).csv` & `./output/task4.b(fiscal-year).csv` respectively.

# data_analysis_exercise

## Tasks

1. Calculate the share of expenditure on school education incurred by various departments/ministries. 
2. Estimate the share of capital expenditure.
3. Using projected population for each of the years under consideration, estimate the per-capita expenditure on school education in the state, and each district. 
4. Rank the districts based on utilization of allotted funds of revenue expenditure and capital expenditure (separately).

### Calculate the share of expenditure on school education incurred by various departments/ministries. 

Assumption : Find the names of all educational departments and select the school education deaprtments.

education departments : शिक्षा विभाग (प्राथमिक शिक्षा), शिक्षा विभाग (माध्यमिक शिक्षा), शिक्षा विभाग (उच्च शिक्षा), शिक्षा विभाग(राज्य शैक्षिक अनुसंधान एवं प्रशिक्षण परिषद्), व्यावसायिक शिक्षा विभाग, प्राविधिक शिक्षा विभाग, चिकित्सा विभाग (चिकित्सा, शिक्षा एवं प्रशिक्षण)

school education departments : शिक्षा विभाग (प्राथमिक शिक्षा), शिक्षा विभाग (माध्यमिक शिक्षा), शिक्षा विभाग (उच्च शिक्षा)

Process followed:
1. Decided on the values to filter out (school education departments)
2. Filtered the joined dataframe of all years according to decided values
3. Sorted the resulting dataframe State name wise.
4. Saved the resulting dataframe in `./output/task1.csv`

### Estimate the share of capital expenditure.
Assumption : Scheme codes starting with 4 and above denote capital expenditure

Process followed:
1. Get data to be filtered according to scheme code.
2. filter the joined dataframe with regex for capital expenditure (initiating with 4 or above).
3. Sort State name wise.
4. Saved the resulting dataframe in `./output/task2.csv`

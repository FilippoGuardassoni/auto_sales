![](https://github.com/FilippoGuardassoni/auto_sales/blob/main/img/headerheader.webp)

## Auto Car Sales Demand, Prices and Income: A Statistical Study Using Functional Data Analysis and Time Series.

![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/pragyy/datascience-readme-template?include_prereleases)
![GitHub last commit](https://img.shields.io/github/last-commit/FilippoGuardassoni/spotify_hitsong)
![GitHub pull requests](https://img.shields.io/github/issues-pr/FilippoGuardassoni/spotify_hitsong)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![contributors](https://img.shields.io/github/contributors/FilippoGuardassoni/spotify_hitsong) 
![codesize](https://img.shields.io/github/languages/code-size/FilippoGuardassoni/spotify_hitsong)

# Project Overview

The automobile industry has a fundamental impact on the economic activity in United States and world. The global automotive industry is estimated to grow to just under 9 trillion dollars by 2030 and new vehicle sales will account for 38% of this value. Acknowledging the fact that US automotive market is one of the largest in the world, in this paper we will explore the US market characteristics focusing on the demand with other explanatory variables.
Previous studies had been conducted using the different models and variables, however some of them used non recent time periods. The purpose of this study is to investigate key aspects of the US automobile market and give a pretext for more exhaustive studies of recent issues. Our main objective is to understand the relationship between the car prices and the consumers’ disposable income through the estimation of the new cars demand. This is done using monthly data from 2005 to 2020 and developing a time series Vector Error Correction Model.
In our study we have used lagged explanatory variables to define a demand function for the new auto sales and the long-run relationship between them. Average auto price emerged as not an important factor for the shift in the demand function (as many previous studies depict) and the disposable income is proportionally related to the demand.
From our model, price elasticity is greater than 1, meaning the reaction of the demand is relatively sensitive to the changes in price.
Our main premise is that the price growth rate is greater than the disposable income growth rate, and this would lead to a decrease in the demand. Even if the price is not significant in our model, further research should be conducted in order to better predict the demand, to understand the relationship between price and income, and to investigate the role of interest rates and loans in the automobile industry.

# Installation and Setup

- Stata

# Data
Data is collected in the form of Time Series at US state level from Federal Reserve Bank of St. Louis (which organize and clean the data from Bureau of Statistic & Transportation) monthly from year 1967 to 2020.

## Source Data & Data Acquisition
### Sales
The variables collected are following:
• Domestic Auto Sales
• Foreign Auto Sales
• Domestic Light Truck Sales
• Foreign Light Truck Sales

### Average Auto Price, Disposable Income & Unemployment Rate
We collected the average auto price, disposable income and unemployment rate from the Bureau of statistics. Regarding the Average Auto Price variable, we were able to retrieve only annual data. In order to continue with analysis, we assumed that the price when an auto is launched in the market remain constant through the years given adjustment for inflation. Therefore, the average annual average auto price coincides with the monthly average auto price in that particular year

### Indexes
We collected the data as:
• Durable goods consumer price index (acpi)
• Automobile & Light Trucks Producer Price Index(appi)
• Public Transportation Price Index(ptcpi)
• Motor Vehicle Insurance Price Index(mvicpi)

# Project structure

```bash
├── dataset
│   ├── car data               
│   │   ├── Annual-LightVehicle-Sales.csv
│   │   ├── Annual-US-Domestic-Production.csv
│   │   ├── Domestic Auto Sales.csv
│   │   ├── Domestic Light Truck Sales.csv
│   │   ├── Foreign Auto Sales.csv
│   │   ├── Foreign Light Truck Sales.csv
│   │   ├── LightVehicle-Sales.csv
│   │   ├── Passenger Miles.csv
│   │   ├── Passenger Miles.xlsx
│   │   ├── US-Domestic-Production.csv
│   │   ├── statistic_id193007_vehicle-miles-traveled-in-the-us---cars-1975-2018.xlsx
│   │   ├── upload-to-stata.csv
│   ├── gasoline price           
│   │   ├── gasoline price.csv
│   │   ├── gasolineprice monthly.csv
│   ├── income   
│   │   ├── Income United States .csv
│   │   ├── disposable income monthly.csv
│   │   ├── disposable income per capita.csv
│   ├── loan data
│   │   ├── Auto finance companies  loans to value ratio.csv
│   │   ├── Average Amount Financed for new car loans .csv
│   │   ├── Average Finance Rate of New Car Loans at Finance Companies.csv
│   │   ├── Average Maturity of New Car Loans at Finance Companies.csv
│   │   ├── Loan-To-Value Ratio of New Car Loans at Auto Finance Companies.csv
│   │   ├── amount financed loan rates and maturity.csv
│   ├── population      
│   │   ├── population and disposable income.csv
│   │   ├── population and income united states.csv
│   │   ├── population.csv
│   │   ├── population.xlsx
│   ├── unemployment rate  
│   │   ├── umemployment rate monthly.csv
│   │   ├── unemployment rate.csv             
├── stata code
│   ├── stata_code.do                
├── report
│   ├── auto_sales_report.pdf   
├── img
│   ├── headerheader.jpg        
├── LICENSE
├── README.md
└── .gitattributes,
```

# Results and evaluation
The aim of this paper is to create a model for the demand of new cars in the automotive market in the US and to lay the foundation for future studies.
The analysis conducted investigated the relationship between the new auto sales and a set of explanatory variables such as the income of consumers, the gasoline price, and the prices of public transportation and insurance. The developed model respects the Law of Demand and Supply, since the findings suggest that the increase in prices reduce total sales of cars while the rise in income fosters total sales. The achieved results regarding the demand meet the expectations, however, the price elasticities in the short and in the long run are opposite to what past studies predicted.
Besides having studied in depth the descripted relationship, this analysis allowed us to make inferences regarding the market landscape. In particular, we considered potential reasons behind the increase in car prices, the role of loans and interest rates as a mean used by the families to be able to afford new cars as well as a differentiated source of profit for car manufacturers, and possible policy concerns of the government related to the environment.
In conclusion, the study of the automobile demand is fundamental in order to raise policy makers awareness in the issue of new regulations. In fact, they could not only jeopardize the efficiency of other regulations, but also trigger phenomena potentially dangerous for one of the biggest industries in the world which is the automotive as well as for the whole economy.


# Future work
The main limitations of our study are two: 1) The construction of the average of car and light trucks price variable and 2) the magnitude of our model. We were able to gather data only for annual average prices of car and light trucks. In order to proceed with our research, we made the strong assumption that monthly average auto prices would be equal to Annual Average divided by No. of Months. The fundamental difficulty in deriving a price variable for the model is that "the actual sales price or transactions price" between the auto dealer and the consumer is an unknown figure. While actual sales prices exist in the files of state revenue offices, the costs of extracting this information make it virtually inaccessible. We would recommend building a price function in order to correctly estimate the monthly average auto prices.
An ideal Demand function would include a series of variables that need to be calculated that we omitted. For example, used car and automobile stock variables are needed to capture the alternatives for the consumers. In addition, a dummy for the ownership of a vehicle would help to estimate the choice of delaying the purchase of a new car. We performed a rudimental analysis considering the general landscape of the auto market in U.S; an improved version should divide the sales into brands and category of vehicles at the state level. Moreover, one can consider also categorical variables such as colour and size. Another strong limitation of our model was the use of indexes instead of actual values; ideally, functions to capture the trends in those variables should be created. The best method to do so is to conduct surveys. Lastly, to be more accurate, discretionary income, which is the money that an individual or a family has to invest, save, or spend after taxes and necessities are paid, would be a better variable to predict the sales trend.

# Acknowledgments/References
See report/song_hit_prediction.pdf for references.

# License
For this github repository, the License used is [MIT License](https://opensource.org/license/mit/).

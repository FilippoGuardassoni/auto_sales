![](https://github.com/FilippoGuardassoni/auto_sales/blob/main/img/headerheader.jpeg)

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
The test set was created randomly using sample.split function from R package.
The Random Forest once again performed better for the classification. The overall results are reported below:


<img width="617" alt="Screenshot 2023-05-18 at 19 45 22" src="https://github.com/FilippoGuardassoni/spotify_hitsong/assets/85356795/b420dcdd-5dbe-4170-81b7-cfe1797d705c">

All the models predicted the test set with an incredibly high consistency, showing almost no overfitting over the training dataset. Considering the training set, the same conclusions can be drawn here.
The focus was mainly on the accuracy of results, but the precision and recall for the best models are reported as well since false positive predictions may be costly when a music label invests in a song that is actually unlikely to become a hit.

<img width="475" alt="Screenshot 2023-05-18 at 19 46 59" src="https://github.com/FilippoGuardassoni/spotify_hitsong/assets/85356795/e4bfc124-b326-4150-b562-a9d66f783085">


# Future work
This study aimed to predict whether a song will be a hit or not using features from Spotify API as a base. The first limitations come in play here. The definition of what a hit is inherently has constraints. This affects the composition of the dataset as well. A broader definition of hit could impact positively the research. In addition, the features are limited to the ones that Spotify API makes available. Other features for example of sound can be inserted such as bit depth and amplitude. Feature extraction and spectrogram analysis from the song audio files could be another successful approach. Subjective preferences, seasonality and time period might be taken in account as well. As instance, certain songs or genre such as Latin music are more likely to become hits in summer than in winter. Furthermore, particular characteristics in songs that made songs famous in the past are not a good guarantee for the future. While rock music dominated in the decades before 2000, nowadays electronic music took hold. Lyrics of a song could be considered to see if there are recurrencies, patterns or words that boost listening.

# Acknowledgments/References
See report/song_hit_prediction.pdf for references.

# License
For this github repository, the License used is [MIT License](https://opensource.org/license/mit/).

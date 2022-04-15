# Crypto Currency Dashboard

A dashboard created by Ishan Dhanani, David Zhu, Anish Maddipotti, Ethan Rich, Ally MacRobert, and Amish Gautam

## Prerequisites
- To run the dashboard, be sure to install the packages listed in requirements.txt
- Make sure to have a folder called 'data' which stores the .csv files

## To download and/or update the data from bitfinex:
1. Download all(400+) sets of .csv files into directory "/data": 
- run the "download_all_data" file (auto downloads from API from 2013 till current time)(might take a while)
- or alternatively: download the latested kaggle dataset on kaggle(https://www.kaggle.com/datasets/tencars/392-crypto-currency-pairs-at-minute-resolution), create and put all the .csv files on "/data" directory (updates once a month)
2. To update a specific file:
- run 'update_data funtion' notebook, use "update_data(desired_coin)" and it will automatically update the /data folder

## Dashboard UI 
Home Page:
- The initial page displayed when the dashboard code is run
- Consists of a header which displays the current price of high market cap cryptocurrencies. Can select different ones based on preference
- The prices are updated live, as derived by the API used

- Under the Price Bar is a Quick Look Candlestick Graph, which is used to take a glance at the Prices of Each Cryptocurrency through a selected time span, which ranges from the last 24 Hours to the last Year
- We can toggle between our graph being a Candlestick or a Line Graph
- The 20 Periods and 50 Period SMA is also plotted

- On the left side of the entire dashboard is a Sidebar that allows us to switch tabs between the kind of information we want to see
-The tabs include:
	1) Home
	2) Stats
	3) Sentiment Analysis
	4) Technical Indicators 

Stats Page:
- On this tab, we can compare multiple cryptocurrencies and view a Correlation plot, as well as a Return on Investment Plot of their prices over a time frame we choose
- There are 2 dropdown menus that are used for providing us options between various cryptocurrencies, and timeframes ranging from the last 1W to all time

Sentiment Analysis:
- On this tab, we can enter phrases and the pie-chart will display the current sentiment breaktown from Twitter. We use basic NLP techniques from the TextBlob package

Technical Indicators Page:
- On this page, we enter the name of the Cryptocurrency, the time frame, and the technical indicator we want to visualize

- The three different types of indicators to view information about are:
	- Exponential Moving Average (EMA)
	- MACD (Moving Average Convergence Convergence/Divergence) 
	- Bollinger Bands
- The table at the bottom of the page displays the selected periods ROI

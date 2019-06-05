# Forecasting electricity daily SPOT market price in Spain

## Description
This repo is a Data Science project which main goal is to build a Machine Learning model to forecast electricity spot market daily price.
The framework contains every step in a DS project, from data ingestion, to visualization and analysis, and finally training and deploying a ML model

### Index
1. Import data from external APIs
2. EDA (Exploratoy Data Analysis)
3. Model Building and evaluation

## Technology

Python 3.6

Install libraries with pip

pip install quandl
https://docs.quandl.com/docs/python-installation

## Import Data
Electricity market data (REE ESIOS API)
* Daily price is set at daily auctions in a pool market. This market is said to be marginal, because there is a matching bid that sets current day price. 
* P48 generation by technology: It is also called PHO (Programa Horario Operativo) and it is the definitive schedulled generation program

REE is the TSO (Transmission System Operator) in Spain, it is a public enterprise which owns, builds and operates high voltage transmission lines. Moreover, at a system operation level, it is responsible of running several auctions and adjustment mechanisms. Regarding SPOT market (run by OMIE), REE delivers data though its website ESIOS. OMIE is responsible of running several auctions, such as spot and intraday.

https://www.esios.ree.es/en

Financial data (Quandl API):
https://www.quandl.com/
* EUA (European Emission Allowances, CO2): Important when marginal generator is a coal or natural gas utility
* Coal API2: There are many kinds of coal (antracite, lignite, etc.), so finantial analysis firms deviced this index arranging European data
* Natural Gas TTF: It stands for Title Transfer Facility, it is a Virtual Trading point in the Netherlands, and also a price reference in European HG markets (like Henry Hub or NBP)

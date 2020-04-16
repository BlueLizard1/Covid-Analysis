# Covid-Analysis
 
## Overview

The Covid Analysis repo was created as a pet project to analyze the current Covid-19 crisis. The data for the repo is taken directly from the Center for Systems Science and Engineering (CSSE) at Johns Hopkins University  ( CSSEGISandData / COVID-19 repo https://github.com/CSSEGISandData/COVID-19). This project will likely change often based on newer expectations on the questions that need answers.

The data from the Github repo is availabe in daily csv files (also available in time-series data) that can be downloaded freely from the repo. 

## Process

### Step 1 - Retrieve the source files

Git was used to retrieve the latest data from Github.

### Step 2 - Import the data into SQL Server

An SSIS package was created to process the lastest file for importing into a Staging Table.

Once the file has been imported, a stored proc is run to process the data into a format that can be readily used in Business Analytics software such as Tableau or Power BI.

NOTE: The format of the csv files and subsequent data changed from January until current date. There was some manual cleanup of the data that was necessary.

### Step 3 - Connect the data to Business Analytics software.

The resulting data consists of just one table that contains all of the necessary information. An Azure SQL database was established to connect to the data.

## Resources

Apart from the resources in this repo, several online resources are available for further Covid-19 research.

Johns Hopkins Dashboard (Currently cited by most news organizations)
https://coronavirus.jhu.edu/map.html

CDC Covid-19
https://www.cdc.gov/coronavirus/2019-ncov/index.html

WHO Situation Reports
https://www.who.int/emergencies/diseases/novel-coronavirus-2019/situation-reports

NCDHHS Covid-19 Response
https://www.ncdhhs.gov/divisions/public-health/covid19

European Commission Coronavirus Response
https://ec.europa.eu/info/live-work-travel-eu/health/coronavirus-response_en



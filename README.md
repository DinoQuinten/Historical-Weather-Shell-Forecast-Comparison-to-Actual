# Weather ETL Process - Proof of Concept

## Overview
This repository contains a proof-of-concept (POC) for an automated Extract, Transform, Load (ETL) process that extracts daily weather forecasts and observed weather data and loads it into a live report. This report is intended for further analysis by the analytics team to monitor and measure the historical accuracy of temperature forecasts by source and station.

## Scenario
You've been tasked by your team to create an ETL process to gather weather data for Casablanca, Morocco. This POC focuses on extracting actual and forecasted temperatures at noon for a single station and one source.

## Data Source
We use the `wttr.in` web service to provide weather forecast information in a simple, text-based format.

## Learning Objectives
After completing this project, you will be able to:
- Download raw weather data
- Extract data of interest
- Transform the data as required
- Load the data into a log file using a tabular format
- Schedule the entire process to run automatically at a set time daily

## Weather Reporting Tasks
The ETL process will extract and store the following data every day at noon (local time) for Casablanca, Morocco:
- The actual temperature (in degrees Celsius)
- The forecasted temperature (in degrees Celsius) for the following day at noon

### Example Report
| year | month | day | obs_tmp | fc_temp |
|------|-------|-----|---------|---------|
| 2023 | 1     | 1   | 10      | 11      |
| 2023 | 1     | 2   | 11      | 12      |
| 2023 | 1     | 3   | 12      | 10      |
| 2023 | 1     | 4   | 13      | 13      |
| 2023 | 1     | 5   | 10      | 9       |
| 2023 | 1     | 6   | 11      | 10      |

## Instructions
1. **Download Raw Data**: Use `curl wttr.in/casablanca` to fetch weather data.
2. **Extract Data**: Parse the raw data to extract actual and forecasted temperatures.
3. **Transform Data**: Format the extracted data into a tabular log file.
4. **Load Data**: Save the formatted data into a log file for analysis.
5. **Automation**: Schedule the script to run daily using cron jobs or a similar scheduler.

## Authors
- Jeff Grossman
- Other Contributors: Rav Ahuja

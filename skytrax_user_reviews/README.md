# Data Set Name

A scraped dataset from 2015 and older, created from all user reviews found on [Skytrax](www.airlinequality.com). It contains reviews of;
 * Flights
 * Airports
 * Airport Lounges
 * Seats

Original data via https://github.com/quankiquanki/skytrax-reviews-dataset.

**NOTE** This data was processed with version 5.0 of the Elastic Stack using the Kibana CSV import process, there are no Logstash configs, see below for details.

This repo only has a dashboard for the flight reviews at the moment.

## Files

 * `README.md` - You're looking at it
 * `skytrax_user_reviews-dashboard.json` - Kibana dashboard export
 * `skytrax_user_reviews-dashboard.jpg` - Screenshot of the dashboard
 * `skytrax_user_reviews_*-data.csv` - Various data files

## Getting it to work

1. In Kibana 5.0, open the *Management* section, then *Upload CSV*
2. Select the file you want to import
3. Make sure the detected mappings match, you may need to change some numeric fields to integers and not strings
4. Wait for the upload to finish
5. Import the dashboard json file
6. Open the *Skytrax User Reviews* dashboard
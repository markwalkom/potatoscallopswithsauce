# Australian National Public Toilets

Original data via https://data.gov.au/dataset/national-public-toilet-map

NOTE - I need to fix this and remove the ruby script, use the spit filter instead.

## Files

 * `README.md` - You're looking at it
 * `australian_national_public_toilets-dashboard.json` - Kibana dashboard export
 * `australian_national_public_toilets-dashboard.jpg` - Screenshot of the dashboard
 * `australian_national_public_toilets-mappings.json` - Elasticsearch mappings
 * `australian_national_public_toilets-logstash.conf` - Logstash config file
 * `australian_national_public_toilets-data.csv.gz` - The data file, ammendments as per above comments

## Getting it to work

1. `PUT` the mappings using Sense
2. Extract the data - `gunzip australian_national_public_toilets-data.csv.gz`
3. Ingest with `cat australian_national_public_toilets-data.csv | /path/to/logstash -f australian_national_public_toilets-logstash.conf`
4. Import the `australian_national_public_toilets-dashboard.conf` file into Kibana
5. Open the *Australian National Public Toilets* dashboard
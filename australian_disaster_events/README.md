# Australian Disaster Events

Original data via https://data.gov.au/dataset/disaster-events-with-category-impact-and-location.

NOTE - I need to fix this and remove the ruby script, use the split filter instead. It's also using a lot of old config, it was one of the first I did with data.gov.au, and needs a clean up :)

## Files

 * `README.md` - You're looking at it
 * `australian_disaster_events-dashboard.json` - Kibana dashboard export
 * `australian_disaster_events-dashboard.jpg` - Screenshot of the dashboard, also below
 * `australian_disaster_events-mappings.json` - Elasticsearch mappings
 * `australian_disaster_events-logstash.conf` - Logstash config file
 * `australian_disaster_events-data.csv` - The data file

## Getting it to work

1. `PUT` the mappings using Sense
2. Ingest with `cat australian_disaster_events-data.csv | /path/to/logstash -f australian_disaster_events-logstash.conf`
3. Import the `australian_disaster_events-dashboard.conf` file into Kibana
4. Open the *Australian Disaster Events* dashboard
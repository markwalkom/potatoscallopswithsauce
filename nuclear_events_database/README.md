# Nuclear Events Database

A dataset of 216 incidents and accidents occurring at nuclear power plants worldwide.

Original data via https://innovwiki.ethz.ch/index.php/Nuclear_events_database.

The CSV data has been modified to clean up irregularities; normalising USA/United States, USSR/Soviet Union etc, some locations had missing countries, *Description* fields with line feeds were concatenated.

TODO;
 * See if I can use this [vector map](https://github.com/stormpython/vectormap)

## Files

 * `README.md` - You're looking at it
 * `nuclear_events_database-dashboard.json` - Kibana dashboard export
 * `nuclear_events_database-dashboard.jpg` - Screenshot of the dashboard
 * `nuclear_events_database-mappings.json` - Elasticsearch mappings
 * `nuclear_events_database-logstash.conf` - Logstash config file
 * `nuclear_events_database-data.csv` - The data file, ammendments as per above

## Getting it to work

1. `PUT` the mappings using Sense, or 
2. Ingest with `cat nuclear_events_database-data.csv | /path/to/logstash -f nuclear_events_database-logstash.conf`
3. Import the `nuclear_events_database-dashboard.conf` file into Kibana
4. Open the *Nuclear Events Database* dashboard
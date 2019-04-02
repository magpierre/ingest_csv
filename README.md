# ingest_csv
Sample Go client reading csv files and ingest them as documents into a MapR Database

To build a docker container:
docker build -t ingest_csv .

to run the docker container:
docker run ingest_csv which will show the parameters

To run with parameters (example):
docker run --rm -it ingest_csv -filename ~/input.csv -password mapr -mapr-url somehost:5678 -mapr-tablename /tmp/ingested_data

*** NOTE ***
This demo code assumes the first field is the id column and appends a time now on it to keep everything unique.
It further assumes that the csv has a header.


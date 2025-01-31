## Module 2 Homework

For the homework, we'll be working with the green taxi dataset located here:

https://github.com/DataTalksClub/nyc-tlc-data/releases/tag/green/download

To get a wget-able link, use this prefix (note that the link itself gives 404):

https://github.com/DataTalksClub/nyc-tlc-data/releases/download/green/

## Homework Questions

1) Within the execution for `Yellow` Taxi data for the year `2020` and month `12`: what is the uncompressed file size (i.e. the output file `yellow_tripdata_2020-12.csv` of the `extract` task)?

- 128.3 MB
- 134.5 MB
- 364.7 MB
- 692.6 MB

### Answer: 128.3 MB

2) What is the rendered value of the variable file when the inputs taxi is set to green, year is set to 2020, and month is set to 04 during execution?

- {{inputs.taxi}}_tripdata_{{inputs.year}}-{{inputs.month}}.csv
- green_tripdata_2020-04.csv
- green_tripdata_04_2020.csv
- green_tripdata_2020.csv


### Answer: green_tripdata_2020-04.csv

3) How many rows are there for the Yellow Taxi data for all CSV files in the year 2020?

- 13,537.299
- 24,648,499
- 18,324,219
- 29,430,127

```sql

SELECT count(1) FROM `kestra-sandbox-449423.de_zoomcamp.yellow_tripdata` 
WHERE filename LIKE '%2020%';
```

### Answer: 24,648,499

4) How many rows are there for the Green Taxi data for all CSV files in the year 2020?

- 5,327,301
- 936,199
- 1,734,051
- 1,342,034

```sql

SELECT count(1) FROM `kestra-sandbox-449423.de_zoomcamp.green_tripdata` 
WHERE filename LIKE '%2020%';
```

### Answer: 1,734,051

5) How many rows are there for the Yellow Taxi data for the March 2021 CSV file?

- 1,428,092
- 706,911
- 1,925,152
- 2,561,031

```sql

SELECT count(1) FROM `kestra-sandbox-449423.de_zoomcamp.yellow_tripdata` 
WHERE filename LIKE '%2021-03%';
```

### Answer: 1,925,152

6) How would you configure the timezone to New York in a Schedule trigger?

- Add a `timezone` property set to `EST` in the `Schedule` trigger configuration  
- Add a `timezone` property set to `America/New_York` in the `Schedule` trigger configuration
- Add a `timezone` property set to `UTC-5` in the `Schedule` trigger configuration
- Add a `location` property set to `New_York` in the `Schedule` trigger configuration  

 ### Answer: Add a `timezone` property set to `America/New_York` in the `Schedule` trigger configuration


## Submitting the solutions

* Form for submitting: https://courses.datatalks.club/de-zoomcamp-2025/homework/hw2
* Check the link above to see the due date

# Project-2 Team 16
Group 16 (Peter Kim and Mohammad Rao) present our ETL project on the 2016 presidential primary.

Extract: your original data sources and how the data was formatted (CSV, JSON, pgAdmin 4, etc). Sources “primary_results.csv” - Primary voter results by county. CSV format in Kaggle. “county_fact.csv” - Demographics by county. CSV format in Kaggle. The two datasets were initially loaded and formatted in Pandas.

Transform: what data cleaning or transformation was required. Demographics table. – imported into Pandas as csv file. •	The column headers in the Demographics table were coded. These headers were renamed in pandas.
•	The only the required columns were brought into the final dataframe. •	The demographic columns included FIPS code, gender, ethnicity, household income • Primary results table. – imported into Pandas as csv file. •	The only the required columns were brought into the final dataframe. •	The column includes FIPS Code, state, county, voter count, political party, candidate.

Load: the final database, tables/collections, and why this was chosen. We loaded and joined the final pandas dataframes into Postgres. The two datasets were relationally joined on the primary key: FIPS code. We choose Portgres to allow for new datasets and clear segmentation of data. Create database connection: connection_string = "postgres:postgres@localhost:5432/xxxx_db" engine = create_engine(f'postgresql://{connection_string}')

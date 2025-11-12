# THE GLOBAL DIGITAL DIVIDE DATA PIPELINE

A data engineering project that builds an automated, end-to-end data pipeline integrating global datasets on internet access, education, and income to analyze patterns of digital inequity. 


## POTENTIAL DATA SOURCES:
- World Bank API
    - Internet Users (% of population)
    - GDP per capita
    - population
    - literacy 
    https://data.worldbank.org

International Telecommunication Union
    - broadband subscriptions
    - mobile usage 
    https://www.itu.int/en/Pages/default.aspx

UNESCO
    - educational enrollment
    - literacy rates
    https://databrowser.uis.unesco.org

Can also look at national statistics or Kaggle datasets (digital skills index, etc)


## PROJECT GOALS
1. ingest real-world datasets from APIs and CSVs
2. transform and standardize country-level data (different schemas, date formats, etc)
3. model the data in a normalized, query optimized database
4. automate the pipeline with a workflow scheduler (Airflow)
5. store and serve data via a cloud-based PostgreSQL database
6. visualize trends (e.g., how income and education correlate with internet access)

## DATABASE SCHEMA: 
Tables
    - countries
        - country_id
        - country_name
        - iso_code
        - region
    - internet access
        - id
        - country_id
        - year
        - internet_users_percent
        - broadband_subscriptions_per_100
    - education
        - id
        - country_code
        - year
        - literacy_rate
        - school_enrollment_rate
    - economy
        - id
        - country_id
        - year
        - gdp_per_capita
        - income_level
    

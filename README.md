# services
Data base management services 



Order
1. fetch mixpanel events
2. transform events if needed:
    a. remove unwanted fields
    b. rename fields
    c. change data types/handle data inconsistencies
    d. validate against schema
    e. log errors if any
    f. return cleaned data 
    g. batch data if needed
    h. prepare for bigquery upload
    i. upload to bigquery staging table 
    j. remove duplicates in staging table
3. merge staging table to main table
    a. log success/failure of each step
    b. send notifications if outlier found 
    c. schedule next run
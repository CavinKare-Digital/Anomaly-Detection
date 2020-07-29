# Facebook Prophet

### Anomaly Detection for Indica Powder in East Region - Primary Data


This Model can detect anomalies for each distributor, based on his buying behaviour.      

**Data Source**
1. Azure Data Warehouse
2. Excel - ACTDTE for merging the dates for no data.

**Model Design**
1. Taking the raw data from Azure database.           
2. Grouping the number of items(**Billing_Qty**) bought by distributor for each month.            
3. Imputing Zeroes for the month where there was no purchase.                    
4. Creating a dataframe with Multi-Index (**Distributor Code and Code**)                 
5. Renaming the columns to ds and y (**Actdte and Billing_Qty**)          
6. Fit the FB prophet Model to the dataframe by looping each Distributor and Code (**keys**)                 
7. Detect the anomalies from the forecast.            
8. Export the data into .xlsx format.              

**Note**: 
1. If you want to run the model for a sample data, make sure you alter the **keys** to sample data and check whether the grouped data is available in **new data**.

(**Bold** used to represent the column names and variables used in the Notebook )

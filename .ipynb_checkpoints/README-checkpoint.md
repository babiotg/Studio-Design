# Studio Design - Data Analysis
For a digital graphics study, the request was to analyze sales over a period of 5 years, from 2018 to 2022.

## Requirements
The requirements were to verify:

* sales
* quantity of sales
* quantity of products sold
* quantity of customers 

for each year, comparing the values with those of the previous year. 

* A plus would have been to have a geographical visualization of these values distributed on a map of Italy.  
* The client specifically requested a dedicated dashboard that contained a single chart providing an overview of the sales of each product for each year.
* A very important element for the client was to improve customer retention, implementing a system to reactivate customers. 

For this reason, I created a dedicated dashboard to see the situation of customer activity in general:

* Average Customer Lifetime
* Average Customer Lifetime Value
* New Customer Acquisition
* Customer Activity by Quarter (first, recurrent, last purchase)

Then another dashboard to go into more detail on what each customer spent during each year, with the relevant details.

# Data Source
The data comes from fattureincloud.it. I was provided with 5 Excel files, one for each year. The project started in July, so at that time the file contained only sales up to June. Over time, the client sent me the data to integrate new information into the dashboards.

<img src="img/img_fattureincloud.png" alt="Data Source from Fattureincloud.it"> 

# Data Cleaning & EDA
* The data cleaning was performed with Python, in the folder *data quality* there is an extract of Data_Quality.ipynb file, obviously there is not the complete file for a matter of data privacy. With data cleaning I standardized and made the names of the cities consistent for the subsequent geolocation.

<img src="img/img_1.png" alt="Sales 2018-2022">
<img src="img/img_3.png" alt="Sales 2018-2022">
<img src="img/img_dataset_info.jpg" alt="Dataset information">


* I merged the 5 sources into a single file, and cleaned it of unnecessary columns. This is how the final output looks like:

<img src="img/img_sales_18_22.jpg" alt="Sales 2018-2022">

* I created a relational table with geolocation data for each customer, to improve dashboard performance.

<img src="img/img_geoloc_custom.jpg" alt="Customers Geolocation">


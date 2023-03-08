# **Studio Design - Data Analysis**
Tableau project for a digital graphics study, the request was to analyze sales over a period of 5 years, from 2018 to 2022.

To **view** the **Tableau visualization** please visit my Tableau profile:
**[Studio Design with Customer Analysis](https://public.tableau.com/app/profile/barbara.callegari/viz/StudioDesignwithCustomerAnalysis/)**

## **Requirements**
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

# **Data Source**
The data comes from fattureincloud.it. I was provided with 5 Excel files, one for each year. The project started in July, so at that time the file contained only sales up to June. Over time, the client sent me the data to integrate new information into the dashboards.

<img src="img/img_fattureincloud.png" alt="Data Source from Fattureincloud.it"> 

# **Data Cleaning & EDA**
* The data cleaning was performed with Python, in the folder *data quality* there is an extract of Data_Quality.ipynb file, obviously there is not the complete file for a matter of data privacy. With data cleaning I standardized and made the names of the cities consistent for the subsequent geolocation.

<img src="img/data_quality.jpg" alt="Extract from Data Quality Jupyter Notebook">

* I merged the 5 sources into a single file, and cleaned it of unnecessary columns. This is how the final output looks like:

<img src="img/img_sales_18_22.jpg" alt="Sales 2018-2022">

* I created a relational table with geolocation data for each customer, to improve dashboard performance.

<img src="img/img_geoloc_custom.jpg" alt="Customers Geolocation">

# **Tableau Dashboard**

The KPI Dashboard displays the values for each year, allowing for a comparison with the previous year, for the following metrics: sales, quantity of sales, quantity of products sold, and quantity of customers. It is possible to select the reference year (from 2018 to 2022).

## **KPI Dashboard**

### **KPI Dashboard** for **Sales** (compared to previous year)
* Sales by category
* Top 5 products on sales 
* Top 10 cities on sales
<figure style="text-align:center;">
  <figcaption>KPI Dashboard - Sales</figcaption>
  <img src="img/KPI_Dashboard_Sales.jpg" alt="KPI Dashboard - Sales">
</figure>

### **KPI Dashboard** for **Nr. of Orders** (compared to previous year)
* Nr. of Orders by category
* Top 5 products on nr. of orders 
* Top 10 cities on nr. of orders
<figure style="text-align:center;">
  <figcaption>KPI Dashboard - Nr. of Orders</figcaption>
  <img src="img/KPI_Dashboard_NrOfOrders.jpg" alt="KPI Dashboard - Nr. of Orders">
</figure>

### **KPI Dashboard** for **Product Quantity** (compared to previous year)
* Product quantity by category
* Top 5 products on product quantity  
* Top 10 cities on product quantity 
<figure style="text-align:center;">
  <figcaption>KPI Dashboard - Product Quantity</figcaption>
  <img src="img/KPI_Dashboard_Product_Quantity.jpg" alt="KPI Dashboard - Product Quantity">
</figure>

## **KPI Geo Dashboard** with geographical details (compared to previous year)
* KPI (switchable between: sales, nr. of orders, product quantity) by region
* KPI (switchable between: sales, nr. of orders, product quantity) by cities
* Option to render the map by region or by city
* Option to select a specific region
<figure style="text-align:center;">
  <figcaption>KPI Geo Dashboard</figcaption>
  <img src="img/KPI_Geo_Dashboard.jpg" alt="KPI Geo Dashboard">
</figure>

## **Product Revenue Dashboard**
Contains a single chart providing an overview of the sales of each product for each year.
<figure style="text-align:center;">
  <figcaption>Product Revenue Dashboard</figcaption>
  <img src="img/Product_Revenue_Dashboard.jpg" alt="Product Revenue Dashboard">
</figure>


## **Customer Growth Dashboard**:
* Avg. Customer Lifetime
* Avg. Customer Lifetime Value
* Option to choose view between:
    * Customer Activity
    * Retention Rate

The **Customer Activity view** contains:
* New Customers Acquisition
* Purchase Frequency
* Customer Activity by Quarter from 2018 to 2022

<figure style="text-align:center;">
  <figcaption>Customer Growth Dashboard - Customer Activity view</figcaption>
  <img src="img/Customer_Growth_Dashboard.jpg" alt="Customer Growth Dashboard - Customer Activity view">
</figure>

The other **view** contains the **Retention Rate** broken down by Elapsed Quarters vs. the Customer Acquisition Quarter. The Retention Rate is colored with Orange-Blue Diverging color, where orange is the lowest and Blue is the highest value.

<figure style="text-align:center;">
  <figcaption>Customer Growth Dashboard - Retention Rate view</figcaption>
  <img src="img/Customer_Retention_Rate.jpg" alt="Customer Growth Dashboard - Retention Rate view">
</figure>

## **Customer Engagement Dashboard**
* Customer Purchase Summary
* Revenue by Client Over Years
* Achievements of the Customer Regain Efforts

<figure style="text-align:center;">
  <figcaption>Customer Engagement Dashboard</figcaption>
  <img src="img/Customer_Engagement_Dashboard.jpg" alt="Customer Engagement Dashboard">
</figure>

## **Key findings**
As of the analysis processing start date on 10/06/2022, there were 316 customers who had not made a purchase in over a year.

Thanks to the analysis conducted, the sales account manager was able to take action to re-engage customers and increase sales in the second half of the year.   
As a result of the **Customer Regain Efforts**, **22 customers** who had not made a purchase in over a year were successfully regained, representing **6.6%** of the potential customer base. These customers contributed **20.711€** to revenue, which would not have been realized without the intervention of the Customer Regain Efforts.

Also there has been an **increase** in:
* **Average Customer Lifetime** from 7.3 to 8.2 months (**+12.3%**)
* **Average Customer Lifetime Value** from 857.8€ to 943.3€ (**+12.2%**)

<figure style="text-align:center;">
    <figcaption>Avg. CL and Avg. CLV <br>before and after Customer Regain Efforts</figcaption>
  <img src="img/Avg_CL_and_CLV_Growth.jpg" alt="Average Customer Lifetime and Customer Lifetime Value Growth">
</figure>

The **Retention Rate has increased significantly**, as can be seen from the chart Retention Rate up to 09/06/2022.

<figure style="text-align:center;">
    <figcaption>Retention Rate up to 09/06/2022 (<b>before Data Analysis</b>)</figcaption>
  <img src="img/Retention_Rate_up_to_09_06_2022.jpg" alt="Retention Rate up to 09/06/2022">
</figure>

<figure style="text-align:center;">
    <figcaption>Retention Rate up to 31/12/2022 (<b>after Customer Regain Efforts</b>)</figcaption>
  <img src="img/Retention_Rate_up_to_31_12_2022.jpg" alt="Retention Rate up to 31/12/2022">
</figure>

### Author 
[Barbara Callegari](https://numberslab.net)  
To learn more about the author visit my [LinkedIn Profile](https://www.linkedin.com/in/barbaracallegari)


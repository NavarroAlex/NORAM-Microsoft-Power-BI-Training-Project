# NORAM Microsoft Power BI Pro Training
![ScreenShot](Power-BI-DAX.png)

## Importing Data Sources:
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Data%20Sources.png)

We will import the following data sources:
* Product Sales Data "Text File"
* Customer Mapping File "Excel File"
* Product Attributes Data "Excel File"

## Steps to Import Data:
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Import%20Data%20Sources.png)

* Under the "Home" tab click "Get Data"
* We will first start with importing the "Product Sales Data" which is a Text file type, so we want to click "Text/CSV"

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Transform%20Data.png)

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Annotation%202022-09-13%20090046.png)

You are now inside the "Microsoft Power BI Query Editor".
Lets grab the rest of our data sources by clicking "New Source" under the "Home" Tab.
Once you're done grabbing the rest of the data sources, should now see the following three data sources:

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/All%20Physical%20Data%20Sources.png)

## Data Transformation/Data Cleaning:

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/5d5c22e040c6beab16860e8e_data-cleaning-thumb.png)

Now that we have all of our data sources imported into the Microsft Power Query Editor, we can start cleaning our data!
We will implement the following steps:
* Remove Uncenessary columns
* Extract specific values from a column
* Data Type Transformation
* Join Data Sources Together
* Remove Duplicates
* Rename Columns
* Create New Columns
* Replace Null Values

Lets start with the "Product Sales Data"

First, lets remove the column called "123" as we don't need this column:
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Remove%20Columns.png)

Next, we can split our "Time" column. We only want the actual date value from the column. So let's get rid of "Week Ending".

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Split%20Columns.png)

Once you click "Split Column" and "By Positions", you should be prompted with the following screen:
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Annotation%202022-09-13%20094116.png)

You should now see two date columns, one is called "Time.1" and the other "Time.2".
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Time%20Column1%20and%20Column2.png)

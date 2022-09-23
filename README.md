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

### You are now inside the "Microsoft Power BI Query Editor".
### Lets grab the rest of our data sources by clicking "New Source" under the "Home" Tab.

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Annotation%202022-09-13%20090046.png)

### Once you're done grabbing the rest of the data sources, should now see the following three data sources:

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/All%20Physical%20Data%20Sources.png)

## Data Transformation/Data Cleaning:

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/5d5c22e040c6beab16860e8e_data-cleaning-thumb.png)

### Now that we have all of our data sources imported into the Microsft Power Query Editor, we can start cleaning our data!
### We will implement the following steps:
* Remove Uncenessary columns
* Extract specific values from a column
* Data Type Transformation
* Join Data Sources Together
* Remove Duplicates
* Rename Columns
* Create New Columns
* Replace Null Values

### Lets start with the "Product Sales Data"

### First, lets remove the column called "123" as we don't need this column:
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Remove%20Columns.png)

### Next, we can split our "Time" column. We only want the actual date value from the column. So let's get rid of "Week Ending".

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Split%20Columns.png)

### Once you click "Split Column" and "By Positions", you should be prompted with the following screen:
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Annotation%202022-09-13%20094116.png)

### You should now see two date columns, one is called "Time.1" and the other "Time.2".
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Time%20Column1%20and%20Column2.png)

### Lets remove column "Time.1" and rename column "Time.2" to "Time":
- right-click on "Time.1" and choose "Remove"
- double click on the header of column "Time.2" and Rename to Time

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Remove%20Column%20time.1.png)

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Time%202.png)

### You should now have one column called "Time" and it should look like the following:
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Final%20Time.png)

### Let's replace the data type of column "Dollar Sales" with a fixed decimal data type. Let's also replace the data type of column "Unit Sales" with a whole number data type:

- click the data type symbol which will be to the left of the column name for each column. Here, you will then be able to change the data type.

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/DS%20Data%20Type.png)

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/US%20Data%20Type.png)

### Now remove the column called "Weighted Average Base Price Per Unit" as we need this column and keep it will contribute to longer compute time of our report.
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Weighted%20Average%20Base%20Price.png)

### Before we do our first merge, lets clean the "Product Attributes" dataset:
* Remove the "123" column as we don't need it.
* Remove Duplicates

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Remove%20Columns%20PA.png)

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Remove%20Duplicates.png)

### Let's do our first merge. We will merge the Product Sales Data with the Product Attributes dataset using "SKU" as our primary key to merge on.
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/First%20Merge.png)

### Under the "Home" tab, select "Merge Queries" and "Merge Queries":
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Merge%20Queries%202.png)

### Scroll to the far right and select the "Product Attributes" column. Click "Expand" and mirror the screenshot below then click "OK".
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Expand%20Columns.png)

### Now let's clean our "Customer Mapping" file.
* Remove column "1" as we don't need this column.
* Promote Headers. Move the headers up one row for we can see the headers were imported on the second and now the first row.

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Remove%20columns%20customer%20mapping.png)

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Column%20Headers.png)

### After cleaning the Customer Mapping file, it should look like the following:
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Customer%20Mapping%20File%20Clean.png)

### Now that our Customer Mapping file is clean, let's merge this dataset with our "Product Sales Data".
* Click the "Customer Mapping" file first.
* Hold down CTRL then click the "Product Sales Data" data set.
* Under the "Home" tab, go to "Merge Queries" and select "Merge Queries"
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Final%20Merge.png)

### Expand Customer Mapping:
* Scroll to the right and select the column "Customer Mapping" mirror the screenshot below and click "OK".
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Customer%20Mapping%20Expand.png)

### Learning how to create a "Conditional Column":
* Lets learn how to add a custom column to our dataset, in this case we are going to create a Conditional column that will display the category depending on the "Custom Type Value" value.
* Go to the "Add Column" tab at the top and then click "Conditional Column".

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Conditional%20Column.png)

### Category Logic:
* IF Custom Type Value = TRADITIONAL THEN BEVERAGES
* IF Custom Type Value = ALMOND THEN BEVERAGES
* IF Custom Type Value = GREEK THEN YOGURT
* IF Custom Type Value = REGULAR THEN YOGURT
* ELSE NULL
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Conditional%20Logic.png)
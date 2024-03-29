# NORAM Microsoft Power BI Pro Training
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Power%20BI%20Theme.png)

## Author
[alex.navarro@danone.com]

# Importing Data Sources:
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

# Data Transformation/Data Cleaning:

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
* IF Product CONTAINS INTERNATIONAL DELIGHT THEN BEVERAGES
* IF Product CONTAINS OIKOS THEN YOGURT
* IF Product CONTAINS DUNKIN THEN BEVERAGES
* IF Product CONTAINS BAILEYS THEN BEVERAGES
* ELSE NULL

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Conditional%20Logic.png)

### We're now done cleaning and transforming our data, click "Close and Apply":
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Close%20and%20Apply.png)

# Creating Data Analysis Expression (DAX):
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Power-BI-DAX.png)

If you're using "physical" data sources and not connected to a live connection, you will want to create a date table if you want to visualize the data by certain date attributes.
* We're going to use the following DAX functions to develop a script that will give us multiple date attributes.
    - ADDCOLUMNS
    - YEAR
    - MONTH
    - FORMAT
    - DAY
    - COMBINEVALUES
    - QUARTER
* Go to the "Data Model" View then click on the "Table tools" tab then select "New table".
    - ![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Calendar%20Table%20Creation.png)
* A blank table will appear, paste in the following date script below then press the check mark.

```
Calendar_Complete = ADDCOLUMNS(
--create generate calendar dates:
CALENDARAUTO(12)
-- create year column:
,"Year",YEAR([Date])
-- create month number column:
,"Month Number", MONTH([Date])
-- create month name:
,"Month Name",FORMAT([Date],"MMMM")
-- create day number:
,"Day",DAY([Date])
-- create month and year column:
,"Month_Year",COMBINEVALUES(", ",FORMAT([Date],"MMMM"),FORMAT([Date],"yyyy"))
-- create quarter column:
,"Quarter",QUARTER([Date])
-- create week day number:
,"Week Day Number",WEEKDAY([Date],1)
--create week day number:
,"Week Day Name",FORMAT([Date],"DDDD")

)
```

Once you've pasted the script and clicked the "Check Mark" you should see the following table created:
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Paste%20in%20Code.png)

* You need to tell Microsoft Power BI that there exist a numeric hierarchy for the "Month Name" column as it's not able to detect this. This is why we created the column called "Month Number". Lets use it to rank our Month Names.
    - Go to the "Calendar_Complete" table and click on "Month Name" column.
    - Then at the top of the page click "Sort by Column" drop-down under the "Column Tools" tab.
    - Then Check Sort By Column "Month Number". Now the months will be sorted in the correct order. Repeat the process for column "Week Day Name" using "Week Day Number" as the sorting column.
    - ![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Ranking%20Month%20Name.png)
    - ![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Week%20Day%20Rank.png)

You should now see the following date table below:
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Date%20Table.png)

# Data Modeling:
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Power%20BI%20Data%20Modeling.png)
* Because we did most of our joining of data sources within the Power Query Editor, we won't have much to join in the data model view. If we hadn't done our joining in the Power Query editor, (which is common if you're connected to a live dataset as you cannot access the Power Query editor when connecting to a live dataset), you will want to use the data modeling tab to join your data.
* The only data sources we need to join is our table called "Dataset" and the "Calendar" table we created earlier.
* We need to join on a primary key (unique column indentifer in both tables) for this we will use "Date".
* Click the "Date" column and drag and drop on top of the "Date" column in the "Dataset" table.
    - ![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Joining%20Date%20Table.png)
* You can see the Microsoft Power BI was able to auto-detect what kind of relationship should be used to join the two tables together. This isn't always the case so make sure that the proper join is being applied before moving onto the next step.
    - ![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Created%20Relationship.png)
* If you double click on the relationship between the two tables, you can view what kind of relationship is being used to join the tables. In this example, Power BI used a many-one relationship.
    - ![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Open%20Join%20View.png)


## Creating Measures Table:
Before we start creating DAX measures, it's best practice to create a "Measures" table to store all of the DAX formulas we create.
* In the Home tab of the Desktop ribbon, click Enter Data. This will pop up a screen that allows you to manually enter data.
* We are going to rename the column to Measures and then rename the table name at the bottom to Measure Table. See the screenshot below.

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Create%20Measures%20Table%201.png)

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/New%20Table.png)

## Creating New Measures:
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/New%20Measure.png)

There is multiple ways you can go about creating new measures "DAX" functions in Microsoft Power BI. We will go about it using the following method:
* Go to the "Modeling" Tab at the top of your screen.
* Click the "New Measure" button.
* A blank formula bar should open up and this is where you will create your new DAX measure.
* Copy and paste the "Total Sales" formula below and paste it into the empty formula bar.
* Format measure using the formatting options under the "Measure Tools" tab at the top of the page.
    - ![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Formating%20Measures.png)
    - make sure you store the measure under the "Measures Table" we created above.
* Click the "check mark" once you're done.
* You then should see the formula propogate under the "Measures Table"
* Repeat this process with the remaining formulas below.

```
Total Sales =
    -- create total sales:
    SUM('Dataset'[Unit Sales]
)
```

```
Current Month Sales = 
-- calculate the latest value of the metric you're wanting to evaluate:
    CALCULATE(
        'Measures Table'[Total Sales],
        -- use the MAX() function to filter the data to grab the value from the lastest month:
        Calendar_Complete[Month Number]=MAX(Calendar_Complete[Month Number])
)
```

```
Previous Month Sales = 
    --calculate the previous month value of the metric you're wanting to evaluate:
    CALCULATE(
        'Measures Table'[Total Sales],
        -- extract the previous month sales value:
        Calendar_Complete[Month Number]=(MAX(Calendar_Complete[Month Number])-1)
    )
```

```
Sales Growth Rate % = 
    --calculate the month to month sales growth rate:
    DIVIDE(
        ([Current Month Sales]-[Previous Month Sales]),
        [Previous Month Sales]
)
```

```
Price = 
    -- create price measure:
    DIVIDE(SUM('Dataset'[Dollar Sales]),'Measures Table'[Total Sales]
)
```

```
Current Month Sales No Blank =
    -- return 0 if blank:
    IF([Current Month Sales]=BLANK(),0,[Current Month Sales])
```

```
Previous Month Sales No Blank =
    -- return 0 if blank
    IF([Previous Month Sales]=BLANK(),0,[Previous Month Sales])
```

```
Switch_True_Function = 
-- set switch true function:
SWITCH(TRUE(),
-- create first logical condition:
[Current Month Sales]=BLANK(),0,
-- create second logical condition:
[Previous Month Sales]=BLANK(),0,
--otherwise return the Sales Growth Rate %:
'Measures Table'[Sales Growth Rate %]<>BLANK(),'Measures Table'[Sales Growth Rate %]
)
```

# Data Visualization:
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Data%20Visualization2.png)
Let's add a color background theme to our report.
* Click into the blank white canvas
* Under the "Visualization" pane, click "Format Your Report"
* Go to "Wallpaper" Then Click Browse and find where you stored the background image on your computer.

![SreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/format%20your%20report.png)

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/format%202.png)

Your report canvas should now look like the following:
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Back%20Ground%20Color.png)

We now will start building our first report using the following visuals:
* Area chart
* Line and Stacked column chart
* Slicer
* KPI Cards

## Area Chart:
* Click the "Area Chart" and you should see it populate into the blank canvas
* Resize to your preference.
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Drag%20and%20Drop%201.png)

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/save%202.png)

* Drag and drop "Month Name" from the "Fields" pane into the X-Axis.
* Drag and Drop "Total Sales" from the "Fields" pane into the Y-Axis.
* Drag and Drop "Geography" from the "Fields" pane into the Legend.

Your Area chart should look like the following below:

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Fields%20First.png)

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Area%20Chart%201.png)

You can format the chart to your liking.

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Area%20Chart%20Final.png)

## KPI Cards:
* Click the "KPI Card" visual and you should see it populate into the blank canvas.
* Copy the Blank KPI Card by clicking on it and pressing CTRL C. Then CTRL V to paste it two more times.
* Resize to your liking.
* Drag and drop the following measures into each of the KPI cards.
    - Current Month Sales No Blank "Rename to Current Month Sales"
    - Previous Month Sales No Blank "Rename to Previous Month Sales"
    - Switch_True_Function "MoM Growth Rate %"
* Format to your liking.

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/KPI%20Card1.png)

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Resize%20and%20Drop%203.png)

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/KPI%20Final.png)

Your report should look similar to the following depending on how you formatted your report so far.
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/2nd.png)

## Line and Stacked Column Chart:
* Click the "Line and Stacked Column Chart" button under the "Visualization" pane.
* Add in the following columns/measures:
    - Month Name
    - Dollar Sales
    - Price
    - Brand Name
* Format the visual to your liking.
* Your report should now look similar to the one below:

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Report%203.png)

## Slicers:
* Click the "Slicer" visual under the "Visualization" pane.
* Copy the Blank "Slicker" visual by clicking on it and pressing CTRL C. Then CTRL V to paste it six more times.
* Resize to your liking.
* Add in the following attributes:
    - Category
    - Custom Type Value "Rename to Product Type"
    - Brand Name
    - Custom Size Value "Renamed to Size"
    - Custom Count Value "Renamed to Count"
    - Product
* To rename a column, double click into the column name, then you should be able to rename it.

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/double%20click%20into%20column%20name.png)

Your report should look similar to the following:

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/final4.png)

# Data Visualization Continued: Connecting to Live Data Source
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/live%20data%20source.png)

before we create our next report, lets connect to our data source which now be a live connection.
* Go to the "Home" tab, "Get Data" then "Power BI datasets"
* ![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/live%20data%20source2.png)

You are then brought to the "Data Hub":
* You can see which live datasets you have access to.
* For our purposes, let's connect to the "300. Order to Cash Dataset".
* ![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Data%20Hub.png)

## Creating New Measures Continued:
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/New%20Measure.png)

### Common Microstrategy Table:
We're going to start with building a common MS table used by many aspects of the business.

![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/MS%20Table.png)

we need a way to display measures as columns in a table we can do this by doing the following:
* Create a Metrics table to reference which metrics we want data displayed for.
* Create a DAX function that will operate like a list to bring in the data for the metrics in our metrics table.

### Creating Metrics Table:
To create the metrics table, do the following:
* Under the "Home" tab, click "Enter Data".
* Then type in all the metrics you wanted to display in the columns field, add a column for each new metric you want to display.
    - Gross Sales
    - Sales Discount
    - Net Sales
    - Bill Cases
    - Bill Lbs
    - Bill Gross Lbs
    - Bill KG
    - Bill Liters
* Rename Table to be "Metric"
* Your table should look like the following:
    - ![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Metric.png)

* Now lets create our Metric Select DAX Function to help us bring in the data of the columns above.
```
Metric Selector = 
VAR TEP=MAX(Metric[Metric])
RETURN
SWITCH (
    TEP,
    "Gross Sales", [Gross Sales],
    "Sales Discount",FORMAT([Sales Discount],"Currency"),
    "Net Sales", FORMAT([Net Sales],"Currency"),
    "Bill Cases", [Bill Cases],
    "Bill Lbs", [Bill Lbs],
    "Bill Gross Lbs", [Bill Gross Lbs],
    "Bill KG", [Bill KG],
    "Bill Liters", [Bill Liters]
)
```

Click on the "Matrix" visual and resize to your preference, then add in the following columns and measures:
* ROWS:
    - Brand
    - Pack Group
    - Pack Group Code
* Columns:
    - Bill Date
* Values:
    - Metric Selector
* Your visual should look like the following:
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/following.png)
* Turn off the following options:
    - Click "Format Your Visual" under the Visualization Pane
    - Scroll down to Row Headers and make sure "+/-" is turned off and "Stepped layout" is turned off.
    - ![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Row%20Headers.png)
* If you want to change the display view of the matrix table to the following:
    - Go the Visualization" Pane.
    - "Style presets"
    - From there you can choose the different style options in the drop down.
    - If you want to match the style I have then select the "Alternating rows" option.
You should now see the following Microstrategy table replicated in Microsoft Power BI.
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Matrix%20MS%20Table.png)

## Scatter Chart 2:
Next we will create a scatter Cart using the data from our live connection.
* Click the "Scatter Chart" Visual under the Visualization Pane.
* ![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/ScatterPlot%20Visualization%20Pane.png)
* Drag and drop the following columns into your Visualization pane:
    - Values: Product Type
    - X Axis: Sales Discount
    - Y Axis: Ship Dollars
    - Order Type: Legend
    - Size: COGS
* ![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/COGS.png)
* You can go to the "Visualization" Pane and format the scatter chart settings to your preference.
    - ![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/For.png)
* Your final Scatter Chart should look similar to mine. It won't look exactly the same unless you replicate the exact formatting that I did. We don't cover the steps for formatting a visual as this is more of a personal preference then practice. What I think might look good formatting wise might not be the same what you think looks good.
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/SCatter%20Plot%20Final.png)

## Table:
Next, we will create a basic table but use the icon feature in Power BI to display Green, Yellow, or Red depending on the sales discount given. To do this please do the following:
* Go to the "Modeling" Tab at the top of your screen.
* Click the "New Measure" button.
* A blank formula bar should open up and this is where you will create your new DAX measure.
* Copy and paste the following two formulas and create two seperate measures:
```
Average Sales Discount = AVERAGE('`Order to Cash'[Sales Discount])
```

```
Sales Discount Type = 
    SWITCH(TRUE(),
    -- first condition:
    [Average Sales Discount]>=-100,"TrafficHighLight",
    -- second condition:
    [Average Sales Discount]<0 && [Average Sales Discount] >=200, "TrafficMediumLight",
    -- third condition:
    [Average Sales Discount]<-100, "TrafficLowLight"
)
```
* Format measure using the formatting options under the "Measure Tools" tab at the top of the page.
    - ![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Formating%20Measures.png)
    - make sure you store the measure under the "Measures Table" we created above.
* Click the "check mark" once you're done.
* You then should see the formula propogate under the "Measures Table"
* We will then select the "Table" visual under the "Visualization" pane and make sure your columns match mine:
    - ![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Table%20Icon.png)
* Next, we will take the measure we created above called "Sales Discount Type" and apply it to our table to display the icons.
    - Go the Visualization Pane.
    - Scroll down to "Cell Elements"
    - Change the "Series" to "Sales Discount"
    - Turn the Icons button to "On"
    - Then Click the "fx"
    
    -![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Icons.png)

* You then will be prompt with the following Icon screen:
    - please make sure your "Format Style" is set to "Field Value".
    - Apply to is set to "Values Only"
    - What Field should we base this on? "Sales Discount Type"
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Field%20and%20Icons.png)

* Format the visual to your liking and the final result should look similar to mine minus the formatting choices:
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Final%20Icons.png)

## Slicers:
* Click the "Slicer" visual under the "Visualization" pane.
* Copy the Blank "Slicker" visual by clicking on it and pressing CTRL C. Then CTRL V to paste it six more times.
* Resize to your liking.
* Add in the following attributes:
    - Bill Year
    - Business Unit
    - Brand
    - Plant Type
    - Customer
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Slicers%202.png)

You're final report should look similar to mine below. It will look slighty different depending on the formatting you choose to go with.
![ScreenShot](https://github.com/NavarroAlex/NORAM-Microsoft-Power-BI-Training/blob/main/Final%20Report%202.png)
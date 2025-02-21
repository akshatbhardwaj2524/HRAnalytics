1# HRAnalytics
A repo for a project that analyses trends and gathers insights from the employee attendance at an organisation and also accomodates for new data to be entered

Step wise description 
Step 1:
We are provided with an excel sheet of employee data for leave, WFH and half day records of the employees.Our goal in thes project is to find the correlation of leaves,
sick leave % and carry out the organization of the data in such a away that it is easier to edit and look at in the future even if it is looked at by an employee/HR not
experienced in data analytics.

Step 2:
The excel sheet is loaded into the power BI desktop app and is transformed to include the headers. Power Query is used in this case, Power Query is the Data engineering
tool in Power BI.
Now we have the table in Power Query. We now duplicate the data and create a template such that we can always insert new data. We are also transforming the data i.e.
column headers and using the dates in one single column rather thana as the headers in the excel file.
Before : 
              |1-1-2022|2-1-2022|3-1-2022|
After:
              |1-1-2022|
              |2-1-2022|
              |3-1-2022|
For that we have to transform the data
After the transformation of the data, we have information and data of the worksheets present in the excel workbook. We now apply several steps.
  i) Duplicate thte query and rename it as template as it will be used for transform and analyse the data added in the future.
 ii) We now filter out unnecessary columns and access the table for APR 2022 to transform and then apply to all data.
iii) We change the headers and remove unneccesary rows.
Now we start to transform the data. First ste is to unpivot the data i.e. I tranform the headers into rowsas previously mentioned(with the dates).
This is done using unpivot in the data transformation tools.
When I follow up with the previous step we also get some non-date and unnecessary data. This can be dealt with if we change the type of date column to date. Thus we can see
the transformation has helped us in removing unnecessary information.
After that we remove errors and now we have a clean sheet.

***When you are excluding/transforming data, always think of a dynamic way so that it will work even with new data.***

We can then create a Parameter named worksheet as and type as text, value as APR 2022.
For the purpose of getting new data and arranging it, we create a function which has all of the steps we did previously and can bew applied on the new data instantly.
We got an error in the function and now we have to clear the error (it was referencing Date column) to clear it we deleted the step where the data is referenced.
Now we load the data but first we invoke the function when it is done, we solve the above error and load the data (disable the loading of the template). We now
have the data in power BI.

 Step 3:
 

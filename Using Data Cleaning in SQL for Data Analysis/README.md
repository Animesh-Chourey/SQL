# Using Data Cleaning in SQL for Data Analysis

## Goal:
The project focuses on analyzing the sales data for the duration of three months. For this analysis, firstly, the database will be extracted using SQL.

#### Steps:-
* In the Products table, deleted the duplicate rows of QuantityPerUnit, with a ROW_NUMBER() function and CTE.
* Created a variable 'WhenToRestock' specifiying to -> 
    * 'Restock Now' : when the condition UnitsOnOrder > 50 and when UnitInStock < 20 using a CASE statement.
    * 'Restock Next Week' : when the condition UnitsOnOrder is between 30 and 40, and when UnitInStock < 50 using a CASE statement.
    * 'Restock Next Month' : when the condition UnitsOnOrder < 30 and when UnitInStock <50 using a CASE statement.
    * 'Restock In 6 Months' : when the condition UnitsOnOrder < 5 and when UnitInStock >= 50 using a CASE statement.
    *  Else 'WhenToRestock' : specifies 'Ask Manager
* From the Customers table, selected CustomerId, ContactName, City, Region, fax, and replace Fax with 'No Fax Specified' when Fax is Null in the Customers table. Also, selected only those rows with the label Fax = 'No Fax Specified' using a CTE.

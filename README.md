# Data-Cleaning

## Data Cleaning with Microsoft Excel / Power Query

### The aim of this project:
Data integrity or consistency is an important aspect of data analytics because a dirty or inconsistent data can lead to poor analysis. Imagine working for an accounting firm as a data analyst and you are tasked with the job of analyzing their quarterly generated data that will help understand their growth and KPI.
The problem is not the analysis, but the consistency of the data used for the analysis. A dirty data will make all your findings and analysis incorrect, and if the firm uses your findings from an inconsistent data to make decisions it will in return lead to a catastrophic outcome. 
The necessity of a clean data cannot be over emphasized because it is the skeleton to your analysis.

### Manual method of data cleaning.

#### Task 1
Extract just the first name from the Name column.

* Solution:
This can be achieved by creating a new column called "first name" and then type out the first names till an auto fill option is given by excel that will reduce the stress of typing out the names individually. 
This functionality is call "FLASH FILL".

* Limitation
The limitations of flash fill is the ability to include the error data in the auto fill, and it is manual.

#### Task 2
The EmpID column contains data like this PR00147, where PR = Cost Center, and 00147 = Employee Number, split the data into two different fields/column.

* Solution:
Text to column is another way of spliting data not just by dilimiter but also by fixed width, with the text to column function in excel we can split EmpID with fixed width.

#### Task 3
Removing Duplicate Values:

* Solution:
From my observation I noticed that the name columns contains some duplicate data, by using the remove duplicate function in the data ribbon we can manually remove every duplicate.

##### Limitations of manually cleaning data:
The above methods of data cleaning are not sustainable because they a manually done and when one data changes we'll have to manually input the data instead of updating automatically.


### Formula method of data cleaning:

#### Task 1
Remove the extra spaces in the name column with the TRIM function.

* Solution:
Using the TRIM formula to erase spaces in data, this function removes any extra unnecessary space in the data.
Some of the names in the name column has space in front or after the names, this method is very necessary in assuring data consistency.

#### Task 2
The FTE column contains data that indicates whether an employee is workig FULL-TIME or PART-TIME. 

* Solution:
In a situation where the FTE number is less than 1 then the employee is a part-time employee, and if the FTE number is 1 or above the employee is a full-time employee.
This can be done using the IF function.

##### Importance of formula method of data cleaning:
The formula data cleaning is completely dinamic to data changes, so when there's a change in the data it updates automatically.


### Power Query method of data cleaning:
This step can be done by creating a table from the worksheet and extracting the table into power query for cleaning.

#### Task 1
Split the EmpID into Cost Center and Employee Number

* Solution
The first step is to split the employeeID into two different parts, this can be done by selecting the EmpID column and right clicking, this will display an option for spliting column by delimiter, Number of characters, Position, Lowercase to Uppercase, Digit to Non-Digit, and Non-Digit to Digit.

#### Task 2
Correct the Start Date column due to its inconsistency in Date.

* Solution
Highlight the column, right click and select change data type to date.

#### Task 3
The next task is to confirm if an employee is a fulltime or part time employee using the FTE column. 

* Solution
This can be done by selecting the conditional column in the Add column ribbon in power query. The IF function is used in this situation.

#### Task 4
The next step is to find and replace the "Null Values" with "Other". 

* Solution
This can be done by selecting the column and right clicking, select replace value.

The next step is to remove every "null" values in the Department column, this can be done by unchecking the null data from the filter.

##### Importance of power query data cleaning:
Power query data cleaning method is the most reliable, efficient, and stress free way of cleaning an inconsistence data beacuse every step taken is recorded and stored by power query, in return it makes it easier to add inconsistent data to the already cleaned table without repeating the whole cleaning process again. By simply refreshing the table whenever a new data is added to it will automatically clean the data using the already stored cleaning procedures.



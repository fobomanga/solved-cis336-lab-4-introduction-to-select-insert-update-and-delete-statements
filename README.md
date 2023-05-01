Download Link: https://assignmentchef.com/product/solved-cis336-lab-4-introduction-to-select-insert-update-and-delete-statements
<br>
Lab 4 will introduce the various aspects of the SQL select statement and the methods of retrieving data from the database tables. This lab will also introduce the fundamentals of updating and deleting records. This lab may be completed using either DeVry’s Omnymbus EDUPE-APP lab environment, or a local copy of the MySQL database running on your own computer using the OM database tables. The lab will utilize a set of tables that are represented by the ERD (OM_ERD.docx) and are created and populated by the script file (create_OM_db.sql).  Follow the instructions in the file CreateOMTables.docx to create your database, tables, and data.

A few IMPORTANT things to note if using EDUPE MySQL:

**There can be NO SPACES in alias names given to a column.  For example:

Select unit_price as “Retail Price “ from items;  –this does NOT work in EDUPE MySQL.

Any of the following WILL WORK:

Select unit_price as “RetailPrice” from items;

Select unit_price as “Retail_Price” from items;

Select unit_price as Retail_Price from items;

Select unit_price as RetailPrice from items;

**Any calculated fields MUST be given an alias (and note above NO SPACES in alias).  For example:

selectunit_price * 2 from items;   –this does NOT work in EDUPE MySQL

This will work:

selectunit_price * 2 as NewPricefrom items;

Deliverables

<ul>

 <li>Lab Report (Answer Sheet) containing both the student-created SQL command(s) for each exercise, and the output showing the results obtained. Be sure your name is on the file.</li>

</ul>

LAB STEPS:  Complete each of the exercises below.

<ul>

 <li>Write a query that displays a list of all customers showing the customer first name, last name, and phone number.  Sort the results by customer last name, then first name.</li>

 <li>Write a query that displays each customer name as a single field in the format “firstnamelastname” with a heading of Customer, along with their phone number with a heading of Phone.  Use the  IN operator to only display customers in New York, New Jersey, or Washington D.C.  Sort the results by phone number.</li>

 <li>Write a query that will list all the cities that have customers with a heading of Cities.  Only list each city once (no duplicates) and sort in descending alphabetical order.</li>

 <li>Write a query that displays the title of each item along with the price (with a heading of Original) and a calculated field reflecting the price with a 25% discount (with a heading of Sale).Display the sale pricewithtwo decimal places using the ROUNDfunction.  Sort by price from lowest to highest.</li>

 <li>Write a query that displays the customer_first_name, customer_last_name, and customer_city from the customers table.  Use the LIKE operator to only display customers that reside in any zipcode beginning with 4.</li>

 <li>Write a query that displays the order id and order date for any orders placed from March 1, 2014 through April 30, 2014.  Do this WITHOUT using the BETWEEN clause.  Format the date field as Month dd, yyyy and use a heading of “Ordered”.</li>

 <li>Write a query that displays the order id and order date for any orders placed during the month of May, 2014.  Do this using the BETWEEN clause.  Format the date field as mm/dd/yy and use a heading of “Ordered”.</li>

 <li>Write a query which displays the order id, customer id, and the number of days between the order date and the ship date (use the DATEDIFF function).  Name this column “Days” and sort by highest to lowest number of days.  Only display orders where this result is 15 days or more.</li>

 <li>Write a query which displaysthe order id, customer id and order date for all orders that have NOT been shipped, sorted by order date with the most recent order at the top.</li>

 <li>The Marketing Department has requested a new report of shipped orders for which the order was placed on either a Saturday or a Sunday.Write a query which displays the order id, order date, shipped date, along with a calculated column labeled “Order_Day” showing the day of the week the order was placed (use the DAYNAME function).  Only display orders that have shipped and were placed on a Saturday or Sunday.  Sort by order date with most recent orders at the top.</li>

 <li>Write a query to display the customer last name, phone number, and fax number but only display those customers that have a fax number.</li>

 <li> Create astatement to insert a new record into the items table with the following values:</li>

</ul>

<table>

 <tbody>

  <tr>

   <td>item_id:</td>

   <td>11</td>

  </tr>

  <tr>

   <td>title:</td>

   <td>Ode To My ERD</td>

  </tr>

  <tr>

   <td>Artist_id:</td>

   <td>15</td>

  </tr>

  <tr>

   <td>unit_price:</td>

   <td>12.95</td>

  </tr>

 </tbody>

</table>

ShowyourINSERT statement along with the results of the followingSELECT query to verify that the insert worked correctly.

select * from items where item_id&gt; 10;

<ul>

 <li>Create astatement to update the record inserted in the previous step to change the unit price of this itemto 7.95.</li>

</ul>

<table>

 <tbody>

  <tr>

   <td>item_id:</td>

   <td>11</td>

  </tr>

  <tr>

   <td>title:</td>

   <td>Ode To My ERD</td>

  </tr>

  <tr>

   <td>artist:</td>

   <td>15</td>

  </tr>

  <tr>

   <td>unit_price:</td>

   <td>7.95</td>

  </tr>

 </tbody>

</table>

Show yourUPDATE statement along with the results of the followingSELECT query to verify that the insert worked correctly.

select * from items where item_id&gt; 10;

<ul>

 <li>Create a statement to delete the entire record that was inserted and then updated in the previous steps.</li>

</ul>

Show your DELETE statement along with the results of the following SELECT query to verify that the insert worked correctly.

select * from items where item_id&gt; 10;

Using the SUBSTRING and CONCAT functions, write a query to display each customer name as a single field in the format “Jones, Tom” with a heading of Customer along with the customer_phone field in a nicely formatted calculated column named Phone. For example, a record containing the customer_phone value 6145535443 would be output with parentheses, spaces, and hyphens, like this: (614) 555-5443.  Sort by last name.

This is the end of Lab 4.
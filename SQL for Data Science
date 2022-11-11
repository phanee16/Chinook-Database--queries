########### SQL basics ##########

---------------------------------------------------------------------------------------------------------
Question 1
Retrieve all the records from the Employees table.
<<<<<<<<<<<<<<<<<<
SELECT *
FROM Employees
>>>>>>>>>>>>>>>>>>

---------------------------------------------------------------------------------------------------------
Question 2
Retrieve the FirstName, LastName, Birthdate, Address, City, and State from the Employees table.
<<<<<<<<<<<<<<<<<<
SELECT FirstName,LastName,Birthdate,Address,City,State
FROM Employees
>>>>>>>>>>>>>>>>>>

---------------------------------------------------------------------------------------------------------
Question 3
Retrieve all the columns from the Tracks table, but only return 20 rows.
<<<<<<<<<<<<<<<<<<
SELECT *
FROM Tracks
LIMIT 20
>>>>>>>>>>>>>>>>>>
---------------------------------------------------------------------------------------------------------
#######   SQL queries based on conditions ######

---------------------------------------------------------------------------------------------------------
Question 1
Find all the tracks that have a length of 5,000,000 milliseconds or more.
<<<<<<<<<<<<<<<<<<
SELECT *
FROM Tracks
WHERE Milliseconds >= 5000000
>>>>>>>>>>>>>>>>>>

---------------------------------------------------------------------------------------------------------
Question 2
Find all the invoices whose total is between $5 and $15 dollars.
<<<<<<<<<<<<<<<<<<
SELECT *
FROM Invoices
WHERE Total BETWEEN 5 AND 15
>>>>>>>>>>>>>>>>>>

---------------------------------------------------------------------------------------------------------
Question 3
Find all the customers from the following States: RJ, DF, AB, BC, CA, WA, NY.
<<<<<<<<<<<<<<<<<<
SELECT *
FROM Customers
WHERE State IN ('RJ','DF','AB','BC','CA','WA','NY')
>>>>>>>>>>>>>>>>>>

---------------------------------------------------------------------------------------------------------
Question 4
Find all the invoices for customer 56 and 58 where the total was between $1.00 and $5.00.
<<<<<<<<<<<<<<<<<<
SELECT *
FROM Invoices
WHERE (CustomerId = 56 OR CustomerId=58) AND (Total BETWEEN 1 AND 5)
>>>>>>>>>>>>>>>>>>

---------------------------------------------------------------------------------------------------------
Question 5
Find all the tracks whose name starts with 'All'.
<<<<<<<<<<<<<<<<<<
SELECT * 
FROM Tracks
WHERE Name LIKE 'All%'
>>>>>>>>>>>>>>>>>>

---------------------------------------------------------------------------------------------------------
Question 6
Find all the customer emails that start with "J" and are from gmail.com.
<<<<<<<<<<<<<<<<<<
SELECT *
FROM Customers 
WHERE Email LIKE 'J%@gmail.com'
>>>>>>>>>>>>>>>>>>

---------------------------------------------------------------------------------------------------------
Question 7
Find all the invoices from the billing city Brasília, Edmonton, and Vancouver and sort in descending order by invoice ID.
<<<<<<<<<<<<<<<<<<
SELECT *
FROM Invoices
WHERE BillingCity IN ('Brasilia','Edmonton','Vancouver')
ORDER BY InvoiceId DESC
>>>>>>>>>>>>>>>>>>

---------------------------------------------------------------------------------------------------------
Question 8
<<<<<<<<<<<<<<<<<<
Show the number of orders placed by each customer (hint: this is found in the invoices table) and sort the result by the number of orders in descending order.
SELECT COUNT(InvoiceId) as cnt
FROM Invoices
GROUP BY CustomerId
ORDER BY InvoiceId DESC
>>>>>>>>>>>>>>>>>>

---------------------------------------------------------------------------------------------------------
Question 9
<<<<<<<<<<<<<<<<<<
Find the albums with 12 or more tracks.
SELECT COUNT(TrackId) as cnt
FROM Tracks
GROUP BY AlbumID
HAVING cnt>=12
>>>>>>>>>>>>>>>>>>

---------------------------------------------------------------------------------------------------------
####### SQL queries using JOINS ######

---------------------------------------------------------------------------------------------------------
Question 1
Using a subquery, find the names of all the tracks for the album "Californication".
<<<<<<<<<<<<<<<<<<
SELECT TRACKS.TRACKID,TRACKS.NAME FROM TRACKS
JOIN ALBUMS ON ALBUMS.ALBUMID = TRACKS.ALBUMID
WHERE ALBUMS.TITLE = 'Californication'
>>>>>>>>>>>>>>>>>>

---------------------------------------------------------------------------------------------------------
Question 2
Find the total number of invoices for each customer along with the customer's full name, city and email.
<<<<<<<<<<<<<<<<<<
SELECT CUSTOMERS.CUSTOMERID,CUSTOMERS.FIRSTNAME,CUSTOMERS.LASTNAME,CUSTOMERS.CITY,CUSTOMERS.EMAIL,SUM(INVOICES.INVOICEID)
FROM CUSTOMERS JOIN INVOICES ON CUSTOMERS.CUSTOMERID = INVOICES.CUSTOMERID
GROUP BY CUSTOMERS.CUSTOMERID
>>>>>>>>>>>>>>>>>>

---------------------------------------------------------------------------------------------------------
Question 3
Retrieve the track name, album, artistID, and trackID for all the albums.
<<<<<<<<<<<<<<<<<<
SELECT TRACKS.NAME, ALBUMS.TITLE,ALBUMS.ARTISTID, TRACKS.TRACKID
FROM ALBUMS JOIN TRACKS ON TRACKS.ALBUMID = ALBUMS.ALBUMID
>>>>>>>>>>>>>>>>>>

---------------------------------------------------------------------------------------------------------
Question 4
Retrieve a list with the managers last name, and the last name of the employees who report to him or her.
<<<<<<<<<<<<<<<<<<
SELECT* 
FROM EMPLOYEES LIMIT 10
>>>>>>>>>>>>>>>>>>

---------------------------------------------------------------------------------------------------------
Question 5
Find the name and ID of the artists who do not have albums. 
<<<<<<<<<<<<<<<<<<
SELECT ARTISTS.ARTISTID,ARTISTS.NAME,ALBUMS.ALBUMID
FROM ARTISTS LEFT JOIN ALBUMS ON ALBUMS.ARTISTID= ARTISTS.ARTISTID
WHERE ALBUMS.ALBUMID IS NULL
>>>>>>>>>>>>>>>>>>

---------------------------------------------------------------------------------------------------------
Question 6
Use a UNION to create a list of all the employee's and customer's first names and last names ordered by the last name in descending order.
<<<<<<<<<<<<<<<<<<
SELECT CUSTOMERS.FIRSTNAME,CUSTOMERS.LASTNAME 
FROM CUSTOMERS
UNION 
SELECT EMPLOYEES.FIRSTNAME,EMPLOYEES.LASTNAME
FROM EMPLOYEES
ORDER BY CUSTOMERS.LASTNAME DESC
>>>>>>>>>>>>>>>>>>

---------------------------------------------------------------------------------------------------------
Question 7
See if there are any customers who have a different city listed in their billing city versus their customer city.
<<<<<<<<<<<<<<<<<<
SELECT CUSTOMERS.CITY, INVOICES.BILLINGCITY
FROM CUSTOMERS
JOIN INVOICES ON INVOICES.CUSTOMERID = CUSTOMERS.CUSTOMERID
WHERE CUSTOMERS.CITY!= INVOICES.BILLINGCITY
>>>>>>>>>>>>>>>>>>

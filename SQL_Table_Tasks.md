Employees Table
EmployeeID	FirstName	LastName
1	John	Doe
2	Jane	Smith
3	Alice	Johnson

Products
ProductID	ProductName	ProductDescription
(101,	'Widget A',	A standard widget'),
(102,	'Gadget B',	A fancy new gadget'),
(103,	'Thingamajig',	'A very useful tool');


SalesOrders Table
SalesOrderID	OrderDate	TotalAmount
(1001, '2023-01-15 14:33:00', 150.00),
(1002, '2023-03-22 10:45:00', 200.00),
(1003, '2024-05-17 09:20:00', 350.00);


Customers Table
(CustomerID,CustomerName,Address)
(201,	Acme Corp,	123 Main St)
(202,	Globex Inc,	456 Elm St)
(203,	Initech	,789 Oak St)



## Team Tasks
Task - 1
Employees Table
(EmployeeID,FirstName,LastName,DepartmentID)
(1,	John ,Doe , 101),
(2,	Jane ,Smith, 102),
(3,	Alice, Johnson, 103);

Departments Table
(DepartmentID, DepartmentName)
(101, Sales),
(102, Engineering),
(103, Marketing);



# Task 4
Exercise 4: Enhanced Product Search
Scenario: Write a query to find products where the description contains the word "useful" and replace the word "useful" with "beneficial". Return the product ID, product name, and modified description.

Tables:

Products (ProductID, ProductName, ProductDescription)
Expected Result:

ProductID, ProductName, ModifiedDescription
Example Data:

Products Table
ProductID	ProductName	ProductDescription
101	Widget A	A standard widget
102	Gadget B	A fancy new gadget
103	Thingamajig	A very useful tool
Expected Output:

ProductID	ProductName	ModifiedDescription
103	Thingamajig	A very beneficial tool
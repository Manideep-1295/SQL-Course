## What is a Database?

A Database is a software used to store data in any form.

## Why we need special software?

### Database lives in cloud

A cloud is a renting pc
Cloud Storage providers are not the cloud.
A server is a group of PC's

Linux is used in cloud

### Advantages of Linux

1. Free
2. Open-Source - All are travelling on the same boat, thats why its important
3. Security
4. Smaller footprint
5. Automation - Can be controlled all operations from the terminal, you wont even need a mouse.

Distro of linux :

- Linux Mint
- Ubuntu etc

## Features of Database

1. Database - Frequently asked data, it will have it in the ram
2. Querying becomes easy
3. CRUD - easy
4. Backups are inbuilt
5. Undo - easily (time limit)
6. Performance (As storing in the RAM)



# SQL Theory
## Keys

- Primary Key :
  1. Should be UNIQUE
  2. Should be NOT NULL
  3. Only one column a table should be PK
-

## Normalization

To avoid anomolies we do normalize the tables or
To increase the safety of the data

Types of Normal Forms:

1.  1st Normal Form
    ![1NF](./Images/image-5.png)
    Row order should not contain any information.
    Dont mix Data types within the same column
    Table without primarykey is not allowed
    Repeating groups are not permitted

    #### Task 1 (Convert to NF)
    ![Task-1](./Images/image-6.png)

    player_id | Inventory | Quantity|
    -|-|-|
    abc|rings|2|
    xyz|shields|3|

    Primary Key - Combinely id and inventory (Composite Key)
    or else we can create a new primary key column.
    

2. 2nd Normal Form  
    Insertion, Updation & Deletion Anamoly  
    ![Table](./Images/image-7.png)

    ![Overcoming Anamolies](./Images/image-9.png)
    **Note - No partial Dependency (Non-key Attribute must depend on the entire Primary Key)**

3. 3rd Normal Form  
    Lesser updates, More safer data.
    ![alt text](image-10.png)
  (3.5 NF)BCNF - Every attribute should depend on Key attribute

## JOINS
![Venn Diagrams](./Images/image-11.png)
```sql
-- Syntax/Formula for join
-- A JOIN B ON Pk = Fk;
```
#### Why Joins required?
- For safety we are dividing the tables(Normalization), to fetch the data from other tables we are joining the tables(De-Normalization).
## Types of JOINS
1. Inner Join
2. Outer Join
    - Left Outer Join (A - B)
    - Right Outer Join (B - A)
    - Full Join

### More Types of Joins
1. Cross Join - All possible combinations
2. Inner Join  
    1. Natural Join - No condition required, Column names in both table should be same  //Not in SSMS
    2. Equi Join - No need to put "=" -> (col1,col2)  //Not in SSMS
    c. Inner Join - We can use relational operators also instead of =  
    3. Self Join - Joining table with itself



## Aggregates
Aggregation nothing but summarization

**Clue - If there is every x in the question then GROUP BY x comes into picture.**
**It is used to drill down to the next level**

## Query Order of Execution
![Order of Execution](./Images/image-17.png)


## WHERE vs HAVING
WHERE checks for the condition in row wise
whereas HAVING is used to more drill down the problem after grouping the table with a condition.

## Types of Keys 
![Keys](image-2.png)
Candidate Key - Which columns have the potential to be PK, Those all columns are combinely called Candidate Key  
Alternate Key - (CK - PK)  
Super Key - Its a group of keys which identifies rows in a table.  
Composite Key - Combinely 2 columns are considered as PK when there is no PK in the table.  

## INDEX
Index is used for faster retrival of data
1. Clustered Index - By Default for primary keys
2. Non Clustered Index - By Default for non key attributes

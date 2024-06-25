AGENDA :
Subqueries
Co-Related SubQueries
Adv Joins
Sets
Operators (All, Any, Exists)

Group By HAVING
ORDER BY

## Ranking Functions

-- 1. Rank
-- 2. Dense_Rank
-- 3 Row_Number
-- 4. N

AGENDA (21-6-24):

1. VIEWS
2. FUNCTIONS
3. CASE (Control Flow)

## Types of User Defined Functions

1. Scalar Functions
2. Inline Table Valued Function
3. Multiple Table Valued Function
   Can only do DML operations on the table mentioned inside the function

> Insert through select statement

```sql
INSERT INTO TABLE_NAME
SELECT * FROM TABLE_NAME2
```

```sql
-- 1. Scalar
Go
Create Function dbo.CalculateAge(@ReleaseDate Int)
Returns Int
As
Begin
  Return Year(GetDate()) - @ReleaseDate;
End
Go

Select dbo.CalculateAge(2000);


-- 2. ITVF - Inline
Go
Create Function dbo.GetMovieByGenre(@Genre nvarchar(30))
returns table
As
Return(
Select * from Movies
Where Genre = @Genre
)
Go

-- 3. MTVF

Create Function dbo.GetMoviesAfter2015()
Returns @LatestDecadeMovies Table(Title varchar(100), ReleaseYear Int, Genre varchar(20))
As
Begin
	Insert Into @LatestDecadeMovies
	Select Title, ReleaseYear, Genre  from Movies where ReleaseYear > 2015

	-- updates

	-- delete
	Return;
End

Select * from dbo.GetMoviesAfter2015()

Select * from dbo.GetMovieByGenre('Action')
Select * from dbo.GetMovieByGenre('Action Comedy')
```

## CASE WHEN

```sql
-- Simple CASE expression:
CASE input_expression
     WHEN when_expression THEN result_expression [ ...n ]
     [ ELSE else_result_expression ]
END

-- Searched CASE expression:
CASE
     WHEN Boolean_expression THEN result_expression [ ...n ]
     [ ELSE else_result_expression ]
END
```

## Stored Procedures

```sql
CREATE PROC spGetMoviesByGenre
    @Genre nVARCHAR(20)
    @
AS
BEGIN
    SELECT * FROM Movies
END
```

### Conditional Statements

1. IF ELSE

### LOOPS

1. WHILE

```sql
[17:36] Ragav Kumar V (Unverified)
-- Stored Procedures

Declare @OrderAmount Decimal(10, 2) = 1500.00

If @OrderAmount > 1000
Begin
	Print 'Applying 10% discount'
End
Else
Begin
	Print 'No Discount'
End
Declare @Counter Int = 10
While @Counter > 0
Begin
	Print @Counter
	Set @Counter = @Counter - 1
End
```

## Functions
### String Functions
```sql
-- 1. Len
Select Len('Manideep') as Length;
-- 2. Left
Select Left('Manideep',4) as Left_Name;
-- 3. Right
Select Right('Manideep',4) as Right_Name;
-- 4. substring - 1 INdexed
Select Substring('Manideep',5,8) as SUB_STR;
-- 5. Upper
Select Upper('manideep') as CAPITALIZE;
-- 6. Lower
Select Lower('MANIDEEP') as LOWER_CASE;
-- 7. Ltrim
Select Ltrim('        Manideep') as LeftTrim_BySpace;
Select Ltrim('12Manideep', '12M') as LeftTrim_Pattern;
Select Ltrim('        Manideep',2) as LeftTrim_ByNChar;
-- 8. Rtrim
Select Rtrim('Manideep        ') as S;
Select Rtrim('12Manideep34', '12') as P;
-- 9. CharIndex - Search
Select CharIndex('a','Mani deep is a cool guy');
-- 10. Replace
Select Replace('Manideep','d','D') as Replace_Char;
-- 11. Concat
Select Concat('Mani','Deep') as STRING;
-- 12. Replicate - repeat
Select Replicate('Hi ',5) as Repeat;
-- 13. Reverse
Select Reverse('manideep');
```

###  Math Functions
```sql
-- 1. Abs - +ve
Select Abs(-5)
-- 2. Power
Select Power(2,5)
-- 3. Round
Select Round(12.3456,2)
-- 4. Ceiling
Select CEILING(2.1)
-- 5. Floor
Select Floor(2.9)
```

### Date Functions
```sql
-- 1. GetDate
Select GetDate() as Today
-- 2. DateAdd
Select DateAdd(Year,10,GetDate()) as Future_Date
-- 3. DateDiff
Select DateDiff(day, '01-01-2024',GETDATE()) as Days_Completed
-- 4. Format
Select Format(GetDate(),'dd.mm.yyyy hh:mm:ss')
-- 5. DatePart - Extracts part of a Date
Select DatePart(month,GetDate()) as Month
Select DatePart(Day,GetDate()) as Day
```
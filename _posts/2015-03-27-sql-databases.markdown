---
layout: post
title:  "SQL: To Be Continued"
date:   2015-03-27 11:21:45
categories: sql databases
---

#**Wax On. Wax Off"**

![KarateKid][KarateKidWax]

#**Sensei says: "To master craft, spend less time doing not craft."**

![Zen Pic][ZenPic]

I spent most of this week reading through SQL resources and doing exercism exercises. Here are my SQL notes for the week:

**Set Operators:**
soundUnion, Intersect, Except
1.With from, you can add variables to make future clauses more readable
-For Example:
-select Student.sID, sName, GPA, Apply.cName, enrollment
2.from Student S, College C, Apply A
3.where A.sID = S.sID and A.cName = C.cName
4.Operator <>	→ “not equal” (i.e. S1.sID <> S2.sID;)
5.Union operator by default in SQL eliminates duplicates
-Use ‘all’ to retain duplicate with union, i.e. (union all)
6.Sub-queries are nested select statements, can be nested in the where clause
7.Some databases don’t support ‘all’ or ‘any’ expressions.  Use exists or not exists instead

**SQL Aggregation Clauses:**
1.Initially appear in the select clause, perform computations over multiple rows in a collection
2.Commonly supported aggregation functions: min, max, sum, avg, and count
3.‘Group By’ lets you create custom groups from an aggregate 
4.‘Having’ clause allows you to test filters for an aggregate set of values
5.Equality operator is only one ‘=’ for SQL Lite 
6.Any query that can be written with a ‘group by’ and ‘having’ clause can be written in another form, even if it’s strange 

**Null Values:**
1.Any value or attribute can take on Null, usually used for unknown or empty values
2.Wont return all dada with all inclusive equality operations if you have null values
3.Can get all data results if you include ‘is null’ in query
4.Will return items with null values if equality operator tests non-null attribute as well (i.e. using ‘or’ equality operators) 
5.Null items not included when counting distinct values
6.Null included when selecting distinct values 

**Join:**
1.Joins used in ‘from’ statement to take the cross product of two tables. Doesn’t add expressiveness to the SQL language
2.Inner Join: explicitly combine relations with a given condition takes the cross product of a table but only keeps the results that meet a condition 
3.Natural Join: implicitly equates columns across tables with the same name and eliminates duplicate columns
4.Inner Join Using(attrs): Like the natural join except you explicitly list the attributes you want equated
5.Left | Right | Full Outer Join: Similar to Inner Join but populates the table with null values where data doesn’t exist
6.Most SQL systems don’t allow a ‘using’ and an ‘on’ clause with a join
7.Left outer join takes any couples on left side of join and if they don’t have a matching couple on the right it’s padded with a null value.
8.Right outer join works like left outer join but goes the other way
9.Full outer join includes unmatched applied couples from both sides of the join
10.Can use left and right outer join to the same effect as full outer join


**Data Modification Statements:**
1.Two methods for inserting data
-Insert using specified values
-Run query over database with select statement and insert returned values
2.Deleting: Delete data where condition is met
3.Update→  Set Attr = Expression where Condition
-Can update multiple attributes in a tuple by including multiple sets
4.Helpful to perform searches first to verify correct database selection before updating and/or deleting


[KrateKidWax]: http://jargonfiles.files.wordpress.com/2013/02/waxonwaxoff.jpg

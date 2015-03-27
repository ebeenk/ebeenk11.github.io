---
layout: post
title:  "SQL: To Be Continued"
date:   2015-03-27 11:21:45
categories: sql databases
---

#**Wax On. Wax Off"**

![KarateKid][KarateKid]

I spent most of this week reading through SQL resources and doing exercism exercises. Here are my SQL notes for the week:

**Set Operators: **
soundUnion, Intersect, Except
*With from, you can add variables to make future clauses more readable
-For Example:
-select Student.sID, sName, GPA, Apply.cName, enrollment
*from Student S, College C, Apply A
*where A.sID = S.sID and A.cName = C.cName
*Operator <>	→ “not equal” (i.e. S1.sID <> S2.sID;)
*Union operator by default in SQL eliminates duplicates
-Use ‘all’ to retain duplicate with union, i.e. (union all)
*Sub-queries are nested select statements, can be nested in the where clause
*Some databases don’t support ‘all’ or ‘any’ expressions.  Use exists or not exists instead

**SQL Aggregation Clauses:**
*Initially appear in the select clause, perform computations over multiple rows in a collection
*Commonly supported aggregation functions: min, max, sum, avg, and count
*‘Group By’ lets you create custom groups from an aggregate 
*‘Having’ clause allows you to test filters for an aggregate set of values
*Equality operator is only one ‘=’ for SQL Lite 
*Any query that can be written with a ‘group by’ and ‘having’ clause can be written in another form, even if it’s strange 

**Null Values:**
*Any value or attribute can take on Null, usually used for unknown or empty values
*Wont return all dada with all inclusive equality operations if you have null values
*Can get all data results if you include ‘is null’ in query
*Will return items with null values if equality operator tests non-null attribute as well (i.e. using ‘or’ equality operators) 
*Null items not included when counting distinct values
*Null included when selecting distinct values 

**Join:**
*Joins used in ‘from’ statement to take the cross product of two tables. Doesn’t add expressiveness to the SQL language
*Inner Join: explicitly combine relations with a given condition takes the cross product of a table but only keeps the results that meet a condition 
*Natural Join: implicitly equates columns across tables with the same name and eliminates duplicate columns
*Inner Join Using(attrs): Like the natural join except you explicitly list the attributes you want equated
*Left | Right | Full Outer Join: Similar to Inner Join but populates the table with null values where data doesn’t exist
*Most SQL systems don’t allow a ‘using’ and an ‘on’ clause with a join
*Left outer join takes any couples on left side of join and if they don’t have a matching couple on the right it’s padded with a null value.
*Right outer join works like left outer join but goes the other way
*Full outer join includes unmatched applied couples from both sides of the join
*Can use left and right outer join to the same effect as full outer join


**Data Modification Statements:**
*Two methods for inserting data
-Insert using specified values
-Run query over database with select statement and insert returned values
*Deleting: Delete data where condition is met
*Update→  Set Attr = Expression where Condition
-	Can update multiple attributes in a tuple by including multiple sets
*Helpful to perform searches first to verify correct database selection before updating and/or deleting


[KrateKid]: http://jargonfiles.files.wordpress.com/2013/02/waxonwaxoff.jpg

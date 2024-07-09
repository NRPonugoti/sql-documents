# sql-documents


# group By :
group by is used to arrange identical data into group  , we can use group by in aggregate functions 
what ever you declare columns in select statement , we should mention in group by as well 

select id , sum(sal) from employee
where id=123
group by  id 

Use GROUP BY when you want to aggregate data by one or more columns. This is useful when you need summary information such as totals, averages, counts, etc., for each group.

# Order by:   
order by is used to sort the result set of query by one or more columns By default, the sorting is in ascending order, but you can also specify descending order

Use ORDER BY when you want to sort the result set based on one or more columns. This is useful when you need to present data in a specific order.

SELECT column_name(s)
FROM table_name
WHERE condition
ORDER BY column_name(s) [ASC|DESC];
Important Notes
The ORDER BY clause comes at the end of the SELECT statement.
You can use multiple columns in the ORDER BY clause. The sorting will be applied in the order the columns are listed.
The ORDER BY clause can be used in combination with other clauses like WHERE, GROUP BY, and HAVING.

# Using GROUP BY and ORDER BY Together
SELECT department, SUM(salary) AS total_salary
FROM employees
GROUP BY department
ORDER BY total_salary DESC;

## Set Operators
union :

Union all :

# Expect or Minus
Expect Operator returns rows from the result set of the first SELECT statement that are not present in the result set of second SELECT statement 
table1 lo rows , not present in table 2 , yemi rows table 1 undi table 2 lo lokunda untayi a rows dispaly chestayi 

Result =Query1 - Query2
it eliminate duplicate rows 

# Intersect
Intersect Operator returns common rows b/w the result sets of two or more select statement 

SELECT columns_name(s) FROM table1
Intersect
SELECT columns_name(s) FROM table2



=========================================================================================
# SQL Operators 
All:
ALL Operator:

The ALL operator returns TRUE if all of the subquery values meet the condition. It can be used with comparison operators like =, >, <, >=, <=, etc.
SELECT column_name(s)
FROM table_name
WHERE column_name operator ALL (SELECT column_name FROM table_name WHERE condition);

Any:
ANY Operator:

The ANY operator returns TRUE if any of the subquery values meets the condition. It can also be used with comparison operators like =, >, <, >=, <=, etc.

Key Differences:

    ALL vs ANY:
        ALL requires all values from the subquery to satisfy the condition.
        ANY requires at least one value from the subquery to satisfy the condition.

    Subquery Comparison:
        ALL and ANY are typically used in subqueries to compare values from the main query against a set of values returned by the subquery.

    Behavior with NULLs:
        ALL and ANY operators handle NULL values differently:
            ALL does not return TRUE if any comparison is NULL.
            ANY returns TRUE if at least one comparison is TRUE, even if others are NULL.

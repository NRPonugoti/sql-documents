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


union :

Union all :

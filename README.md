# SQL_JOIN_EXERCISE

Count the number of cars for each owner and display the average price for each of the cars as integers. Display the owners first_name, last_name, average price and count of vehicles. The first_name should be ordered in descending order.
Only display results with more than one vehicle and an average price greater than 10000. Your output should look like this:

 SELECT
  first_name, last_name,
  ROUND(AVG(price)) as average_price,
  COUNT(owner_id)
 FROM owners o
JOIN vehicles v on o.id=v.owner_id
 GROUP BY
 (first_name, last_name)
 HAVING
COUNT(owner_id) > 1 AND ROUND(AVG(price)) > 10000
 ORDER BY first_name DESC;


Count the number of cars for each owner. Display the owners first_name, 
last_name and count of vehicles. The first_name should be ordered in ascending order. 

SELECT first_name,last_name, COUINT(OWNER_id) FROM 
owners o JOIN vehicles v on o.id=v.owner_id
GROUP BY (first_name, last_name);

# SQL_JOIN_EXERCISE

Count the number of cars for each owner and display the average price for each of the cars as integers. Display the owners first_name, last_name, average price and count of vehicles. The first_name should be ordered in descending order.
Only display results with more than one vehicle and an average price greater than 10000. Your output should look like this:

joins_exercise=# SELECT
joins_exercise-#   first_name, last_name,
joins_exercise-#   ROUND(AVG(price)) as average_price,
joins_exercise-#   COUNT(owner_id)
joins_exercise-# FROM owners o
joins_exercise-# JOIN vehicles v on o.id=v.owner_id
joins_exercise-# GROUP BY
joins_exercise-#   (first_name, last_name)
joins_exercise-# HAVING
joins_exercise-#   COUNT(owner_id) > 1 AND ROUND(AVG(price)) > 10000
joins_exercise-# ORDER BY first_name DESC;


Count the number of cars for each owner. Display the owners first_name, 
last_name and count of vehicles. The first_name should be ordered in ascending order. 

SELECT first_name,last_name, COUINT(OWNER_id) FROM 
owners o JOIN vehicles v on o.id=v.owner_id
GROUP BY (first_name, last_name);

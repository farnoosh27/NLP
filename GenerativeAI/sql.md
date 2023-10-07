## SQL Query to Retrieve Films with Rental Rate Greater Than $2.98

This SQL query is used to retrieve information about films from a database where the rental rate is greater than $2.98. It selects the `film_id`, `title`, and `rental_rate` columns from the `film` table and limits the result to the first 10 rows.

```sql
SELECT film_id,
       title,
       rental_rate
FROM film
WHERE rental_rate > 2.98
LIMIT 10;

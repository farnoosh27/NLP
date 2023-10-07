## SQL Query to Retrieve Films with Rental Rate Greater Than $2.98
```
import numpy as np
```
This SQL query is used to retrieve information about films from a database where the rental rate is greater than $2.98. It selects the `film_id`, `title`, and `rental_rate` columns from the `film` table and limits the result to the first 10 rows.

```sql
SELECT film_id,
       title,
       rental_rate
FROM film
WHERE rental_rate > 2.98
LIMIT 10;

film_id	title	rental_rate
133	Chamber Italian	$4.99
384	Grosse Wonderful	$4.99
8	Airport Pollock	$4.99
98	Bright Encounters	$4.99
2	Ace Goldfinger	$4.99
3	Adaptation Holes	$2.99
4	Affair Prejudice	$2.99
5	African Egg	$2.99
6	Agent Truman	$2.99
7	Airplane Sierra	$4.99

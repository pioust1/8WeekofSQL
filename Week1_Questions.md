### Exercise Question: How does the output differ when you remove the alias component from the above query?  
**SELECT
  COUNT(*) AS row_count
FROM dvd_rentals.film_list;**  
#### Show Unique Column Values  
We can use the DISTINCT keyword to obtain unique values from a deduplicated target column.  
What are the unique values for the rating column in the film table?  
 **SELECT
  distinct rating
FROM dvd_rentals.film;**  
Find the count of the distinct values in the film table?  

SELECT
  count(distinct rating) as rating_count
FROM dvd_rentals.film;  

SELECT
  count(distinct rating) as rating_count
FROM dvd_rentals.film;  

**What is the frequency of values in the rating column in the film_list table?**  
SELECT rating,
  count( rating) rating_count
FROM dvd_rentals.film
group by rating;  
**SELECT
  rating,
  COUNT(*) AS frequency,
  COUNT(*)::NUMERIC / SUM(COUNT(*)) OVER () AS percentage
FROM dvd_rentals.film_list
GROUP BY rating
ORDER BY frequency DESC;**  

### EXERCISES:  

Which actor_id has the most number of unique film_id records in the dvd_rentals.film_actor table?  

Select 
actor_id,
count(distinct film_id) uniq_film_id
from 
dvd_rentals.film_actor
group by actor_id
order by count(distinct film_id)  desc limit 1;   

How many distinct fid values are there for the 3rd most common price value in the dvd_rentals.nicer_but_slower_film_list table?  

SELECT
  price,
  COUNT(DISTINCT fid)
FROM dvd_rentals.nicer_but_slower_film_list
GROUP BY 1
ORDER BY 2 DESC;  

How many unique country_id values exist in the dvd_rentals.city table?  

Select  country_id,count(distinct country_id) from 
dvd_rentals.city group by country_id  












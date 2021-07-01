#### Data with Danny  
  
  
---dvd_rentals.rental    
**Which customer_id had the latest rental_date for inventory_id = 1 and 2?**     
Select customer_id,inventory_id,rental_date from dvd_rentals.rental    
where inventory_id in (1,2) order by inventory_id,rental_date desc    
limit 10;  
  
**In the dvd_rentals.sales_by_film_category table, which category has the highest total_sales?**    
Select category,total_sales from  
dvd_rentals.sales_by_film_category order by total_sales desc limit 10;  
  
---dvd_rentals.rental  
---Which customer_id had the latest rental_date for inventory_id = 1 and 2?  
Select customer_id,inventory_id,rental_date from dvd_rentals.rental  
where inventory_id in (1,2) order by inventory_id,rental_date desc  
limit 10;  
  
---In the dvd_rentals.sales_by_film_category table, which category has the highest total_sales?  
Select category,total_sales from  
dvd_rentals.sales_by_film_category order by total_sales desc limit 10;  
  
---What is the name of the category with the highest category_id in the dvd_rentals.category table?  
Select category,category_id,name from dvd_rentals.category order by category_id desc limit 10;  
  
--For the films with the longest length, what is the title of the “R” rated film with the lowest replacement_cost in dvd_rentals.film table?  
Select title,rating,length,replacement_cost,* from dvd_rentals.film where rating='R' order by length desc,replacement_cost limit 10;  
  
---Who was the manager of the store with the highest total_sales in the dvd_rentals.sales_by_store table?  
Select manager,total_sales from   
dvd_rentals.sales_by_store order by total_sales limit 10;  
  
---Who was the manager of the store with the highest total_sales in the dvd_rentals.sales_by_store table?  
Select manager,total_sales from   
dvd_rentals.sales_by_store order by total_sales limit 10;  
---What is the postal_code of the city with the 5th highest city_id in the dvd_rentals.address table  
Select postal_code,* from dvd_rentals.address  
order by city_id desc  
limit 10;   

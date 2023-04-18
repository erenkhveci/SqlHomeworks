# SqlHomeworks

### ilk Denemeler
#### İlk ödev
select title,description from film; 
select * from film where length>60 and length<75;


select * from film where (rental_rate = 0.99 )and (replacement_cost = 12.99 or replacement_cost = 28.99)

4.Smith

select * from film where not length >50 and (not (rental_rate=2.99 or rental_rate = 4.99));
#### İkinci ödev
select * from film where replacement_cost Between 12.99 and 16.99;

select first_name,last_name from actor where first_name IN('Penelope','Nick','Ed');

select * from film where rental_rate IN( 0.99, 2.99, 4.99 ) and replacement_cost IN(12.99, 15.99, 28.99);

select * from country where  country  Like 'A%a';
#### Üçüncü ödev
select * from country  where  country Like '%_____n';

select title from film where title ILIKE '%t%t%t%t%';

select * from film where title ILIKE 'c%' and length >90 and rental_rate IN(2.99)  ;

#### Üçüncü ödev

select distinct replacement_cost from film

select count(distinct replacement_cost) from film

select count(*) from film  where title Like 'T%' and rating = 'G';

select count(*) from country where country like '_____';

select count(*) from city where city ilike '%R';
#### Dördüncü ödev
select * from film where title LIKE '%n' limit 5;

select * from film where title LIKE '%n' Offset 5 limit 5;

select * from customer where store_id=1  Order by last_name DESC;
#### Beşinci ödev
select round(avg(rental_rate),4) from film;

select count(*) from film where title Like('C%');

select Max(length) from film where rental_rate IN(0.99);

select count(distinct(replacement_cost)) from film where length>150;


#### Yedinci Ödev

select rating from film group by rating;

select replacement_cost,count(*) from film group by replacement_cost
having count(*)>50;

select store_id, count(*) from customer group by store_id;

select country_id, Count(city) from city group by country_id
Order By count DESC
Limit 1;


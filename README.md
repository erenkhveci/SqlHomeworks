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

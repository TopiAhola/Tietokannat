## 07 Koostetietokysely harjoitukset

--Kysymys 1
select max(elevation_ft)
from airport;

--Kysymys 2
select continent, count(*)
from country
group by continent;

--Kysymys 3
select screen_name, count(*)
from goal_reached
inner join game on game.id = game_id
group by screen_name;

--Kysymys 4
select screen_name
from game
where co2_consumed in
      (select min(co2_consumed) from game);

--Kysymys 5
select country.name, count(*)
from airport
inner join country on country.iso_country = airport.iso_country
group by country.name
order by count(*) desc, country.name asc
limit 50;

--Kysymys 6
select country.name
from airport
inner join country on country.iso_country = airport.iso_country
group by country.iso_country
having count(*) > 1000;

--Kysymys 7
select airport.name
from airport
where elevation_ft in( select max(elevation_ft) from airport) ;

--Kysymys 8
select country.name
from country
inner join airport on airport.iso_country = country.iso_country
where elevation_ft in( select max(elevation_ft) from airport) ;

--Kysymys 9
select count(*)
from goal_reached
inner join game on game.id = game_id
where screen_name ="Vesa";

--Kysymys 10
select airport.name
from airport
where latitude_deg in (select min(airport.latitude_deg) from airport);

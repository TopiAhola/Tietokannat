## 07 Koostetietokysely harjoitukset

--Kysymys 1      </br>
select max(elevation_ft)
from airport;      </br>
![7 1](https://github.com/user-attachments/assets/eee59789-cb9d-4360-8f71-f5aa677dd9ab)

--Kysymys 2      </br>
select continent, count(*)
from country
group by continent;      </br>
![7 2](https://github.com/user-attachments/assets/5253d174-ba08-4b56-b127-dc206dc4cbd9)

--Kysymys 3      </br>
select screen_name, count(*)
from goal_reached
inner join game on game.id = game_id
group by screen_name;      </br>
![7 3](https://github.com/user-attachments/assets/818aa1c4-edc3-44d2-ba3a-17374cf37c32)

--Kysymys 4      </br>
select screen_name
from game
where co2_consumed in
      (select min(co2_consumed) from game);      </br>
![7 4](https://github.com/user-attachments/assets/e81f856e-23fa-4405-8fd4-b2684c9d39e8)

--Kysymys 5      </br>
select country.name, count(*)
from airport
inner join country on country.iso_country = airport.iso_country
group by country.name
order by count(*) desc, country.name asc
limit 50;      </br>
![7 5](https://github.com/user-attachments/assets/63d0c5c7-a9fc-4785-a02c-7ca8bc275eca)

--Kysymys 6      </br>
select country.name
from airport
inner join country on country.iso_country = airport.iso_country
group by country.iso_country
having count(*) > 1000;      </br>
![7 6](https://github.com/user-attachments/assets/98506184-4c91-42b2-bd36-31783db805a4)

--Kysymys 7      </br>
select airport.name
from airport
where elevation_ft in( select max(elevation_ft) from airport) ;      </br>
![7 7](https://github.com/user-attachments/assets/e6e5a208-5049-457a-9c5e-f8243a14a90b)

--Kysymys 8      </br>
select country.name
from country
inner join airport on airport.iso_country = country.iso_country
where elevation_ft in( select max(elevation_ft) from airport) ;      </br>
![7 8](https://github.com/user-attachments/assets/e87404c3-bcb3-4d98-9bb8-2d7f19ca1763)

--Kysymys 9      </br>
select count(*)
from goal_reached
inner join game on game.id = game_id
where screen_name ="Vesa";      </br>
![7 9](https://github.com/user-attachments/assets/cafd0f9e-8327-4c46-84bf-2f326d281a3e)

--Kysymys 10      </br>
select airport.name
from airport
where latitude_deg in (select min(airport.latitude_deg) from airport);      </br>
![7 10](https://github.com/user-attachments/assets/40e881b5-c1d8-4656-8cc4-01fd053faeed)

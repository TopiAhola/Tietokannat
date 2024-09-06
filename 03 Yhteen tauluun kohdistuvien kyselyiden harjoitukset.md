## 03 Yhteen tauluun kohdistuvien kyselyiden harjoitukset.

--Kysymys 1
select * from goal;
![ruudunkaappaus](kuvatiedoston-nimi.png)

--Kysymys 2 </br>
select name, type 
from airport
where iso_country = "fi";
![3 2](https://github.com/user-attachments/assets/59890710-ca3b-4fa6-9d3a-04e087c58b3e)

--Kysymys 3
select airport.name
from airport
where iso_country = "FI"
order by airport.name;


--Kysymys 4
select airport.name, airport.type
from airport
where iso_country = "FI"
order by airport.type, airport.name;

--Kysymys 5
select name
from country
where name like "F%";

--Kysymys 6
select name
from country
where name like "%f%";

--Kysymys 7
select location
from game
where location = "EGCC";

--Kysymys 8
select co2_consumed
from game
where screen_name = "Ilkka";

--Kysymys 9
select co2_budget
from game
group by co2_budget;





















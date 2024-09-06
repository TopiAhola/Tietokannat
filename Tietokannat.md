#Tietokanta

## Tentti 2 Yhteen tauluun kohdistuvien kyselyiden harjoitukset.

--tehtävä 1
select * from goal;
![ruudunkaappaus](kuvatiedoston-nimi.png)

--tehtävä 2
select name, type 
from airport
where iso_country = "fi";

--tehtävä 3
select airport.name
from airport
where iso_country = "FI"
order by airport.name;

--tehtävä 4
select airport.name, airport.type
from airport
where iso_country = "FI"
order by airport.type, airport.name;

---tehtävä 5
select name
from country
where name like "F%";

---tehtävä 6
select name
from country
where name like "%f%";

---tehtävä 7
select location
from game
where location = "EGCC";

---tehtävä 8
select co2_consumed
from game
where screen_name = "Ilkka";

---tehtävä 9
select co2_budget
from game
group by co2_budget;

## Tentti 3 





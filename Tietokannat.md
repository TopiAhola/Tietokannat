# Tietokanta tehtävien palautus

## 03 Yhteen tauluun kohdistuvien kyselyiden harjoitukset.

--Kysymys 1
select * from goal;
![ruudunkaappaus](kuvatiedoston-nimi.png)

--Kysymys 2
select name, type 
from airport
where iso_country = "fi";

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



## 04 Where-osan liitosehto harjoitukset

--Kysymys 1
select country.name as "country name", airport.name as "airport name"
from airport, country
where airport.iso_country = country.iso_country
and country.name = "Iceland";


--Kysymys 2
select airport.name as "airport name"
from airport, country
where airport.type like "large%"
and airport.iso_country = country.iso_country
and country.name = "France";

--Kysymys 3
select country.name as "country_name", airport.name as "airport_name"
from country, airport
where airport.continent = "AN"
and airport.iso_country = country.iso_country;


--Kysymys 4
select elevation_ft as elevation_m
from airport, game
where airport.ident = game.location
and game.screen_name = "Heini"

--Kysymys 5
select elevation_ft*0.3048 as elevation_m
from airport, game
where airport.ident = game.location
and game.screen_name = "Heini"

---Kysymys 6
select airport.name
from airport, game
where game.location = airport.ident
and game.screen_name = "Ilkka"

--Kysymys 7
select country.name
from airport, game, country
where country.iso_country = airport.iso_country
and game.location = airport.ident
and game.screen_name = "Ilkka"

--Kysymys 8
select goal.name
from goal, goal_reached, game
where goal_id = goal.id
and game_id = game.id
and screen_name = "Heini"

--Kysymys 9
select airport.name
from airport, game, goal_reached, goal
where goal.name = "CLOUDS"
and goal.id = goal_reached.goal_id
and goal_reached.game_id = game.id
and game.screen_name = "Ilkka"
and game.location = airport.ident


--Kysymys 10
select country.name
from country, airport, game, goal_reached, goal
where goal.name = "CLOUDS"
and goal.id = goal_reached.goal_id
and goal_reached.game_id = game.id
and game.screen_name = "Ilkka"
and game.location = airport.ident
and airport.iso_country = country.iso_country

















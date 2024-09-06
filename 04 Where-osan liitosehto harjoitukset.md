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

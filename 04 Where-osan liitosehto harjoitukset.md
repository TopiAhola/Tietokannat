## 04 Where-osan liitosehto harjoitukset

--Kysymys 1 </br>
select country.name as "country name", airport.name as "airport name"
from airport, country
where airport.iso_country = country.iso_country
and country.name = "Iceland";  </br>
![4 1](https://github.com/user-attachments/assets/07e9db70-08b7-4c74-a26c-22b328200afc)


--Kysymys 2  </br>
select airport.name as "airport name"
from airport, country
where airport.type like "large%"
and airport.iso_country = country.iso_country
and country.name = "France";  </br>
![4 2](https://github.com/user-attachments/assets/7b53302d-c376-46b3-84c3-d2114831db1a)


--Kysymys 3  </br>
select country.name as "country_name", airport.name as "airport_name"
from country, airport
where airport.continent = "AN"
and airport.iso_country = country.iso_country;  </br>
![4 3](https://github.com/user-attachments/assets/9a5fd03c-2b4b-4384-9ca1-2a80627b23bf)


--Kysymys 4  </br>
select elevation_ft 
from airport, game
where airport.ident = game.location
and game.screen_name = "Heini";  </br>
![4 4](https://github.com/user-attachments/assets/36042be6-fde0-4511-8b38-7dac9e7cf83f)


--Kysymys 5  </br>
select elevation_ft*0.3048 as elevation_m
from airport, game
where airport.ident = game.location
and game.screen_name = "Heini";  </br>
![4 5](https://github.com/user-attachments/assets/34749ee2-f568-4a88-9014-980fbb34119e)


--Kysymys 6  </br>
select airport.name
from airport, game
where game.location = airport.ident
and game.screen_name = "Ilkka";  </br>
![4 6](https://github.com/user-attachments/assets/dd694d5d-5502-4d5c-876b-cb6ae8c5d5cb)


--Kysymys 7  </br>
select country.name
from airport, game, country
where country.iso_country = airport.iso_country
and game.location = airport.ident
and game.screen_name = "Ilkka";  </br>
![4 7](https://github.com/user-attachments/assets/c44e6e7a-ca70-4ca9-a55b-a660d5ec4dda)


--Kysymys 8  </br>
select goal.name
from goal, goal_reached, game
where goal_id = goal.id
and game_id = game.id
and screen_name = "Heini";  </br>
![4 8](https://github.com/user-attachments/assets/79d159c9-6ade-4e44-9204-ad35f017089f)


--Kysymys 9  </br>
select airport.name
from airport, game, goal_reached, goal
where goal.name = "CLOUDS"
and goal.id = goal_reached.goal_id
and goal_reached.game_id = game.id
and game.screen_name = "Ilkka"
and game.location = airport.ident;  </br>
![4 9](https://github.com/user-attachments/assets/7bdb4f5b-8546-43b4-8699-971acd4d6d96)


--Kysymys 10  </br>
select country.name
from country, airport, game, goal_reached, goal
where goal.name = "CLOUDS"
and goal.id = goal_reached.goal_id
and goal_reached.game_id = game.id
and game.screen_name = "Ilkka"
and game.location = airport.ident
and airport.iso_country = country.iso_country;  </br>
![4 10](https://github.com/user-attachments/assets/78b2f4d9-2d36-44b3-9fe2-431fff308d52)

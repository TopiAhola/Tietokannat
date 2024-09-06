## 05 Join harjoitukset

--Kysymys 1  </br>
select country.name as "country name", airport.name as "airport name"
from country
inner join airport on airport.iso_country = country.iso_country
where country.name = "Finland"
and scheduled_service = "yes";  </br>
![5 1](https://github.com/user-attachments/assets/ae973efe-30ac-4aeb-bb6b-615ea322b133)


--Kysymys 2  </br>
select screen_name, airport.name
from game
inner join airport on location = ident;  </br>
![5 2](https://github.com/user-attachments/assets/9a07df46-048e-4d54-a0d6-0f5584c51b45)


--Kysymys 3  </br>
select screen_name, country.name
from game
inner join airport on location = ident
inner join country on airport.iso_country = country.iso_country;  </br>
![5 3](https://github.com/user-attachments/assets/58906813-6e27-4496-8017-988a83237f26)

--Kysymys 4  </br>
select name, screen_name
from airport
left join game on location = ident
where airport.name like "%hels%";  </br>
![5 4](https://github.com/user-attachments/assets/6b7a884c-63f5-4364-9410-d7fe5a81a309)

--Kysymys 5  </br>
select name, screen_name
from goal
left join goal_reached on goal.id = goal_id
left join game on game_id = game.id;  </br>
![5 5](https://github.com/user-attachments/assets/c4eea206-6798-463d-844b-6a29bd68a45e)

--Kysymys 1
select country.name as "country name", airport.name as "airport name"
from country
inner join airport on airport.iso_country = country.iso_country
where country.name = "Finland"
and scheduled_service = "yes";

--Kysymys 2
select screen_name, airport.name
from game
inner join airport on location = ident;

--Kysymys 3
select screen_name, country.name
from game
inner join airport on location = ident
inner join country on airport.iso_country = country.iso_country;

--Kysymys 4
select name, screen_name
from airport
left join game on location = ident
where airport.name like "%hels%";

--Kysymys 5
select name, screen_name
from goal
left join goal_reached on goal.id = goal_id
left join game on game_id = game.id;

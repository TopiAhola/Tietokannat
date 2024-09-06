## 06 Sisäkysely harjoitukset

--Kysymys 1
select name
from country
where iso_country in
(select iso_country from airport where name like "Satsuma%");

--Kysymys 2
select name
from airport
where iso_country in
(select iso_country from country where name = "Monaco");

--Kysymys 3
select screen_name
from game
where id in
    (select game_id from goal_reached where goal_id in
        (select id from goal where name = "CLOUDS") );

--Kysymys 4
select name
from country
where iso_country not in (select iso_country from airport);

--Kysymys 5
select goal.name
from goal
where id not in
      (select goal_id from goal_reached where game_id in
        (select id from game where screen_name ="Heini"));


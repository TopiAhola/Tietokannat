## 06 Sisäkysely harjoitukset

--Kysymys 1    </br>
select name
from country
where iso_country in
(select iso_country from airport where name like "Satsuma%");    </br>
![6 1](https://github.com/user-attachments/assets/b0ff8250-98f9-4611-8ed9-016a3cbe89e4)

--Kysymys 2    </br>
select name
from airport
where iso_country in
(select iso_country from country where name = "Monaco");    </br>
![6 2](https://github.com/user-attachments/assets/58c65cd1-e4fc-4015-934a-eff5a8c99f2d)

--Kysymys 3    </br>
select screen_name
from game
where id in
    (select game_id from goal_reached where goal_id in
        (select id from goal where name = "CLOUDS") );    </br>
![6 3](https://github.com/user-attachments/assets/298613a4-db68-420a-8fbf-60def7ebdc3a)

--Kysymys 4    </br>
select name
from country
where iso_country not in (select iso_country from airport);    </br>
![6 4](https://github.com/user-attachments/assets/0db6ebd6-abd8-4ae5-8b55-064b0a8ecfa5)

--Kysymys 5    </br>
select goal.name
from goal
where id not in
      (select goal_id from goal_reached where game_id in
        (select id from game where screen_name ="Heini"));    </br>
![6 5](https://github.com/user-attachments/assets/9a786bcb-c4df-473d-963e-9ce2b0385dc1)


## 08 Päivityskyselyt harjoitukset

--Kysymys 1
update game 
set
co2_consumed = co2_consumed + 500,
location = (select ident from airport where airport.name = "Nottingham airport")
where screen_name ="Vesa";

--Kysymys 3
delete from goal_reached;


--Kysymys 4
delete from game;

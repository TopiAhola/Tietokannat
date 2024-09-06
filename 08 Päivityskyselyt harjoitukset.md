## 08 Päivityskyselyt harjoitukset

--Kysymys 1  </br>
update game 
set
co2_consumed = co2_consumed + 500,
location = (select ident from airport where airport.name = "Nottingham airport")
where screen_name ="Vesa";  </br>
![8 1](https://github.com/user-attachments/assets/59a28eeb-1e36-4a67-8652-57730519b7af)

--Kysymys 3  </br>
delete from goal_reached;  </br>
![8 3](https://github.com/user-attachments/assets/b4741f00-b555-41d6-81df-104a118aea03)


--Kysymys 4  </br>
delete from game;  </br>
![8 4](https://github.com/user-attachments/assets/51050a96-fe85-4c09-91a3-e4ab6f1d6604)

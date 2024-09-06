## 03 Yhteen tauluun kohdistuvien kyselyiden harjoitukset.

--Kysymys 1 </br>
select * from goal;
![3 1](https://github.com/user-attachments/assets/80cc7479-115c-4b9e-b91d-8996a7175ddd)


--Kysymys 2 </br>
select name, type 
from airport
where iso_country = "fi";
![3 2](https://github.com/user-attachments/assets/59890710-ca3b-4fa6-9d3a-04e087c58b3e)

--Kysymys 3 </br>
select airport.name
from airport
where iso_country = "FI"
order by airport.name;
![3 3](https://github.com/user-attachments/assets/63325352-0e42-47f1-9970-8e1d64c5e5dc)

--Kysymys 4 </br>
select airport.name, airport.type
from airport
where iso_country = "FI"
order by airport.type, airport.name;
![3 4](https://github.com/user-attachments/assets/a5bab3ad-785c-49a2-9ca4-2a47847aa2ba)

--Kysymys 5 </br>
select name
from country
where name like "F%";
![3 5](https://github.com/user-attachments/assets/07671f24-7806-44a9-ae42-cf66c8d29c05)


--Kysymys 6 </br>
select name
from country
where name like "%f%";
![3 6](https://github.com/user-attachments/assets/0d04b728-9dea-43a8-b014-377a5b65e4bc)


--Kysymys 7 </br>
select location
from game
where location = "EGCC";
![3 7](https://github.com/user-attachments/assets/695519fc-c576-4c9f-9918-ec3d4138c568)


--Kysymys 8 </br>
select co2_consumed
from game
where screen_name = "Ilkka";
![3 8](https://github.com/user-attachments/assets/79cbc65d-ed4f-4ab2-b941-f0b828b08a1a)


--Kysymys 9 </br>
select co2_budget
from game
group by co2_budget;
![3 9](https://github.com/user-attachments/assets/5a153427-7037-44b7-a006-aa049e7008b2)  

.





















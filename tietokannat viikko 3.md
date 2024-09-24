osio = join harjoitukset

1 Tehtävä:
select country.name as "country name", airport.name as "airport name"
from country inner join airport on airport.iso_country = country.iso_country
where country.name = "Finland" and scheduled_service = "yes";
![1](https://github.com/user-attachments/assets/03dac5a0-da15-4581-a3c6-a12b6449a7a7)

2 Tehtävä:
select screen_name, airport.name
from game inner join airport on location = ident;
![2](https://github.com/user-attachments/assets/38c44a96-3326-4fe0-91e2-7897a067c371)


3 Tehtävä:
select screen_name, country.name
from game inner join airport on location = ident inner join country on airport.iso_country = country.iso_country;
![3](https://github.com/user-attachments/assets/5d08ccbd-879e-4c25-871b-d80ddcc06dcd)


4 Tehtävä:
select airport.name, screen_name
from airport left join game on ident = location where name like "%Hels%";
![4](https://github.com/user-attachments/assets/a6e71e6b-ca71-4337-9182-81bec1ace4eb)


5 Tehtävä:
select name, screen_name
from goal left join goal_reached on goal.id = goal_id  left join game on game.id = game_id;
![5](https://github.com/user-attachments/assets/4198d95c-2668-4796-affc-e3efdab65e69)




osio = sisäkysely harjoitukset

1 Tehtävä:
select name from country where 
iso_country in( select iso_country from airport where name like "Satsuma%");
![1](https://github.com/user-attachments/assets/ef15eb20-978a-4a69-a427-cc91f06d955f)

2 Tehtävä:
select name from airport where iso_country in( select iso_country from country where name = "Monaco");
![2](https://github.com/user-attachments/assets/eb51e68f-d79d-4cd6-a2ba-fa0a1bb33c6e)

3 Tehtävä:
select screen_name from game where id in ( select game_id from goal_reached where goal_id in( select id from goal where name = "CLOUDS"));
![3](https://github.com/user-attachments/assets/5863df4e-2b16-4900-99eb-87083d3679d2)


4 Tehtävä:
select country.name from country where iso_country not in (select airport.iso_country from airport);
![4](https://github.com/user-attachments/assets/ca29ee07-2356-4d16-967f-b7b7247e6a98)

5 Tehtävä:
select name from goal where id not in( select goal.id from goal, goal_reached, game where game.id = game_id and goal.id = goal_id and screen_name = "Heini");
![5](https://github.com/user-attachments/assets/e2dcab64-70dc-4239-ad3c-241b4733e3b3)


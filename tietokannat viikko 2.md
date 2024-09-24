Osio = yhteen tauluun kohdistuvien kyselyiden harjoitukset

1 tehtävä: 
select * from goal;
![tietokanta viikko 2 teht 1](https://github.com/user-attachments/assets/d54fcda5-c7fe-4043-8684-9ed556d22802)


2 tehtävä:
select name airport_type from airport where iso_country = "FI";
![tietokanta viikko 2 teht 2](https://github.com/user-attachments/assets/fced81a6-29cc-48b0-b084-2c1d6ded979f)


3 tehtävä:
select name from airport where iso_country = "FI" order by name;
![tietokanta viikko 2 teht 3](https://github.com/user-attachments/assets/309bed18-41cf-4a7e-a93a-87f33793a7d9)


4 tehtävä:
select name, type from airport where iso_country = "FI" order by type, name;
![tietokanta viikko 2teht 4](https://github.com/user-attachments/assets/f8623d5d-a318-42ce-bdf9-02c08bfdc781)


5 tehtävä:
select name from country where name like "F%";
![tietokanta viikko 2 tehtävä 5](https://github.com/user-attachments/assets/49a7f3da-d57b-40c4-be3b-b88eaec0e7ee)


6 tehtävä:
select name from country where name like "%F%";
![tietokanta viikko 2 tehtävä 6](https://github.com/user-attachments/assets/50fddbcf-ed0d-419f-bc37-4a364b910425)

7 tehtävä:
select location from game where screen_name = "Vesa";
![tietokanta viikko 2 teht 7](https://github.com/user-attachments/assets/2b364f1f-d283-4ab7-aa49-353bcd831082)


8 tehtävä:
select co2_consumed from game where screen_name = "Ilkka";
![tietokanta viikko 2 teht 8](https://github.com/user-attachments/assets/e293b53e-6b2b-4242-80aa-87a5a2efecb4)


9 tehtävä:
select distinct co2_budget from game;
![tietokanta viikko 2 teht 9](https://github.com/user-attachments/assets/89fa01c7-f796-4acc-9637-a3ce0f660297)


Osio = Where osan liitosehto harjoitukset

1 tehtävä:
SELECT country.name AS "country name", airport.name AS "airport name" FROM airport JOIN country ON airport.iso_country = country.iso_country WHERE country.name = 'Iceland';
![1](https://github.com/user-attachments/assets/dce4cc9f-8b2a-418f-a93c-cc3cb1be6df1)


2 tehtävä:
SELECT airport.name AS "airport name" FROM airport JOIN country ON airport.iso_country = country.iso_country WHERE country.name = 'France' AND airport.type = 'large_airport';

![2](https://github.com/user-attachments/assets/8c0915f7-1f22-4dae-a225-cd5f8db569fb)

3 tehtävä:
SELECT country.name AS country_name, airport.name AS airport_name FROM airport JOIN country ON airport.iso_country = country.iso_country WHERE airport.continent = 'AN';

![3](https://github.com/user-attachments/assets/601230da-c925-43cc-b3e3-c81c2949f178)

4 tehtävä:
SELECT airport.elevation_ft FROM game JOIN airport ON game.location = airport.ident WHERE game.screen_name = 'Heini';
![4](https://github.com/user-attachments/assets/adffb969-145f-44b1-b20c-2d42f9518625)

5 tehtävä:
SELECT airport.elevation_ft * 0.3048 AS elevation_m FROM game JOIN airport ON game.location = airport.ident WHERE game.screen_name = 'Heini';
![5](https://github.com/user-attachments/assets/123a9b89-b807-46ce-afc0-6b1430540f9d)

6 tehtävä:
SELECT airport.name FROM game JOIN airport ON game.location = airport.ident WHERE game.screen_name = 'Ilkka';
![6](https://github.com/user-attachments/assets/e4bff242-eb87-46f9-9ef0-4b1512cf3256)

7 tehtävä:
SELECT country.name FROM game JOIN airport ON game.location = airport.ident JOIN country ON airport.iso_country = country.iso_country WHERE game.screen_name = 'Ilkka';
![7](https://github.com/user-attachments/assets/5ce9bc88-0d19-456f-a340-b63d1f2acdae)

8 tehtävä:
select name from goal, goal_reached, game where game.id = game_id and goal.id = goal_id and screen_name = "Heini";
![8](https://github.com/user-attachments/assets/2b3359ce-997b-447b-9dcf-8ebe77fecc1d)

9 tehtävä:
select airport.name from airport, game, goal, goal_reached where ident = location and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS";
![9](https://github.com/user-attachments/assets/f41b0dc7-e894-4704-928a-43d88fc7d898)

10 tehtävä:
select country.name from country, airport, game, goal, goal_reached where airport.iso_country = country.iso_country and ident = location and game.id = game_id and goal.id = goal_id and screen_name = "Ilkka" and goal.name = "CLOUDS";

![10](https://github.com/user-attachments/assets/d1494a7e-2d84-430c-9917-a9597fc73c3a)

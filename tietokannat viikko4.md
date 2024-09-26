osio = koostetieto kyselyt

tehtävä 1: select max(elevation_ft) from airport;
![image](https://github.com/user-attachments/assets/8cb3341a-77d2-41b0-a524-7a0d2a5b2d93)

tehtävä 2: select continent, count(*) from country group by continent;
![image](https://github.com/user-attachments/assets/77a1895a-f510-474e-ac23-38b67485729a)

tehtävä 3: select screen_name, count(*) from game, goal_reached where id = game_id group by screen_name;
![image](https://github.com/user-attachments/assets/ec4bbb06-1e4b-44fa-a128-3677a68bd4ab)

tehtävä 4: select screen_name from game where co2_consumed in(select min(co2_consumed) from game);
![image](https://github.com/user-attachments/assets/e2747d45-4fcd-4412-8368-7c83a8338a12)

tehtävä 5:select country.name, count(*) from airport, country where airport.iso_country = country.iso_country 
group by country.iso_country order by count(*) desc limit 50;
![image](https://github.com/user-attachments/assets/96bc93ac-9759-4f33-bcd5-e6235f14b453)

tehtävä 6:select country.name from airport, country where airport.iso_country = country.iso_country 
group by country.iso_country having count(*) > 1000;
![image](https://github.com/user-attachments/assets/c9bd9102-f2bb-4fad-9ecd-5f411fd87965)

tehtävä 7: select name from airport where elevation_ft in ( select max(elevation_ft) from airport );
![image](https://github.com/user-attachments/assets/fca8e01d-55eb-4ef6-9b90-be0afe37e442)

tehtävä 8: select name from country where iso_country in (select iso_country from airport
where elevation_ft in(select max(elevation_ft)from airport));
![image](https://github.com/user-attachments/assets/bc616ce7-7c16-451a-a1c1-d7d42575a899)

tehtävä 9: select count(*) from game, goal_reached where id = game_id and screen_name = "Vesa" group by screen_name;
![image](https://github.com/user-attachments/assets/d8953c6e-3fcb-4f62-9732-e56ebbf95a73)

tehtävä 10: select name from airport where latitude_deg in( select min(latitude_deg) from airport);
![image](https://github.com/user-attachments/assets/fefa72e1-843b-4515-941b-6e13b87efa84)

osio =päivityskysely harjoitukset
tehtävä 1: update game 
            set  location = (select ident from airport where name = "Nottingham Airport"), co2_consumed = co2_consumed+500
            where screen_name = "Vesa";
![image](https://github.com/user-attachments/assets/61ca9d81-fb01-472a-8559-8621a2389e10)


tehtävä 2: ![image](https://github.com/user-attachments/assets/5d26fb5f-323b-44b7-be88-59078c51ac3f)
tehtävä 3: delete from goal_reached;
tehtävä 4: delete from game;


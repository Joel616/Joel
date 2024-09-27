Code 1:
SELECT * 
FROM crime_scene_report
LIMIT 5;

Output:
 
![image](https://github.com/user-attachments/assets/f93c9f24-7939-46d7-8d13-0fc8d7545f39)

Code 2:
SELECT *
FROM crime_scene_report
WHERE type = "mur  der";

Code 3:
SELECT *
FROM crime_scene_report
WHERE type = "murder"
AND date = 20180115
AND city = "SQL City";

Output:
 
![image](https://github.com/user-attachments/assets/249092eb-2ef9-4f72-8a2e-5896980e6fdc)

Code 4:
SELECT *
FROM person
LIMIT 5;

Output:
 ![image](https://github.com/user-attachments/assets/fa8e3eb3-293d-4055-92f7-53353a7a2dbb)


Code 5:
SELECT *
FROM person
WHERE address_street_name = "Northwestern Dr"
ORDER BY address_number DESC;

14887	Morty Schapiro	118009	4919	Northwestern Dr	111564949
Output:
![image](https://github.com/user-attachments/assets/3728423c-bd6b-40e5-aa91-983578d71258)


Code 6:
SELECT *
FROM person
WHERE name LIKE '%Annabel%'
AND address_street_name = "Franklin Ave";

Output:
 ![image](https://github.com/user-attachments/assets/6471bc70-cbfc-4d33-8b93-9da437608e94)


Code 7:
SELECT *
FROM interview
WHERE person_id IN ("14887", "16371");

Output:
 ![image](https://github.com/user-attachments/assets/04612420-3e74-42d9-8b83-2e37dfc2c4f4)



So, here's our clues:
•	Murderer is a man and a member of a gym called "Get Fit Now Gym" and has a gold membership no. starting from "48Z".
•	He was working out at the gym on 9th Jan.
•	He drives a car with car plate containing "H42W".


Code 8:
SELECT *
FROM get_fit_now_check_in
WHERE membership_id LIKE '48Z%'
AND check_in_date = "20180109";

Output:
 
![image](https://github.com/user-attachments/assets/9b4df330-0d9d-446b-882c-fa95207e795e)

Code 9:
SELECT *
FROM drivers_license
WHERE gender = "male"
AND plate_number LIKE '%H42W%';




Output:
 ![image](https://github.com/user-attachments/assets/0ca638e6-025c-4d9e-9ec3-adff00d1ac74)


Code 10:
SELECT *
FROM person
WHERE license_id IN ("423327", "664760");

Output:
 ![image](https://github.com/user-attachments/assets/9beeba36-ec14-4294-8ef8-a5c3f05f6edc)


Code 11:
SELECT *
FROM get_fit_now_member
WHERE person_id IN ("51739", "67318");

Output:
![image](https://github.com/user-attachments/assets/5a86f6b5-9c5a-4c31-993d-3a4c581f00ad)

Jeremy Bowers is the Murderer.

THE FINAL SOLUTION
 
![image](https://github.com/user-attachments/assets/18ee7acc-1436-4886-b930-ed13e56e62b3)
SELECT * FROM interview WHERE person_id = "67318";
![image](https://github.com/user-attachments/assets/85f6abd0-dc25-4713-a34a-9dafb0b51003)

SELECT * FROM drivers_license WHERE gender = "female" AND hair_color = "red" AND height BETWEEN 65 AND 67 AND car_make = "Tesla" AND car_model = "Model S";
![image](https://github.com/user-attachments/assets/5d1c65e2-3a3c-4a9a-8f05-f14044d5eba1)

SELECT * FROM person WHERE license_id IN ("202298", "291182", "918773");
![image](https://github.com/user-attachments/assets/477de5b6-2c29-4f61-afa0-2ed5cdf69321)

SELECT person_id, event_name, COUNT(*) AS event_count FROM facebook_event_checkin WHERE person_id IN ("78881", "90700", "99716") GROUP BY person_id, event_name;
![image](https://github.com/user-attachments/assets/1965e0dc-257c-4b6c-9d2b-2110270870ac)

SELECT *FROM PERSON WHERE ID="99716"; 
![image](https://github.com/user-attachments/assets/f957f4b7-5e8b-48b3-b11b-32efaa570613)
INSERT INTO solution VALUES (1, 'Miranda Priestly');
 ![image](https://github.com/user-attachments/assets/bbfd709b-df10-43f8-9870-fb21ddfbc679)
       
        

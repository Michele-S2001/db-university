# UNIVERSITY MYSQL

1) Selezionare tutti gli studenti nati nel 1990 (160): 
  ```MYSQL
  SELECT *
  FROM `students`
  WHERE YEAR(`date_of_birth`) = 1990;
  ```

2) Selezionare tutti i corsi che valgono più di 10 crediti:
  ```MYSQL
  SELECT * 
  FROM `courses`
  WHERE `cfu` > 10;
  ```

3) Selezionare tutti gli studenti che hanno più di 30 anni:
  ```MYSQL
  SELECT * 
  FROM `students`
  WHERE YEAR(CURRENT_DATE) - YEAR(`date_of_birth`) > 30;
  ```

4) Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea (286):
  ```MYSQL
  SELECT * 
  FROM `courses`
  WHERE `year` = 1 AND `period` LIKE 'I_s%';
  ```

5) Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del 20/06/2020 (21):
  ```MYSQL
  SELECT *
  FROM `exams`
  WHERE `date` = '2020/06/20' AND `hour` > '14:00:00';
  ```

6) Selezionare tutti i corsi di laurea magistrale (38):
  ```MYSQL
  SELECT * 
  FROM `degrees`
  WHERE `level` LIKE 'm%';
  ```

7) Da quanti dipartimenti è composta l'univesità ? (12):
  ```MYSQL
  SELECT COUNT(`id`) AS 'n_departments'
  FROM `departments`;
  ```

8) Quanti sono gli insegnanti che non hanno un numero di telefono (50):
  ```MYSQL
 SELECT COUNT(`id`) AS 'without_phone_number' 
  FROM `teachers`
  WHERE `phone` IS NULL;
  ```
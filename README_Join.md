# UNIVERSITY JOIN QUERIES

1) Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia
  ```MYSQL
  SELECT `students`.*, `degrees`.`name` AS 'corso_di_laurea'
  FROM `degrees`
  INNER JOIN `students` ON `degrees`.`id` = `students`.`degree_id`
  WHERE `degrees`.`name` = 'Corso di Laurea in Economia';
  ```

2) Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di
Neuroscienze
  ```MYSQL
  SELECT `departments`.*, `degrees`.`name` AS 'corso_magistrale' 
  FROM `departments`
  INNER JOIN `degrees` ON `departments`.`id` = `degrees`.`department_id`
  WHERE `departments`.`name` = 'Dipartimento di Neuroscienze' 
  AND `degrees`.`level` = 'magistrale';
  ```

3) Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)
  ```MYSQL
  SELECT `teachers`.*, `courses`.`name` AS 'nome_corso'
  FROM `teachers`
  INNER JOIN `course_teacher` ON `teachers`.`id` = `course_teacher`.`teacher_id`
  INNER JOIN `courses` ON `courses`.`id` = `course_teacher`.`course_id`
  WHERE `teachers`.`name` = 'Fulvio' AND `teachers`.`surname` = 'Amato';
  ```

4) Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui
sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e
nome
  ```MYSQL
  SELECT `students`.*, `degrees`.`name` AS 'corso_di_laurea', `departments`.`name` AS 'dipartimento' 
  FROM `students`
  INNER JOIN `degrees` ON `students`.`degree_id` = `degrees`.`id`
  INNER JOIN `departments` ON `departments`.`id` = `degrees`.`department_id`
  ORDER BY `students`.`surname`, `students`.`name` ASC;
  ```

5) Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti
  ```MYSQL
  ```

6)  Selezionare tutti i docenti che insegnano nel Dipartimento di
Matematica (54)
  ```MYSQL
  ```

7)  BONUS: Selezionare per ogni studente il numero di tentativi sostenuti
per ogni esame, stampando anche il voto massimo. Successivamente,
filtrare i tentativi con voto minimo 18.
  ```MYSQL
  ```
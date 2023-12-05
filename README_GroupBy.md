# UNIVERSITY GROUP BY

1) Contare quanti iscritti ci sono stati ogni anno
  ```MYSQL
  SELECT COUNT(*) AS 'iscritti_ogni_anno', YEAR(`enrolment_date`) AS 'year'
  FROM `students`
  GROUP BY YEAR(`enrolment_date`);
  ```

2) Contare gli insegnanti che hanno l'ufficio nello stesso edificio
  ```MYSQL
  SELECT COUNT(*) AS 'insegnanti', `office_address`
  FROM `teachers`
  GROUP BY `office_address`;
  ```

3) Calcolare la media dei voti di ogni appello d'esame
  ```MYSQL
  SELECT COUNT(*) AS 'numero_appelli', `exam_id`, AVG(`vote`) AS 'media'
  FROM `exam_student`
  GROUP BY `exam_id`;
  ```

4) Contare quanti corsi di laurea ci sono per ogni dipartimento
  ```MYSQL
  ```
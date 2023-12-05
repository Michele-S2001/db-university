# UNIVERSITY GROUP BY

1) Contare quanti iscritti ci sono stati ogni anno
  ```MYSQL
  SELECT COUNT(*) AS 'iscritti_ogni_anno', YEAR(`enrolment_date`) AS 'year'
  FROM `students`
  GROUP BY YEAR(`enrolment_date`);
  ```
## Esercizio query group

# Contare quanti iscritti ci sono stati ogni anno
SELECT COUNT(id) AS num_students, year(enrolment_date) AS year_enrolment FROM students GROUP BY year(enrolment_date);

# Contare gli insegnanti che hanno l'ufficio nello stesso edificio
SELECT COUNT(id) AS Num_teachers, office_address FROM teachers GROUP BY office_address;

# Calcolare la media dei voti di ogni appello d'esame
SELECT exam_id ,avg(vote) AS avg_vote FROM exam_student GROUP BY exam_id;

# Contare quanti corsi di laurea ci sono per ogni dipartimento
SELECT department_id, COUNT(id) AS num_degrees FROM degrees GROUP BY department_id;


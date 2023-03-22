create database my_company_database

create table employees(id int auto_increment,birth_date date,first_name varchar(100),last_name varchar(100),gender varchar(100),PRIMARY KEY(id));

alter table employees add salary int;

alter table employees add tittle varchar(100);

alter table employees add tittle_date date;

select * from employees;

INSERT INTO employees (birth_date, first_name, last_name, gender, salary, title, title_date) VALUES ('1990-01-01', 'Javier', 'Martínez', 'M', 25000, 'Gerente', '2020-01-01'),('1992-02-15', 'Sofía', 'García', 'F', 30000, 'Auxiliar', '2020-01-01'),('1995-03-30', 'Luis', 'Hernández', 'M', 35000, 'Marinero', '2020-01-01'), ('1998-04-10', 'María', 'López', 'F', 40000, 'Cirujano', '2020-01-01'),('1990-05-20', 'Francisco', 'González', 'M', 45000, 'Profesor', '2020-01-01'),('1992-06-05', 'Carmen', 'Ruiz', 'F', 5000, 'Asociada', '2021-02-01'),('1995-07-15', 'Jorge', 'Fernández', 'M', 10000, 'Psicologo', '2021-02-01'),('1998-08-20', 'Ana', 'Pérez', 'F', 15000, 'Criminologa', '2021-02-01'),('1990-09-25', 'Diego', 'Sánchez', 'M', 20000, 'Escritor', '2021-02-01'),('1992-10-30', 'Isabel', 'Gómez', 'F', 25000, 'Desarrolladora Web', '2021-02-01'),('1995-11-10', 'Alejandro', 'Muñoz', 'M', 30000, 'Soldador', '2022-03-01'),('1998-12-20', 'Sara', 'Torres', 'F', 35000, 'Traductora', '2022-03-01'),('1990-01-03', 'Miguel', 'Romero', 'M', 40000, 'Cajero', '2022-03-01'),('1992-02-08', 'Lucía', 'Jiménez', 'F', 45000, 'Abogada', '2022-03-01'),('1995-03-18', 'Pedro', 'Díaz', 'M', 5000, 'Masajista', '2020-05-01');

UPDATE employees SET first_name = 'Julian' WHERE last_name = 'Barroso' AND birth_date = '2000-01-12' AND first_name = 'Javier';

SELECT * FROM employees WHERE salary > 20000;

SELECT * FROM employees WHERE salary < 10000;

SELECT * FROM employees WHERE salary BETWEEN 14000 AND 50000;

SELECT COUNT(*) FROM employees;

SELECT title FROM employees WHERE YEAR(title_date) = 2019;

SELECT UPPER(first_name) AS name FROM employees;

SELECT DISTINCT first_name FROM employees;

DELETE FROM employees WHERE salary > 20000;

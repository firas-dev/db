# db
--1
select max(salary),min(salary),avg(salary),sum(salary) from hr.employees;
--2
select round(max(salary)) as MAX,round(min(salary)) as MIN ,round(avg(salary)) as AVERAGE,round(sum(salary)) as SUM from hr.employees;
--3 
select max(salary),min(salary),avg(salary),sum(salary),job_id from hr.employees group by job_id ;
--4
select count(*) as nombre_employées from hr.employees;
--5
SELECT d.department_name, COUNT(e.employee_id) AS nombre_employes
FROM hr.departments d
LEFT JOIN hr.employees e ON d.department_id = e.department_id
GROUP BY d.department_name; 
--6 
select job_id,count (employee_id) from hr.employees group by job_id ;
--7 
select count(department_id) as nombre_total_departments from hr.employees;
select count (nvl(department_id,0)) as nombre_total_departments from hr.employees;
--8


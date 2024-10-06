<h1 align="center" text="bold">
Employee Database Management System (SQL)
</h1> 


### *Introduction*
* This project involves creating an employee database to manage employee and department information for an organization.
* It includes creating tables to store relevant data and inserting initial records.
________________________________________________________________________________________________________________________

### *Database Creation*
* To create the database, use the following SQL command:

```
create database employeedb;
```
________________________________________________________________________________________________________________________

### *Database Usage*
* To use the created database, execute the following command:

```
use employeedb;
```
________________________________________________________________________________________________________________________

### Department Table

##### *Creating Department Table*
* To create the department table, execute the following SQL command:

```
create table department
(
    dept_number INT primary key not null,
    dept_name varchar(30) not null,
    loc varchar(30)
);
```

##### *Inserting Data into Department Table* 
* Insert sample data into the department table using the following command:

```
insert into department
values
      (10, 'accounting', 'new york'),
      (20,'research','dallas'),
      (30,'sales','chicago'),
      (40,'operations','boston');
```
________________________________________________________________________________________________________________________

### Employee Table

##### *Creating Employee Table* 
* To create the employee table, execute the following SQL command:

```
create table employee
(
    emp_number int primary KEY NOT NULL,
    emp_name varchar(10) not null,
    job varchar(20),
    mgr int,
    hire_date date not null,
    salary double check (sal > 0),
    commition int,
    dept_number int not null,
    foreign key (dept_number) references department(dept_number)
);
```

##### *Inserting Data into Employee Table* 
* Insert sample data into the employee table using the following command:

```
insert into employee (emp_number, emp_name, job, mgr, hire_date, salary, commition, dept_number)
values
	(7369, 'smith', 'clerk', 7902, '1980-12-17', 800, null, 20),
	(7499, 'allen', 'salesman', 7698, '1981-02-20', 1600, 300, 30),
	(7521, 'ward', 'salesman', 7698, '1981-02-22', 1250, 500, 30),
	(7566, 'jones', 'manger', 7839, '1981-04-02', 2975, null, 20),
	(7654, 'martin', 'salesman', 7698, '1981-09-28', 1250, 1400, 30),
	(7698, 'blake', 'manger', 7839, '1981-05-01', 2850, null, 30),
	(7782, 'clark', 'manger', 7839, '1981-06-09', 2450, null, 10),
	(7788, 'scott', 'analyst', 7566, '1987-04-19', 3000, null, 20),
	(7839, 'king', 'president', null, '1981-11-17', 5000, null, 10),
	(7844, 'turner', 'salesman', 7698, '1981-09-08', 1500, 0, 30),
	(7876, 'adams', 'clerk', 7788, '1987-05-23', 1100, null, 20),
	(7900, 'james', 'clerk', 7698, '1981-12-03', 950, null, 30),
	(7902, 'ford', 'analyst', 7566, '1981-02-20', 3000, null, 20),
	(7934, 'miller', 'clerk', 7782, '1982-01-23', 1300, null, 10);
```

________________________________________________________________________________________________________________________

### Conclusion
This SQL Employee Database project is designed to help manage employee and department information efficiently. Future enhancements may include adding more features such as updating and deleting records, as well as more complex queries for reporting.



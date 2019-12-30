# Attendance Management System.


## Features

### Feature 1: Login and Logout

  ``` sql
  create table employee(employee_id number,
emp_name varchar2(20) not null,
login_time timestamp ,logout_time timestamp default null,
constraint emp_id_pk primary key(employee_id));

insert into employee(employee_id,emp_name,login_time)values(1001,'ABCD',systimestamp);
'''

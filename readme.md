# Payroll Management System.


## Features

### Feature 1: Login and Logout

  ``` sql
  create table employee(employee_id number,
emp_name varchar2(20) not null,
login_time timestamp ,logout_time timestamp default null,
constraint emp_id_pk primary key(employee_id));

insert into employee(employee_id,emp_name,login_time)values(1001,'ABCD',systimestamp);



EMP_ID	EMP_NAME	DESIGNATION	LOGIN_TIME	LOGOUT_TIME	PERFORMANCE_GRADE	LEAVES_TAKEN
1001	Aadhav	DBA	31-12-19 02:16:35.351000000 PM	 	2	0
1011	Rahul	Project Manger	31-12-19 02:16:35.383000000 PM	 	1	0
1012	Vani	Project Manger	31-12-19 02:16:35.392000000 PM	 	3	1
1023	Thamos	Team Leader	31-12-19 02:16:35.401000000 PM	 	3	2
1112	Raji	Technical consultant	31-12-19 02:17:33.509000000 PM	 	1	0

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


<!DOCTYPE html>
<html>

<head>
  <meta charset='Cp1252'>
  
  <title>Responsive Table</title>
  
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  
  <style>
  * { 
    margin: 0; 
    padding: 0; 
  }
  body { 
    font: 14px/1.4 Georgia, Serif; 
  }
  
  /* 
  Generic Styling, for Desktops/Laptops 
  */
  table { 
    width: 100%; 
    border-collapse: collapse; 
  }
  /* Zebra striping */
  tr:nth-of-type(odd) { 
    background: #eee; 
  }
  th { 
    background: #333; 
    color: white; 
    font-weight: bold; 
  }
  td, th { 
    padding: 6px; 
    border: 1px solid #9B9B9B; 
    text-align: left; 
  }
  @media 
  only screen and (max-width: 760px),
  (min-device-width: 768px) and (max-device-width: 1024px)  {
    table, thead, tbody, th, td, tr { display: block; }
    thead tr { position: absolute;top: -9999px;left: -9999px;}
    tr { border: 1px solid #9B9B9B; }
    td { border: none;border-bottom: 1px solid #9B9B9B; position: relative;padding-left: 50%; }
    
    td:before { position: absolute;top: 6px;left: 6px;width: 45%; padding-right: 10px; white-space: nowrap;}
    
    /*
    Label the data
    */
td:nth-of-type(0):before { content: "EMP_ID"; }
td:nth-of-type(1):before { content: "EMP_NAME"; }
td:nth-of-type(2):before { content: "DESIGNATION"; }
td:nth-of-type(3):before { content: "LOGIN_TIME"; }
td:nth-of-type(4):before { content: "LOGOUT_TIME"; }
td:nth-of-type(5):before { content: "PERFORMANCE_GRADE"; }
td:nth-of-type(6):before { content: "LEAVES_TAKEN"; }
  }
  
  /* Smartphones (portrait and landscape) ----------- */
  @media only screen
  and (min-device-width : 320px)
  and (max-device-width : 480px) {
    body { 
      padding: 0; 
      margin: 0; 
      width: 320px; }
    }
  
  /* iPads (portrait and landscape) ----------- */
  @media only screen and (min-device-width: 768px) and (max-device-width: 1024px) {
    body { 
      width: 495px; 
    }
  }
  
  </style>
  <!--<![endif]-->
<script type="text/javascript">

function search(){
  
  var s = document.getElementById('search').value;

  rows = document.getElementById('data').getElementsByTagName('TR');
  for(var i=0;i<rows.length;i++){
    if ( rows[i].textContent.indexOf(s)>0 ) {
	  rows[i].style.display ='';
    } else {
      rows[i].style.display ='none';
    }
  }
}


var timer;
function delayedSearch() {
	clearTimeout(timer);
	console.log('delay-ing')
    timer = setTimeout(function () {
		console.log('delay-running')
		search();
    }, 500);
  }</script>
</head>

<body>
<div><input type="text" size="30" maxlength="1000" value="" id="search" onkeyup="delayedSearch();" /><input type="button" value="Go" onclick="lsearch();"/> </div>
<table><thead><tr>	<th>EMP_ID</th>
	<th>EMP_NAME</th>
	<th>DESIGNATION</th>
	<th>LOGIN_TIME</th>
	<th>LOGOUT_TIME</th>
	<th>PERFORMANCE_GRADE</th>
	<th>LEAVES_TAKEN</th>
</tr></thead>
<tbody id="data">

	<tr>
<td align="right">1001</td>
<td>Aadhav</td>
<td>DBA</td>
<td>31-12-19 02:16:35.351000000 PM</td>
<td>&nbsp;</td>
<td align="right">2</td>
<td align="right">0</td>
	</tr>
	<tr>
<td align="right">1011</td>
<td>Rahul</td>
<td>Project Manger</td>
<td>31-12-19 02:16:35.383000000 PM</td>
<td>&nbsp;</td>
<td align="right">1</td>
<td align="right">0</td>
	</tr>
	<tr>
<td align="right">1012</td>
<td>Vani</td>
<td>Project Manger</td>
<td>31-12-19 02:16:35.392000000 PM</td>
<td>&nbsp;</td>
<td align="right">3</td>
<td align="right">1</td>
	</tr>
	<tr>
<td align="right">1023</td>
<td>Thamos</td>
<td>Team Leader</td>
<td>31-12-19 02:16:35.401000000 PM</td>
<td>&nbsp;</td>
<td align="right">3</td>
<td align="right">2</td>
	</tr>
	<tr>
<td align="right">1112</td>
<td>Raji</td>
<td>Technical consultant</td>
<td>31-12-19 02:17:33.509000000 PM</td>
<td>&nbsp;</td>
<td align="right">1</td>
<td align="right">0</td>
	</tr>
</tbody></table><!-- SQL:
select * from employee--></body></html>

| EMP_ID | EMP_NAME |      DESIGNATION     | PERFORMANCE_GRADE | LEAVES_TAKEN | SALARY | TOTAL_LEAVES |
|:------:|:--------:|:--------------------:|:-----------------:|:------------:|:------:|:------------:|
|  1001  |  Aadhav  |          DBA         |         2         |       1      |  20000 |      11      |
|  1011  |   Rahul  |    Project Manager   |         1         |       0      |  25000 |      12      |
|  1012  |   Vani   |    Project Manager   |         3         |       1      |  25000 |      11      |
|  1023  |  Thomas  |      Team Leader     |         3         |       2      |  20000 |      10      |
|  1112  |   Raji   | Technical consultant |         1         |       0      |  15000 |      12      |


| EMP_ID | ALLOWANCE | SALARY_INCREMENT |
|:------:|:---------:|:----------------:|
|  1001  |    500    |         0        |
|  1011  |    700    |         0        |
|  1012  |    600    |         0        |
|  1023  |    500    |         0        |
|  1112  |    300    |         0        |


| EMP_ID | FOOD_DETECTION | CAB_DETECTION | LOSS_OF_PAY | PROVIDENT_FUND |
|:------:|:--------------:|:-------------:|:-----------:|:--------------:|
|  1001  |       200      |      2000     |      0      |      1000      |
|  1011  |        1       |      1000     |      0      |      1000      |
|  1012  |        0       |      1000     |      0      |      1000      |
|  1023  |       200      |       0       |      0      |      1000      |
|  1112  |        0       |       0       |      0      |      1000      |


| EMP_ID |           LOGIN_TIME           | LOGOUT_TIME |
|:------:|:------------------------------:|:-----------:|
|  1001  | 02-01-20 05:42:26.921000000 PM |      0      |
|  1011  | 02-01-20 05:42:26.921000000 PM |      0      |
|  1012  | 02-01-20 05:42:26.921000000 PM |      0      |
|  1023  | 02-01-20 05:42:26.921000000 PM |      0      |
|  1112  | 02-01-20 05:42:26.921000000 PM |      0      |



| EMP_ID | FINAL_SALARY |
|:------:|:------------:|
|  1001  |       0      |
|  1011  |       0      |
|  1012  |       0      |
|  1023  |       0      |
|  1112  |       0      |

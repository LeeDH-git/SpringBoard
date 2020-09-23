# SpringBoard

#DB name : test
table name : i_can_do_it

<---- copy and paste ---->

CREATE TABLE i_can_do_it(
	no int(10) NOT NULL AUTO_INCREMENT PRIMARY KEY, 
	id varchar(50) NOT NULL UNIQUE,
	name varchar(50),
	goal varchar(255),
	date date,
	time time
);

alter table i_can_do_it add position_code varchar(5) NOT NULL; 
ALTER TABLE i_can_do_it COMMENT = '나는 할 수 있다.';

CREATE TABLE position_code(
	position_code varchar(5) NOT NULL PRIMARY KEY,
	position_name varchar(10) NOT NULL
);
ALTER TABLE i_can_do_it COMMENT = "직급_코드 테이블";

insert into i_can_do_it(id,name,goal,date,time,position_code)
	values('9618', '짱구', '부문장', NOW(), NOW(), '02');

insert into i_can_do_it(id,name,goal,date,time,position_code)
	values('1255', '맹구', '실장', NOW(), NOW(), '03');

insert into i_can_do_it(id,name,goal,date,time,position_code)
	values('6489', '영희', '팀장', NOW(), NOW(), '04');

insert into i_can_do_it(id,name,goal,date,time,position_code)
	values('0113', '철수', '파트장', NOW(), NOW(), '05');

insert into i_can_do_it(id,name,goal,date,time,position_code)
	values('6378', '훈이', '파트장', NOW(), NOW(), '05');

insert into i_can_do_it(id,name,goal,date,time,position_code)
	values('4963', '치타', '파트장', NOW(), NOW(), '05');

insert into i_can_do_it(id,name,goal,date,time,position_code)
	values('2978', '원장쌤', '담당', NOW(), NOW(), '06');

insert into i_can_do_it(id,name,goal,date,time,position_code)
	values('7542', '흰둥이', '담당', NOW(), NOW(), '06');
  
  insert into position_code(position_code, position_name)
	values('00', '사장');

insert into position_code(position_code, position_name)
	values('01', '부문장');

insert into position_code(position_code, position_name)
	values('02', '실장');

insert into position_code(position_code, position_name)
	values('03', '팀장');

insert into position_code(position_code, position_name)
	values('04', '파트장');

insert into position_code(position_code, position_name)
	values('05', '담당');

insert into position_code(position_code, position_name)
	values('06', '인턴');

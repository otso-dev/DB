
# transaction
show variables like 'AUTOCOMMIT';
set autocommit = 0;

start transaction;

savepoint sp1;

insert into user_mst
values(0,'kkk12','123452','김준일','kkk12@gmail.com');

select * from user_mst;

rollback to sp1;

commit;

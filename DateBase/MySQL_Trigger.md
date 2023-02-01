# Trigger
Table에 어떤 신호가 가해졌을 때 미리 정해진 활동이 자동으로 실행되는 것  
구체적으로 특정 테이블에 Insert,Delete,Update 같은 DML문이 수행될 때  
데이터베이스에서 자동으로 동작을 한다.  
After는 대부분 insert에서 쓰인다.
Before는 대부분 delete에서 쓰인다.
updates는 상황에 따라 After,Before 둘다 쓴다.

## After
``` mysql
CREATE DEFINER=`root`@`localhost` TRIGGER `user_mst_AFTER_INSERT` AFTER INSERT ON `user_mst` FOR EACH ROW BEGIN
	insert into user_dtl(user_id)
    values(new.user_id);
END
```

## Before
``` mysql
CREATE DEFINER=`root`@`localhost` TRIGGER `user_mst_BEFORE_DELETE` BEFORE DELETE ON `user_mst` FOR EACH ROW BEGIN
	delete
    from
		role_dtl
	where
		user_id = old.user_id; /* old는 기존의 것을 들고옴 */
        
	delete
    from
		user_dtl
	where user_id = old.user_id;
END
```

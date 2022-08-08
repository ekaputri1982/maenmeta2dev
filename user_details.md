Table : user_details
--------------------

```SQL
USE maenmeta2dev

CREATE TABLE `user_details` (
	`userid` INT(11) NOT NULL,
	`gender` TINYINT(4) NULL DEFAULT NULL COMMENT '1:m 2:f',
	`nickname` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`office` INT(11) NOT NULL,
	`collapsed` TINYINT(4) NOT NULL DEFAULT '0',
	`notif` TINYINT(4) NOT NULL DEFAULT '1',
	PRIMARY KEY (`userid`) USING BTREE,
	INDEX `office` (`office`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
;
```
__Notes__

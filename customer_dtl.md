Table : customer_dtl
--------------------

```SQL
USE maenmeta2dev

CREATE TABLE `customer_dtl` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`customer` INT(11) UNSIGNED ZEROFILL NOT NULL,
	`method` VARCHAR(20) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`location` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`dtime` BIGINT(20) NOT NULL,
	`response` VARCHAR(20) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`phase` TINYINT(4) NOT NULL COMMENT '1: follow up , 2: closing , 3: refused , 4: invalid , 5 : maintain',
	`details` TEXT NOT NULL COLLATE 'latin1_swedish_ci',
	`user` INT(11) NOT NULL,
	`updated` BIGINT(20) NOT NULL,
	`tags` VARCHAR(20) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	PRIMARY KEY (`id`) USING BTREE,
	INDEX `idx_phase` (`phase`) USING BTREE,
	INDEX `customer` (`customer`) USING BTREE,
	INDEX `user` (`user`) USING BTREE
)
COMMENT='detail of opportunity (history follow-up clients)'
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=79055
;
```
__Notes__

+ __Table: customer_dtl__ Give an information of record-keeping detail from marketing team plan.
  
+ __dtime__ (unix-timestamp). It is function to return a Unix timestamp. A Unix timestamp is the number of seconds that have elapsed since ‘1970-01-01 00:00:00’ UTC as an epoch year. It can be used on the current date/time or another specified date/time.
  
+ __updated__ (unix-timestamp). It is function to return a Unix timestamp. A Unix timestamp is the number of seconds that have elapsed since ‘1970-01-01 00:00:00’ UTC as an epoch year. It can be used on the current date/time or another specified date/time.

+ __phase__ Step of timeline classification from consultant to user: 1.follow up, 2.closing, 3.refused, 4.invalid, 5.maintain.


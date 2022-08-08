Table : auto_chop
-----------------

```SQL
USE maenmeta2dev

CREATE TABLE `auto_chop` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`date` DATE NULL DEFAULT NULL,
	`crm_id` INT(11) UNSIGNED ZEROFILL NOT NULL,
	`marketing` VARCHAR(10) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`rolling` BIGINT(20) NULL DEFAULT NULL,
	`expired` BIGINT(20) NULL DEFAULT NULL,
	`created_at` DATETIME NULL DEFAULT utc_timestamp(),
	PRIMARY KEY (`id`) USING BTREE,
	INDEX `crm_id` (`crm_id`) USING BTREE,
	INDEX `marketing` (`marketing`) USING BTREE
)
COLLATE='utf8_general_ci'
ENGINE=InnoDB
;
```
__Notes__

+ __Table: auto_chop__ If within and extended period of time (3 months) the sales marketing process is not closed, and that is a failure to make sure a collecting leads of ideal target market of customer. It will enabling sales marketing process to roll the customer into the other customer relationship agents to evaluate the return on lead investments.
  
+ __id__ (Primary Key, Integer, Auto Increment).

+ __created_at__ (datetime, utc_timestamp).

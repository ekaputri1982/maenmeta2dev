Table : customer
----------------

```SQL
USE maenmeta2dev

CREATE TABLE `customer` (
	`id` INT(11) UNSIGNED ZEROFILL NOT NULL,
	`phone` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`event` INT(11) UNSIGNED NOT NULL COMMENT 'time created in CRM',
	`fullname` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`nickname` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`email` VARCHAR(255) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`mobile` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`mobile2` VARCHAR(200) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`bbm` VARCHAR(20) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`address` TEXT NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`city` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`country` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`profession` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`birthday` DATE NULL DEFAULT NULL,
	`religion` VARCHAR(20) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`info` TEXT NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`trading` TEXT NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`marketing` VARCHAR(10) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`maintenance` VARCHAR(10) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`investor` TINYINT(4) UNSIGNED NOT NULL DEFAULT '0' COMMENT '0:none, 1:closed, 2:declined, 3:invalid',
	`source` VARCHAR(20) NULL DEFAULT NULL COMMENT 'brokers (0:manual)' COLLATE 'latin1_swedish_ci',
	`prospect` TINYINT(4) UNSIGNED NULL DEFAULT NULL COMMENT '1: alot, 2: hot',
	`take_over` TINYINT(4) NULL DEFAULT '0',
	`rolling` BIGINT(20) UNSIGNED NULL DEFAULT NULL COMMENT 'save unixtime when opportunity is assigned/rolling',
	`expired` BIGINT(20) UNSIGNED NULL DEFAULT NULL COMMENT 'save unixtime for expired data',
	`merge_id` INT(11) UNSIGNED ZEROFILL NULL DEFAULT NULL,
	`noteadm` TEXT NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`notemkt` TEXT NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`pin` TINYINT(4) NULL DEFAULT NULL COMMENT 'pin priority client',
	`MODIFY_TIME` BIGINT(20) UNSIGNED NOT NULL,
	PRIMARY KEY (`id`) USING BTREE,
	UNIQUE INDEX `unik_customer` (`email`, `phone`, `source`, `merge_id`) USING BTREE,
	INDEX `idx_marketing` (`marketing`) USING BTREE,
	INDEX `fullname` (`fullname`) USING BTREE,
	INDEX `phone` (`phone`) USING BTREE,
	INDEX `mobile` (`mobile`) USING BTREE,
	INDEX `maintenance` (`maintenance`) USING BTREE,
	INDEX `rolling` (`rolling`) USING BTREE,
	INDEX `expired` (`expired`) USING BTREE,
	INDEX `prospect` (`prospect`) USING BTREE,
	INDEX `source` (`source`) USING BTREE,
	INDEX `pin` (`pin`) USING BTREE,
	INDEX `mobile2` (`mobile2`) USING BTREE,
	INDEX `customer_take_over` (`take_over`) USING BTREE
)
COLLATE='utf8mb4_general_ci'
ENGINE=InnoDB
;
```
__Notes__

+ __Table: customer__ It contains all information about customer.
  
+ __id__ (Primary Key).

+ __email, phone, source, merge_id__ (Unique Key).

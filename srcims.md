Table : srcims
--------------

```SQL
USE maenmeta2dev

CREATE TABLE `srcims` (
	`id` INT(11) UNSIGNED NOT NULL AUTO_INCREMENT,
	`crm_id` INT(11) UNSIGNED ZEROFILL NULL DEFAULT NULL,
	`registered` INT(11) NOT NULL,
	`ims_id` VARCHAR(20) NOT NULL COLLATE 'latin1_swedish_ci',
	`username` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`fullname` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`email` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`phone` VARCHAR(30) NOT NULL COLLATE 'latin1_swedish_ci',
	`mobile` VARCHAR(30) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`bbm` VARCHAR(20) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`birthday` DATE NULL DEFAULT NULL,
	`source` INT(11) NOT NULL,
	`address` TEXT NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`city` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`country` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`first_ref` TEXT NULL DEFAULT NULL COMMENT 'user_ref_url (MRG)' COLLATE 'latin1_swedish_ci',
	`last_ref` TEXT NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`first_visit` TEXT NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`goal_ref` TEXT NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`referrer` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`bankname` VARCHAR(20) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`bankaccno` VARCHAR(20) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`bankreg` VARCHAR(100) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`info_regis` TINYINT(4) NOT NULL DEFAULT '1' COMMENT '1: new regis , 2: regis ulang ,  3: international',
	`investor` TINYINT(4) NULL DEFAULT NULL COMMENT '1: investor',
	`email_ver` TINYINT(4) NOT NULL DEFAULT '0',
	`notes` TEXT NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`MODIFY_TIME` BIGINT(20) NOT NULL DEFAULT '0',
	PRIMARY KEY (`id`) USING BTREE,
	UNIQUE INDEX `UNIK` (`ims_id`, `email`, `source`, `username`) USING BTREE,
	INDEX `fullname` (`fullname`) USING BTREE,
	INDEX `email` (`email`) USING BTREE,
	INDEX `phone` (`phone`) USING BTREE,
	INDEX `username` (`username`) USING BTREE,
	INDEX `crm_id` (`crm_id`) USING BTREE,
	INDEX `source` (`source`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=75570
;
```
__Notes__

+ __id__ (Primary Key, Integer, Auto Increment).

+ __ims_id, email, source, username__ Unique Key.
  
  
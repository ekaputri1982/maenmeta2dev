Table : srcmanual
-----------------

```SQL
USE maenmeta2dev

CREATE TABLE `srcmanual` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`crm_id` INT(11) UNSIGNED ZEROFILL NULL DEFAULT NULL,
	`fullname` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`email` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`phone` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`address` TEXT NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`event` INT(11) NOT NULL,
	`source` INT(11) NOT NULL,
	`notes` TEXT NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`user` INT(11) NOT NULL,
	`broker` INT(11) NULL DEFAULT NULL,
	PRIMARY KEY (`id`) USING BTREE,
	INDEX `source` (`source`) USING BTREE,
	INDEX `admin` (`user`) USING BTREE,
	INDEX `crm_id` (`crm_id`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=1408
;
```
__Notes__

+ __id__ (Primary Key, Integer, Auto Increment).

+ __crm_id__ customer relationship managemend id.
  
+ __srcmanual__ berisi data informasi dari crm_id.
  
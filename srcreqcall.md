Table : srcreqcall
------------------

```SQL
USE maenmeta2dev

CREATE TABLE `srcreqcall` (
	`id` INT(11) UNSIGNED NOT NULL AUTO_INCREMENT,
	`crm_id` INT(11) UNSIGNED ZEROFILL NULL DEFAULT NULL,
	`req_id` INT(11) NOT NULL,
	`ims_id` INT(11) NOT NULL,
	`email` VARCHAR(50) NOT NULL DEFAULT '' COLLATE 'latin1_swedish_ci',
	`phone` VARCHAR(50) NOT NULL DEFAULT '' COLLATE 'latin1_swedish_ci',
	`waktu` DATETIME NOT NULL,
	`comments` TEXT NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`notes` TEXT NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`source` VARCHAR(50) NULL DEFAULT 'callback' COLLATE 'latin1_swedish_ci',
	`created_at` DATETIME NOT NULL,
	`updated_at` DATETIME NULL DEFAULT NULL,
	PRIMARY KEY (`id`) USING BTREE,
	UNIQUE INDEX `req_id` (`req_id`) USING BTREE,
	INDEX `crm_id` (`crm_id`) USING BTREE,
	INDEX `ims_id` (`ims_id`) USING BTREE,
	INDEX `created_at` (`created_at`) USING BTREE,
	INDEX `updated_at` (`updated_at`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=6
;
```
__Notes__

+ __id__ (Primary Key, Integer, Auto Increment).

+ __req_id__ merupakan Unique Key.
  
+ __crm_id__ Identification for CRM (Customer Relationship Management).

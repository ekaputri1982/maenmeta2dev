Table : srclivechat
-------------------

```SQL
USE maenmeta2dev

CREATE TABLE `srclivechat` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`crm_id` INT(11) UNSIGNED ZEROFILL NULL DEFAULT NULL,
	`fullname` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`email` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`phone` VARCHAR(20) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`online` TINYINT(4) NOT NULL DEFAULT '1' COMMENT '1: on / 2: off',
	`source` INT(11) NOT NULL,
	`media` VARCHAR(10) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`event` INT(11) NOT NULL,
	`content` TEXT NOT NULL COLLATE 'latin1_swedish_ci',
	`response` TEXT NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`ref_site` TEXT NULL DEFAULT NULL COMMENT 'from web (offline)' COLLATE 'latin1_swedish_ci',
	`page` TEXT NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`user` INT(11) NULL DEFAULT NULL COMMENT 'onduty staff',
	`method` VARCHAR(20) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`location` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`claim` TINYINT(4) NOT NULL DEFAULT '0',
	`approve` TINYINT(4) NOT NULL DEFAULT '0',
	`MODIFY_TIME` BIGINT(20) NULL DEFAULT '0',
	PRIMARY KEY (`id`) USING BTREE,
	INDEX `crm_id` (`crm_id`) USING BTREE,
	INDEX `user` (`user`) USING BTREE,
	INDEX `source` (`source`) USING BTREE,
	INDEX `email` (`email`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=29122
;
```
__Notes__

+ __Table: srclivechat__ Live chat support that is a web service for businesses that allows visitors to communicate with the business, usually through real-time live chat. Live support is designed to provide customers and clients with immediate support and information. The Web service is integrated with the business website and generally includes invisible website traffic analysis and secure administrative controls.
  
+ __id__ (Primary Key, Integer, Auto Increment).
  




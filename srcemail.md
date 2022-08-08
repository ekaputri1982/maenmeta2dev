Table : srcemail
----------------

```SQL
USE maenmeta2dev

CREATE TABLE `srcemail` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`crm_id` INT(10) UNSIGNED ZEROFILL NULL DEFAULT NULL,
	`fullname` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`email` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`phone` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`source` INT(11) NOT NULL,
	`support` INT(11) NOT NULL COMMENT 'email support',
	`event` INT(11) NOT NULL,
	`sbjemail` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`content` TEXT NOT NULL COLLATE 'latin1_swedish_ci',
	`reply` TEXT NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`user` INT(11) NOT NULL,
	PRIMARY KEY (`id`) USING BTREE,
	INDEX `crm_id` (`crm_id`) USING BTREE,
	INDEX `user` (`user`) USING BTREE,
	INDEX `support` (`support`) USING BTREE,
	INDEX `source` (`source`) USING BTREE,
	INDEX `fullname` (`fullname`) USING BTREE,
	INDEX `email` (`email`) USING BTREE,
	INDEX `phone` (`phone`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=5946
;
```
__Notes__

+ __id__ (Primary Key, Integer, Auto Increment).
  
+ __crm_id, user, support, source, fullname, email, phone__ Index Key.

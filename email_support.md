Table : email_support
---------------------

```SQL
USE maenmeta2dev

CREATE TABLE `email_support` (
	`id` INT(11) UNSIGNED NOT NULL AUTO_INCREMENT,
	`source` VARCHAR(20) NOT NULL COLLATE 'latin1_swedish_ci',
	`email` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`status` TINYINT(3) UNSIGNED NOT NULL DEFAULT '1',
	PRIMARY KEY (`id`) USING BTREE,
	INDEX `source` (`source`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=41
;
```
__Notes__

+ __id__ (Primary Key, Auto Increment).
  
+ __status__ It contains leads email support when users contact/send a message to email support then CA (Client Analyst) will put the information on CRM (Customer Relationship Management) platform: 1 for default).

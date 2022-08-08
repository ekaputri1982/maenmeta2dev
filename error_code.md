Table : error_code
------------------

```SQL
USE maenmeta2dev

CREATE TABLE `error_code` (
	`id` INT(10) UNSIGNED NOT NULL AUTO_INCREMENT,
	`file` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`message` TEXT NOT NULL COLLATE 'latin1_swedish_ci',
	PRIMARY KEY (`id`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=3
;
```
__Notes__

+ __id__ (Primary Key, Integer, Auto Increment).
  
+ __Table: error_code__ Notice all filter of warning messages.
  
Table : office
--------------

```SQL
USE maenmeta2dev

CREATE TABLE `office` (
	`id` TINYINT(4) NOT NULL AUTO_INCREMENT,
	`location` VARCHAR(10) NOT NULL COLLATE 'latin1_swedish_ci',
	`address` TEXT NOT NULL COLLATE 'latin1_swedish_ci',
	`status` TINYINT(4) NOT NULL DEFAULT '1',
	PRIMARY KEY (`id`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=4
;
```
__Notes__

+ __id__ (Primary Key, Auto Increment).
  
+ __Table: office__ Information of several main offices in different cities.
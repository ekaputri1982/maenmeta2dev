Table : srcmanual_from
----------------------

```SQL
USE maenmeta2dev

CREATE TABLE `srcmanual_from` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`name` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	PRIMARY KEY (`id`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=14
;
```
__Notes__

+ __id__ (Primary Key, Integer, Auto Increment).
  
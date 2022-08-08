Table : server
--------------

```SQL
USE maenmeta2dev

CREATE TABLE `server` (
	`ID` INT(11) NOT NULL AUTO_INCREMENT,
	`host` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`manager` INT(11) NOT NULL,
	PRIMARY KEY (`ID`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=11
;
```
__Notes__

+ __id__ (Primary Key, Integer, Auto Increment).
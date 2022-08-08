Table : cifeicom_settings
-------------------------

```SQL
USE maenmeta2dev

CREATE TABLE `cifeicom_settings` (
	`name` VARCHAR(20) NOT NULL COLLATE 'latin1_swedish_ci',
	`value` TEXT NOT NULL COLLATE 'latin1_swedish_ci',
	PRIMARY KEY (`name`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
;
```
__Notes__




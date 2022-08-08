Table : configs
---------------

```SQL
USE maenmeta2dev

CREATE TABLE `configs` (
	`cfg` VARCHAR(64) NOT NULL COLLATE 'utf8_general_ci',
	`value` VARCHAR(255) NOT NULL COLLATE 'utf8_general_ci',
	PRIMARY KEY (`cfg`) USING BTREE
)
COLLATE='utf8_general_ci'
ENGINE=InnoDB
;
```
__Notes__

+ __Table: configs__ in which the component are arranged to make up the computer system, it consists of software/hardware configuration.

+ __cfg__ (Primary Key), token secret key.


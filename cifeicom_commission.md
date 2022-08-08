Table : cifeicom_commission
---------------------------

```SQL
USE maenmeta2dev

CREATE TABLE `cifeicom_commission` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`gid` INT(11) NOT NULL,
	`minlot` DOUBLE NOT NULL,
	`maxlot` DOUBLE NOT NULL,
	`usdlot` DOUBLE NOT NULL,
	`idrate` DOUBLE NOT NULL,
	PRIMARY KEY (`id`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=2
;
```
__Notes__

+ __id__ (Primary Key, Integer, Auto Increment).

+ __gid__ Group Identification.

+ __minlot__ Minimum lot of currency trading lot size which is lot as a unit measuring a transaction amount.
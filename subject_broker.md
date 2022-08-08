Table : subject_broker
----------------------

```SQL
USE maenmeta2dev

CREATE TABLE `subject_broker` (
	`id` INT(11) UNSIGNED NOT NULL AUTO_INCREMENT,
	`subject_id` INT(11) UNSIGNED NOT NULL,
	`broker_id` INT(11) UNSIGNED NOT NULL,
	PRIMARY KEY (`id`) USING BTREE,
	UNIQUE INDEX `subject_broker_id` (`subject_id`, `broker_id`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=399
;
```
__Notes__

+ __id__ (Primary Key, Integer, Auto Increment).

+ __subject_broker__ A broker is a financial services company that provides traders access to a platform for buying and selling foreign currencies. Forex is short for foreign exchange. Transactions in the forex market are always between a pair of two different currencies.

+ __subject_id, broker_id__ merupakan Unique Key.
Table : migrations
------------------

```SQL
USE maenmeta2dev

CREATE TABLE `migrations` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`timestamp` BIGINT(20) NOT NULL,
	`name` VARCHAR(255) NOT NULL COLLATE 'utf8_general_ci',
	PRIMARY KEY (`id`) USING BTREE
)
COLLATE='utf8_general_ci'
ENGINE=InnoDB
AUTO_INCREMENT=42
;
```
__Notes__

+ __id__ (Primary Key, Integer, Auto Increment).
  
+ __timestamp__ (unix-timestamp). It is a function to return a Unix timestamp. A Unix timestamp is the number of seconds that have elapsed since ‘1970-01-01 00:00:00’ UTC as an epoch year. It can be used on the current date/time or another specified date/time.

+ __migrations__ Users migration information table.
  
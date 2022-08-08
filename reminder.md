Table : reminder
----------------

```SQL
USE maenmeta2dev

CREATE TABLE `reminder` (
	`id` BIGINT(20) NOT NULL AUTO_INCREMENT,
	`clientid` BIGINT(20) NOT NULL,
	`notes` TEXT NOT NULL COLLATE 'latin1_swedish_ci',
	`datetime` BIGINT(20) NOT NULL DEFAULT '0',
	`postphone` BIGINT(20) NOT NULL DEFAULT '0',
	`userid` BIGINT(20) NOT NULL,
	`active` TINYINT(4) NOT NULL,
	`posted` BIGINT(20) NOT NULL,
	PRIMARY KEY (`id`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=229
;
```
__Notes__

+ __datetime__ (unix-timestamp). It is function to return a Unix timestamp. A Unix timestamp is the number of seconds that have elapsed since ‘1970-01-01 00:00:00’ UTC as an epoch year. It can be used on the current date/time or another specified date/time.
  
+ __posted__ (unix-timestamp). It is function to return a Unix timestamp. A Unix timestamp is the number of seconds that have elapsed since ‘1970-01-01 00:00:00’ UTC as an epoch year. It can be used on the current date/time or another specified date/time.
  
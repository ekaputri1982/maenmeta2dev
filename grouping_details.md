Table : grouping_details
------------------------

```SQL
USE maenmeta2dev

CREATE TABLE `grouping_details` (
	`id` BIGINT(20) NOT NULL AUTO_INCREMENT,
	`gid` INT(11) NOT NULL,
	`account` INT(11) NOT NULL,
	`start` DATE NOT NULL DEFAULT '1970-01-01',
	`end` DATE NOT NULL DEFAULT '2999-12-31',
	`del` TINYINT(4) NOT NULL DEFAULT '0',
	`userid` INT(11) NOT NULL,
	`chop` DATETIME NULL DEFAULT NULL,
	PRIMARY KEY (`id`) USING BTREE,
	UNIQUE INDEX `Index 2` (`gid`, `account`, `start`, `end`) USING BTREE,
	INDEX `gid` (`gid`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=7623254
;
```
__Notes__

+ __gid__ Group Identification.

+ __Table: grouping details__ Data grouping_details is performed using a group by clause that allows us to group individual data based on defined criteria. The creator will make a list of all users that will be put on the listed group, then they will get an information afterwards.

Table : grouping_share
----------------------

```SQL
USE maenmeta2dev

CREATE TABLE `grouping_share` (
	`userid` INT(11) NOT NULL,
	`groupid` INT(11) NOT NULL,
	`cmd` VARCHAR(12) NOT NULL COLLATE 'latin1_swedish_ci',
	PRIMARY KEY (`userid`, `groupid`, `cmd`) USING BTREE,
	INDEX `FK_grouping_share_grouping` (`groupid`) USING BTREE,
	INDEX `userid` (`userid`) USING BTREE,
	CONSTRAINT `FK_grouping_share_grouping` FOREIGN KEY (`groupid`) REFERENCES `grouping` (`id`) ON UPDATE CASCADE ON DELETE CASCADE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
;
```
__Notes__

+ __userid, groupid, cmd__ (Primary Key).
  
+ __groupid__ Column groupid will be linked with __grouping__ table. It contains group list that will be a target for campaign and many informations.
Table : users_spesific_rules
----------------------------

```SQL
USE maenmeta2dev

CREATE TABLE `users_spesific_rules` (
	`userid` INT(11) NOT NULL,
	`ruleid` INT(11) NOT NULL,
	PRIMARY KEY (`userid`, `ruleid`) USING BTREE,
	INDEX `userid` (`userid`) USING BTREE
)
COLLATE='utf8_general_ci'
ENGINE=InnoDB
;
```
__Notes__

+ __Table: users_spesific_rules__ the data of userid and ruleid of rules that have been given to users to get a few access of selected criteria.
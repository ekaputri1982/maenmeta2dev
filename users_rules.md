Table : users_rules
-------------------

```SQL
USE maenmeta2dev

CREATE TABLE `users_rules` (
	`id` INT(11) NOT NULL,
	`rules` VARCHAR(128) NOT NULL COLLATE 'utf8_general_ci',
	`state` TINYINT(4) NOT NULL DEFAULT '0',
	PRIMARY KEY (`id`) USING BTREE,
	UNIQUE INDEX `rules` (`rules`) USING BTREE,
	INDEX `state` (`state`) USING BTREE
)
COLLATE='utf8_general_ci'
ENGINE=InnoDB
;
```
__Notes__

+ __Table: users_rules__ the right of rules that have been given to users to get a few access of selected criteria.


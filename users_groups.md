Table : users_groups
--------------------

```SQL
USE maenmeta2dev

CREATE TABLE `users_groups` (
	`id` INT(11) NOT NULL,
	`path` VARCHAR(1024) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`name` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	PRIMARY KEY (`id`) USING BTREE,
	UNIQUE INDEX `name` (`name`) USING BTREE,
	UNIQUE INDEX `path` (`path`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
;
```
__Notes__

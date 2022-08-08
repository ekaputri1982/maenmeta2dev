Table : users_mrg
-----------------

```SQL
USE maenmeta2dev

CREATE TABLE `users_mrg` (
	`user_id` INT(11) NOT NULL,
	`mrg_id` INT(11) NULL DEFAULT NULL,
	PRIMARY KEY (`user_id`) USING BTREE,
	UNIQUE INDEX `mrg_id` (`mrg_id`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
ROW_FORMAT=COMPACT
;
```
__Notes__

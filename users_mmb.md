Table : users_mmb
-----------------

```SQL
USE maenmeta2dev

CREATE TABLE `users_mmb` (
	`user_id` INT(11) NOT NULL,
	`mmb_id` INT(11) NULL DEFAULT NULL,
	PRIMARY KEY (`user_id`) USING BTREE,
	UNIQUE INDEX `mmb_id` (`mmb_id`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
;
```
__Notes__


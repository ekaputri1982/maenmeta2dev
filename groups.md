Table : groups
--------------

```SQL
USE maenmeta2dev

CREATE TABLE `groups` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`name` VARCHAR(100) NOT NULL COLLATE 'utf8_general_ci',
	`creator_id` INT(11) NOT NULL,
	`created_at` DATETIME NULL DEFAULT utc_timestamp(),
	`updated_at` DATETIME NULL DEFAULT utc_timestamp(),
	PRIMARY KEY (`id`) USING BTREE,
	UNIQUE INDEX `name` (`name`) USING BTREE,
	INDEX `creator_id` (`creator_id`) USING BTREE,
	CONSTRAINT `groups_ibfk_1` FOREIGN KEY (`creator_id`) REFERENCES `users` (`id`) ON UPDATE RESTRICT ON DELETE RESTRICT
)
COLLATE='utf8_general_ci'
ENGINE=InnoDB
;
```
__Notes__

+ __id__ (Primary Key, Integer, Auto Increment).

+ __creator_id__ User who have rights to list all users that mentioned on grouping_share table.
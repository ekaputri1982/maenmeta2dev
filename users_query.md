Table : users_query
-------------------

```SQL
USE maenmeta2dev

CREATE TABLE `users_query` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`user_id` INT(11) NOT NULL,
	`widget_id` VARCHAR(50) NOT NULL COLLATE 'utf8_general_ci',
	`title` VARCHAR(255) NOT NULL COLLATE 'utf8_general_ci',
	`query_text` TEXT NOT NULL COLLATE 'utf8_general_ci',
	`created_at` DATETIME NULL DEFAULT utc_timestamp(),
	PRIMARY KEY (`id`) USING BTREE,
	INDEX `user_id` (`user_id`) USING BTREE,
	INDEX `widget_id` (`widget_id`) USING BTREE,
	INDEX `title` (`title`) USING BTREE,
	INDEX `created_at` (`created_at`) USING BTREE
)
COLLATE='utf8_general_ci'
ENGINE=InnoDB
AUTO_INCREMENT=46
;
```
__Notes__

+ __Table: users_query__ Contains information of user_id whom get an access to make a query for trend analysis.
Table : users
-------------

```SQL
USE maenmeta2dev

CREATE TABLE `users` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`username` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`name` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`email` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`password` VARCHAR(75) NOT NULL COLLATE 'latin1_swedish_ci',
	`avatar` VARCHAR(75) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`language` VARCHAR(30) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`aktif` TINYINT(4) NULL DEFAULT NULL,
	`created_at` DATETIME NULL DEFAULT utc_timestamp(),
	`updated_at` DATETIME NULL DEFAULT utc_timestamp(),
	PRIMARY KEY (`id`) USING BTREE,
	UNIQUE INDEX `username` (`username`) USING BTREE,
	UNIQUE INDEX `email` (`email`) USING BTREE,
	INDEX `name` (`name`) USING BTREE,
	INDEX `created_at` (`created_at`) USING BTREE,
	INDEX `updated_at` (`updated_at`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
ROW_FORMAT=COMPACT
AUTO_INCREMENT=1139
;
```
__Notes__

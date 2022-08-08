Table : users_query_share
-------------------------

```SQL
USE maenmeta2dev

CREATE TABLE `users_query_share` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`user_id` INT(11) NOT NULL,
	`query_id` INT(11) NOT NULL,
	`created_at` DATETIME NULL DEFAULT utc_timestamp(),
	PRIMARY KEY (`id`) USING BTREE,
	INDEX `user_id` (`user_id`) USING BTREE,
	INDEX `query_id` (`query_id`) USING BTREE,
	INDEX `created_at` (`created_at`) USING BTREE
)
COLLATE='utf8_general_ci'
ENGINE=InnoDB
AUTO_INCREMENT=151
;
```
__Notes__

+ __Table: users_query_share__ Give an information of a query or a request for data or information from a database table or combination of tables that have been asking by users. This data may be generated as results returned by Structured Query Language (SQL) for trend analyses from data-mining tools.
  
+ __id__ (Primary Key, Integer, Auto Increment).
  
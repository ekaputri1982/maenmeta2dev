Table : groups_member
---------------------

```SQL
USE maenmeta2dev

CREATE TABLE `groups_member` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`group_id` INT(11) NOT NULL,
	`user_id` INT(11) NOT NULL,
	`role` ENUM('ADMIN','MEMBER') NOT NULL COLLATE 'utf8_general_ci',
	PRIMARY KEY (`id`) USING BTREE,
	INDEX `user_id` (`user_id`) USING BTREE,
	INDEX `group_id` (`group_id`, `user_id`, `role`) USING BTREE,
	CONSTRAINT `groups_member_ibfk_1` FOREIGN KEY (`group_id`) REFERENCES `groups` (`id`) ON UPDATE RESTRICT ON DELETE RESTRICT,
	CONSTRAINT `groups_member_ibfk_2` FOREIGN KEY (`user_id`) REFERENCES `users` (`id`) ON UPDATE RESTRICT ON DELETE RESTRICT
)
COLLATE='utf8_general_ci'
ENGINE=InnoDB
;
```
__Notes__

+ __id__ (Primary Key, Integer, Auto Increment).
  
+ __Group_id, user_id, role__ Index Key.
  
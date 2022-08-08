Table : srcims_tags
-------------------

```SQL
USE maenmeta2dev

CREATE TABLE `srcims_tags` (
	`id` INT(11) UNSIGNED NOT NULL AUTO_INCREMENT,
	`srcims_id` INT(11) UNSIGNED NOT NULL,
	`tag_id` INT(11) UNSIGNED NOT NULL,
	PRIMARY KEY (`id`) USING BTREE,
	UNIQUE INDEX `srcims_id_tag_id` (`srcims_id`, `tag_id`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=263
;
```
__Notes__

+ __id__ (Primary Key, Integer, Auto Increment).

+ __scrims_id, tag_id__ Unique Key.
Table : srcemail_subject
------------------------

```SQL
USE maenmeta2dev

CREATE TABLE `srcemail_subject` (
	`id` INT(11) UNSIGNED NOT NULL AUTO_INCREMENT,
	`srcemail_id` INT(11) UNSIGNED NOT NULL,
	`subject_id` INT(11) UNSIGNED NOT NULL,
	PRIMARY KEY (`id`) USING BTREE,
	UNIQUE INDEX `srcemail_subject_id` (`srcemail_id`, `subject_id`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=6027
;
```
__Notes__

+ __Table: srcemail_subject__ This table is used for many to many relationship. 

+ __srcemail_id, subject_id__ Unique Key.


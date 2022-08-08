Table : tags
------------

```SQL
USE maenmeta2dev

CREATE TABLE `tags` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`tagname` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`descriptions` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`status` TINYINT(4) NOT NULL DEFAULT '1',
	PRIMARY KEY (`id`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=34
;
```
__Notes__

+ __Table: tags__ Mentioned an information that describes the data or content that it is assigned to. Tags are nonhierarchical keywords used for Internet bookmarks, digital images, videos, files and so on. A tag doesn't carry any information or semantics itself.
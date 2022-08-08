Table : grouping
----------------

```SQL
USE maenmeta2dev

CREATE TABLE `grouping` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`name` VARCHAR(128) NOT NULL COLLATE 'latin1_swedish_ci',
	`mt4server` VARCHAR(12) NOT NULL DEFAULT '' COLLATE 'latin1_swedish_ci',
	`creator` INT(11) NOT NULL DEFAULT '0',
	`owner` INT(11) NOT NULL DEFAULT '0',
	`mkt_id` INT(11) NULL DEFAULT NULL,
	`del` INT(11) NOT NULL DEFAULT '0',
	PRIMARY KEY (`id`) USING BTREE,
	INDEX `name` (`name`) USING BTREE,
	INDEX `mt4server` (`mt4server`) USING BTREE,
	INDEX `owner` (`owner`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=11742
;
```
__Notes__

+ __Table: Grouping__ Provide information of all grouping_share that created by the creator.
  

  
+ __Table: Grouping__ tabel ini berisi listing group yang akan menerima email untuk campaign yang dipilih oleh owner.
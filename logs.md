Table : logs
------------

```SQL
USE maenmeta2dev

CREATE TABLE `logs` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`userid` INT(11) NOT NULL,
	`action_type` VARCHAR(50) NULL DEFAULT '' COLLATE 'latin1_swedish_ci',
	`target` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`log` TEXT NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`dt` DATETIME NOT NULL,
	PRIMARY KEY (`id`) USING BTREE,
	INDEX `logs_userid` (`userid`) USING BTREE,
	INDEX `logs_action_type` (`action_type`) USING BTREE,
	INDEX `logs_dt` (`dt`) USING BTREE,
	INDEX `logs_target` (`target`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=125
;
```
__Notes__

+ __dt__ Date time is storing for every log of data logging. That is used to the process of collecting and storing data over a period of time in order to analyze specific trends or record the data-based events/actions of a system. It enables the tracking of all interactions through which data, files or applications are stored, accessed or modified on a storage device or application.
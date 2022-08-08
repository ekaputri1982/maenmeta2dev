Table : crm_logs_details
------------------------

```SQL
USE maenmeta2dev

CREATE TABLE `crm_logs_details` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`desc` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`desc_pas` VARCHAR(50) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	PRIMARY KEY (`id`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=65
;
```
__Notes__

+ __table: crm_logs_details__ Contain of data logging in specified of CRM (customer relationship management). It contains of the process of collecting and storing data over a period of time in order to analyze specific trends or record the database events/actions of a system management network. It enables the tracking of all interactions through which data, files or applications are stored, accessed or modified on a storage device or application.

+ __id__ (Primary Key, Integer, Auto Increment).
  





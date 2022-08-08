Table : crm_logs
----------------

```SQL
USE maenmeta2dev

CREATE TABLE `crm_logs` (
	`id` BIGINT(20) NOT NULL AUTO_INCREMENT,
	`event` BIGINT(20) NOT NULL,
	`source_id` BIGINT(20) NOT NULL COMMENT 'subject',
	`details` INT(11) NOT NULL COMMENT 'action',
	`action_id` VARCHAR(30) NULL DEFAULT NULL COMMENT 'object' COLLATE 'latin1_swedish_ci',
	`target_id` BIGINT(20) NULL DEFAULT NULL COMMENT 'target',
	`unread` TINYINT(1) NOT NULL DEFAULT '0' COMMENT '0=unread; 1=read',
	PRIMARY KEY (`id`) USING BTREE,
	INDEX `details` (`details`) USING BTREE,
	INDEX `target_id` (`target_id`) USING BTREE,
	INDEX `source_id` (`source_id`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=294708
;
```
__Notes__

+ __Table: crm_logs__ Contain of data logging in specified of CRM (customer relationship management). It contains of the process of collecting and storing data over a period of time in order to analyze specific trends or record the database events/actions of a system management network.
  
+ __id__ (Primary Key, Integer, Auto Increment).
  
+ __event__ an event log is a basic resource that helps provide information about network traffic, usage and other conditions. An event log stores these data for retrieval by security professionals or automated security systems to help CRM (Customer Relationship Management) to manage various aspects such as security, performance, transparency and date time.
Table : crm_timelines
---------------------

```SQL
USE maenmeta2dev

CREATE TABLE `crm_timelines` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`event` VARCHAR(50) NOT NULL COLLATE 'utf8_general_ci',
	`query` MEDIUMTEXT NOT NULL DEFAULT '' COLLATE 'utf8_general_ci',
	`icon` MEDIUMTEXT NOT NULL DEFAULT '' COLLATE 'utf8_general_ci',
	`template` MEDIUMTEXT NOT NULL DEFAULT '' COLLATE 'utf8_general_ci',
	PRIMARY KEY (`id`) USING BTREE
)
COLLATE='utf8_general_ci'
ENGINE=InnoDB
AUTO_INCREMENT=8
;
```
__Notes__

+ __Table: crm_timelines__ Deliver an information chronological arrangement of events in the order of their occurrence on the environment of CRM (Customer Relationship Management). 
  
+ __id__ (Primary Key, Integer, Auto Increment).

+ __crm_timelines__ tabel yang berisi data alur waktu terjadi event pada customer relation management.
  
+ __query__ query column is a request for data or information from a database table or combination of tables. This data may be generated as results returned by Structured Query Language (SQL) or as pictorials, graphs or complex results when a process or procedure will be carried out.

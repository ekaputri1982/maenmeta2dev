Table : customer_tags
---------------------

```SQL
USE maenmeta2dev

CREATE TABLE `customer_tags` (
	`id` INT(11) UNSIGNED NOT NULL AUTO_INCREMENT,
	`crm_id` INT(11) UNSIGNED NOT NULL,
	`tag_id` INT(11) UNSIGNED NOT NULL,
	PRIMARY KEY (`id`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
;
```
__Notes__

+ __id__ (Primary Key, Integer, Auto Increment). 
  
+ __crm_id__ Identification for CRM (Customer Relationship Management).
  
+ __tag_id__ A piece of information that describes the data or content that it is assigned to. Tags are nonhierarchical keywords used for Internet bookmarks, digital images, videos, files and so on. A tag doesn't carry any information or semantics itself Tagging serves many functions, including: classification, marking ownership, describing content type, and online identity.
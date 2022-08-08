Table : customer_dtl_tags
-------------------------

```SQL
USE maenmeta2dev

CREATE TABLE `customer_dtl_tags` (
	`id` INT(11) UNSIGNED NOT NULL AUTO_INCREMENT,
	`detail_id` INT(11) UNSIGNED NOT NULL,
	`tag_id` INT(11) UNSIGNED NOT NULL,
	PRIMARY KEY (`id`) USING BTREE,
	UNIQUE INDEX `customer_dtl_tag_id` (`detail_id`, `tag_id`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=3368
;
```
__Notes__

+ __Table: customer_dtl_tags__ Customer relationship management includes the principles, practices, and guidelines, and refers also to help manage external interactions with customers. It contains a tag of an information that describes the data or content that it is assigned to. Tags are nonhierarchical keywords used for Internet bookmarks, digital images, videos, files and so on.
  
+ __id__ (Primary Key, Integer, Auto Increment).

+ __tag_id__ status of tag_id could be switched depend on the list.
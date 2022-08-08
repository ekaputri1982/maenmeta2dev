Table : srclivechat_subject
---------------------------

```SQL
USE maenmeta2dev

CREATE TABLE `srclivechat_subject` (
	`id` INT(11) UNSIGNED NOT NULL AUTO_INCREMENT,
	`srclivechat_id` INT(11) UNSIGNED NOT NULL,
	`subject_id` INT(11) UNSIGNED NOT NULL,
	PRIMARY KEY (`id`) USING BTREE,
	UNIQUE INDEX `srclivechat_subject_id` (`srclivechat_id`, `subject_id`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=30654
;
```
__Notes__

+ __Table: srclivechat_subject__ Subject string that deliver an information of live chat support that is a Web service for businesses that allows visitors to communicate with the business, usually through real-time live chat. Live support is designed to provide customers and clients with immediate support and information. The Web service is integrated with the business website and generally includes invisible website traffic analysis and secure administrative controls.
  
+ __id__ (Primary Key, Integer, Auto Increment).
  
+ __srclivechat_id, subject_id__ Unique Key.
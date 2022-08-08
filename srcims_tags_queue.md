Table : srcims_tags_queue
-------------------------

```SQL
USE maenmeta2dev

CREATE TABLE `srcims_tags_queue` (
	`id` INT(11) UNSIGNED NOT NULL AUTO_INCREMENT,
	`ims_id` INT(11) NOT NULL,
	`source` INT(11) NOT NULL,
	`tag` INT(11) NOT NULL,
	`modify_at` TIMESTAMP NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
	PRIMARY KEY (`id`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=2
;
```
__Notes__

+ __Table: srcims_tags_queue__ Information tag queue of Source (scr) and Investment Management System (IMS).

+ __ims_id__ Contains identification of Investor Management System could be an address of website that often refers to managing the holdings within an investment portfolio, and the trading of them to achieve a specific investment objective. Investment management is also known as money management, portfolio management, or wealth management.
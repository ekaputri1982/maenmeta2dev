Table : brokers
---------------

```SQL
USE maenmeta2dev

CREATE TABLE `brokers` (
	`id` INT(11) NOT NULL AUTO_INCREMENT,
	`nickname` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`codename` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`realname` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`ims` VARCHAR(50) NOT NULL COLLATE 'latin1_swedish_ci',
	`parent_id` INT(11) NULL DEFAULT NULL,
	`icon` VARCHAR(75) NULL DEFAULT NULL COLLATE 'latin1_swedish_ci',
	`status` TINYINT(4) NOT NULL DEFAULT '1',
	PRIMARY KEY (`id`) USING BTREE,
	INDEX `parent_id` (`parent_id`) USING BTREE
)
COLLATE='latin1_swedish_ci'
ENGINE=InnoDB
AUTO_INCREMENT=8
;
```
__Notes__

+ __Table: brokers__ Contain forex broker data which is a financial services company that provides traders access to a platform for buying and selling foreign currencies. The transactions in the forex market are always between a pair of two different currencies. A forex broker may also known be as a retail forex broker or a currency trading broker.
  
+ __ims__ Investor Management System could be an address of website that often refers to managing the holdings within an investment portfolio, and the trading of them to achieve a specific investment objective. Investment management is also known as money management, portfolio management, or wealth management.

+ __status__ Approval status.
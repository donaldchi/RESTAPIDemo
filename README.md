#概略

このサンプルコードは、Node.jsとExpressを使って、mysqlとやりとりをし、その結果をjson形式で返すような簡単なREST apiです。

元の文章:

http://qiita.com/donaldchi/items/6cf83493b2a8efa402a5

データベース　スクリプト

```
create database Test;
use Test;
CREATE TABLE IF NOT EXISTS `users` (
  `id` INT(70) NOT NULL AUTO_INCREMENT,
  `email` VARCHAR(45) NOT NULL,
  `password` VARCHAR(45) NULL,
  `created_date` TIMESTAMP NULL DEFAULT CURRENT_TIMESTAMP,
  PRIMARY KEY (`id`),
  UNIQUE INDEX `email_UNIQUE` (`email` ASC))
ENGINE = InnoDB;
```

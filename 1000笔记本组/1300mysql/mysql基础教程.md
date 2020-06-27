| 商品编号 | 商品名称 | 商品分类 | 销售单价 | 进货单价 | 等级日期 |
| --- | --- | --- | --- | --- | --- |
| 0001 | T恤衫 | 衣服 | 1000 | 500 | 2009-09-20 |
| 0002 | 打孔器 | 办公用品 | 500 | 300 | 2009-09-11 |
#### 显示当前数据库
```
SHOW DATABASES
```

#### 增添数据库
```
CREATE DATABASE database_name
```
#### 删除数据库
```
DROP DATABASE database_name
```
#### 使用数据库
```
USE test_db
Database changed #数据库已更改
```
#### 建立表
```
create table 表名称
```
#### 显示数据库里面的所有的表
```
show tables
```
#### 显示某一个表的结构
```
desc T_student #显示名为T_student的表

显示一个表格创建时候的语句
```
mysql> SHOW CREATE TABLE TB1;
+-------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| Table | Create Table                                                                                                                                                                                                        |
+-------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| TB1   | CREATE TABLE `TB1` (
  `stu_id` varchar(100) DEFAULT NULL,
  `stu_name` varchar(20) DEFAULT NULL,
  `stu_phono` varchar(20) DEFAULT NULL,
  `stu_sex` varchar(50) DEFAULT NULL
) ENGINE=InnoDB DEFAULT CHARSET=utf8 |
+-------+---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+
1 row in set (0.00 sec)
```
desc语句不同,这两个语句意思为什么不同呢
```
desc table_name
```
desc table 这两个区别在哪table_name
```
```
#### 创建表
```
CREATE TABLE Shohin
(shohin_id CHAR(4) NOT NULL,
shohin_mei VARCHAR(100) NOT MULL,
shohin_burui VARCHAR(32) NOT NULL,)
;
```
#### 创建表的语句
```
CREATE TABLE <表名>
（<列名1> <数据类型> <该列所需约束>,
<列名2> <数据类型> <该列所需约束>，
<列名3> <数据类型> <该列所需约束>，
<列名4> <数据类型> <该列所需约束>）
;
```
#### 数据类型
- INTEGER
用来指定存储整数的列的数据类型（数字型），不能存储小数。
- CRAR
是用来指定存储字符串的列的数据类型（字符型）。可以向CHAR（10）或者CHAR（200）这样，在括号里指定【该列可以存储的字符串的长度，输入的字符串超过长度无法输入到该列中。即为定长字符。
- VARCHAR
同CHAR类型一样，也是用来之sk存储字符串的列的数据类型（字符串类型）。可变长字符串。
- DATE
用来指定存储日期（年月日）的列的数据类型（日期型）
```
#### 主键约束 
```
PRIMARY KEY （列名）
```
#### 更新表
```
ALTER TABLE <表名>  ADD COLUMN  <列名>  <数据类型>;
```
#### 插入数据
```
BEGIN TRANSACTION;
INSERT INTO <表名> VALUES (`0001`,`T恤衫`,`衣服`,1000,500,`2009-09-20);
INSERT INTO <表名> VALUES (`0002`,`打孔器`,`办公用品`,500,320,`2009-09-11`);
COMMIT;
```
```
CREATE TABLE TB1(
mai_id INT NOT NULL,
mai_name VARCHAR(100) NOT NULL,
mai_gs VARCHAR(100) NOT NULL,
mai_jg INT NOT NULL,
mai_ib INT NOT NULL,
mai_data DATE NOT NULL
PRIMARY KEY (mail_id));
```
#### 这个踩坑的问题
- VARCHAR 必须有数值
- DATA 是 DATE
- 设置关键词语的时候看清楚

```
BEGIN TRANSACTION
```
插入数据开头起始句
```
COMMIT
```
插入数据结束句
#### SELECT语句
```
SELECT <列名>,
FROM <表名>;
```

# MySql
## 数据类型
### int  4 
### float 4
### double 8双精度浮点
### enum 单选 eg: enum(‘a’, ‘b’, ‘c’)
### set 多选
### date 3 YYYY-MM-DD
### time 3 HH:MM:SS
### year 1 YYYY
### char 
### varchar 变长字符串
### text
## 常用操作
### 数据库操作
#### show databases;
#### drop database (database name);
#### create database (database name);
#### use (database name)
#### 备份
##### mysqldump -u root 数据库名>备份文件名
#### 恢复 
##### source ‘sql文件路径’
##### mysql -u root 新database名 < sql文件名
### 表操作
#### show tables;
#### insert into (table name)(列a, 列b, 列c) values(值1, 值2, 值3);
#### select * from (table name);
#### create table (table name) (name a   datatype(data length));
#### select 要查询的列名 from 表名 where 限制条件
##### where条件可有=,>,<,>=,<=,and,or,in,not in
##### 关键字like和通配符
###### _ 代表一个未指定字符
###### % 代表不定个未指定字符
##### order by 
###### 默认升序
###### asc 升序
###### desc 降序
##### 内置函数
###### count 计数
###### sum 求和
###### avg 求平均
###### max
###### min
##### as 重命名
##### 子查询
###### where 换成having
##### 连接查询join
##### group by
#### 重命名
##### rename table 原名 to 新名；
##### alter table 原名 rename 新名；
##### alter table 原名 rename to 新名；
#### drop table 表名；
#### 增加一列
##### alter table 表名 add column 列名字 数据类型 约束；
##### alter table 表名 add 列名 数据类型 约束 after 列名（或者 first）；
#### 删除一列
##### alter table 表名 drop （column ）列名字 ；
#### 重命名一列 
##### alter table 表名字 change 原列名 新列名 数据类型 约束；（数据类型不能省）
#### 改变数据类型
##### alter table 表名 modify 列名 新数据类型；（谨慎使用）
#### 修改表中某个值
##### update 表名 set 列1=值1，列2=值2 where 条件；
#### 删除一行记录 
##### delete from 表名 where 条件；
#### 建立索引
##### alter table 表名 add index 索引名 （列名）；
##### create index 索引名 on 表名 （列名）；
#### 创建视图
##### create 视图名（列a，列b，列c）as select 列1，列2，列3 from 表名；
#### 导入
##### load data infile ‘文件路径和文件名’ into table 表名字；
#### 导出
##### select 列1，列2 into outfile ‘文件路径和名称’ from 表名；
#### 备份
##### mysqldump -u root 数据库名 表名>备份文件名
## 约束类型
### 主键
#### Primary key
### 默认值
#### Default
### 唯一
#### Unique
### 外键(一个表可有多个外键）
#### Foreign key
### 非空
#### Not null

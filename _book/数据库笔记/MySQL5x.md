# MySQL5.x 数据库

### 用户管理

1. 用户授权：使用`grant all privileges on 数据库名.表名 to '用户名'@'地址' identified by '密码';`来设置用户的访问权限。

    * eg1:`grant all privileges on *.* to 'root'@'%' identified by '000000'`设置root用户可以使用`000000`密码__远程__登陆

    * eg2:`grant all privileges on *.* to 'root'@'localhost' identified by '000000'`设置root用户可以使用`000000`密码__本地__登陆

2. 刷新权限:使用`flush privileges;`刷新数据库权限，使得设置生效。

### 字符设置



### 数据库(database)操作

1.创建数据库

&emsp;&emsp;使用`create database 数据库名`创建数据库  
&emsp;&emsp;使用`show databases;`显示所有数据库

### 表(table)操作

### 查询(select)操作


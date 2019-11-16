# MySQL5.x 数据库

### 一、用户管理

1. 用户授权

	* 使用`grant all privileges on 数据库名.表名 to '用户名'@'地址' identified by '密码'`来设置用户的访问权限。

>例子:
>1. `grant all privileges on *.* to 'root'@'%' identified by '000000'`设置root用户可以使用`000000`密码`远程`登陆`所有`数据库的`所有`表
>
>2. `grant all privileges on *.* to 'root'@'localhost' identified by '000000'`设置root用户可以使用`000000`密码`本地`登陆`所有`数据库的`所有`表

2. 刷新权限

	* 使用`flush privileges`刷新数据库权限，使得设置生效。

### 二、字符设置

1. 更新中...

### 三、数据库(database)操作

1. 创建数据库

	* 使用`create database 数据库名`创建数据库

>例子：
>1. `create database Test`创建Test数据库

2. 查看数据库

	* 使用`show databases;`显示所有数据库

### 四、表(table)操作

1. 更新中...

### 五、查询(select)操作

1. 更新中...

### 六、插入(insert)操作

1. 更新中...

# MySQL5.x 数据库

### 一、用户管理

#### 用户授权

设置用户的访问权限

```
grant all privileges on 数据库名.表名 to '用户名'@'地址' identified by '密码';
```

>例子:
>1. 设置root用户可以使用`000000`密码`远程`登陆`所有`数据库的`所有`表  
>	grant all privileges on \*.\* to 'root'@'%' identified by '000000';	
>
>2. 设置root用户可以使用`000000`密码`本地`登陆`所有`数据库的`所有`表  
>	grant all privileges on *.* to 'root'@'localhost' identified by '000000';  
  
#### 刷新权限

刷新数据库权限，使得设置生效

```
flush privileges;
```

### 二、字符集设置

#### 查看字符集

查看 MySQL 数据库服务器和数据库字符集

```
show variables like '%character%';
```  

查看 MySQL 所支持的字符集

```
show charset;
```  

查看创建数据库的字符集

```
show create database from 库名;
```  

#### 修改字符集

使用`alter`修改数据库字符集

```
alter database 数据库名 character set utf8;
```

ps: 修改完之后需要重启数据库才能生效

使用`alter`修改表的字符集

```
alter table 表名 default character set utf8 collate utf8_general_ci;
```

#### 配置文件中修改字符集

在 my.ini(windows)/my.cnf(Linux) 配置文件中修改

```
character_set_server = utf8
```

PS: 配置完需重启服务器

### 三、数据库(database)操作

#### 创建数据库

创建数据库  

```
create database 数据库名;
```

>例子：
>1. 创建Test数据库  
>	create database Test; 

创建数据库的时候指定字符集

```
create database if not exists 库名 default character set='utf8';
```

ps: 通过`default character set`来指定数据库的字符集
  
#### 查看数据库

显示所有数据库

```
show databases;
```

### 四、表(table)操作

&emsp;&emsp;更新中...

### 五、查询(select)操作

&emsp;&emsp;更新中...

### 六、插入(insert)操作

&emsp;&emsp;更新中...

# MySQL5.x 数据库

### 一、用户管理

#### 用户授权

设置用户的访问权限

```
	grant all privileges on 数据库名.表名 to '用户名'@'地址' identified by '密码';
```

>例子:
>1. 设置root用户可以使用`000000`密码`远程`登陆`所有`数据库的`所有`表  
>	grant all privileges on *.* to 'root'@'%' identified by '000000';	
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

查看数据库的字符集

```
	show create database from 库名;
```  

#### 修改字符集

修改 my.ini 配置文件


### 三、数据库(database)操作

#### 创建数据库

创建数据库  

```
create database 数据库名;
```

>例子：
>1. 创建Test数据库  
>	create database Test; 
  
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

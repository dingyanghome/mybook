# MySQL8.x 数据库

### 密码配置

在 `MySQL 8.0` 版本中，密码插件验证方式发生了变化，早期版本为 `mysql_native_password`，而 8.0 版本为 `caching_sha2_password`

需要修改 my.ini/my.cnf 配置：

```
[mysqld]
default_authentication_plugin=mysql_native_password
```

ps：修改完成后需重启服务器

然后在 mysql 下执行以下命令来修改密码：

```
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '新密码';

flush privileges;
```
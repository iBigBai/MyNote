### 调整MySQL数据连接数
#### 查询MySQL数据连接数
1. 查询mysql的最大连接数
```mysql
show variables like '%max_connections%';
```
2. 查询当前状态连接数
```mysql
show global status like 'Max_used_connections';
```
#### 修改MySQL数据连接数
1. 找到`mysqld`的路径
`which mysqld`
2. 查询`my.cnf`路径
`/usr/local/mysql/bin/mysqld --verbose --help |grep -A 1 'Default options'`
3. 修改mysql配置文件`my.cnf`
`max_connections=512`
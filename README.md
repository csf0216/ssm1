#优雅的SSM架构(Spring+SpringMVC+Mybatis）
- Maven
- Spring（IOC DI AOP 声明式事务处理）
- SpringMVC（支持Restful风格）
- Hibernate Validate（参数校验）
- Mybatis（最少配置方案）
- Quartz时间调度
- Redis缓存（ProtoStuff序列化）
- [Redis Sentinel主从高可用方案](http://wosyingjun.iteye.com/blog/2289593)
- [Redis Cluster集群高可用方案](http://wosyingjun.iteye.com/blog/2289220)
- [Druid（数据源配置 sql防注入 sql性能监控)](http://wosyingjun.iteye.com/blog/2306139)
- 统一的异常处理
- JSP JSTL JavaScript
- Sping Shiro权限控制（待完善）

###**架构图：**
![](http://i.imgur.com/vc6iu0X.png)

###1、配置redis
- vi ../redis.conf
- requirepass csf119078
- ./redis-server ../redis.conf

###2、修改redis.properties
- redis.ip=127.0.0.1
- redis.pass=*******

### 3、配置mysql
- source /home/wangmin/work/java/beauty_ssm/src/main/resources/sql/schema.sql
- source /home/wangmin/work/java/beauty_ssm/src/main/resources/sql/execute_bug.sql

### 4.访问http://localhost:8080/beauty/goods/list

### 5.mysql 5.6.4之前不支持2列current_timestamp

### 6.升级mysql
- sudo apt-get autoremove mysql-server
- wget https://dev.mysql.com/get/mysql-apt-config_0.8.1-1_all.deb
- sudo dpkg -i mysql-apt-config_0.8.1-1_all.deb
- sudo apt-get update
- sudo apt-get install mysql-server

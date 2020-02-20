---
title: SpringBoot中的application.properties常用配置
date: 2020-02-20 20:00:08
categories:
- java
tags:
- SpringBoot
---



### 基本示例

```properties
#应用名称
spring.application.name=apply
#端口号
server.port=8888
#多环境配置，测试，生产用不同的配置文件
spring.profiles.active=test
#session超时，单位秒
server.session.timeout=30
```

### 数据库配置

```properties
spring.datasource.app.url=jdbc:oracle:thin:@//172.20.2.44:1521/testdb
spring.datasource.app.username=test
spring.datasource.app.password=test123
spring.datasource.app.driver-class-name=oracle.jdbc.driver.OracleDriver
spring.datasource.app.type=com.alibaba.druid.pool.DruidDataSource
spring.datasource.app.minIdle=5
spring.datasource.app.maxActive=400
spring.datasource.app.initialSize=10
spring.datasource.app.maxWait=60000
spring.datasource.app.timeBetweenEvictionRunsMillis=60000
spring.datasource.app.minEvictableIdleTimeMillis=300000
spring.datasource.app.validationQuery=SELECT 1 FROM DUAL
spring.datasource.app.testWhileIdle=true
spring.datasource.app.testOnBorrow=false
spring.datasource.app.testOnReturn=false
spring.datasource.app.poolPreparedStatements=true
spring.datasource.app.maxPoolPreparedStatementPerConnectionSize=50
spring.datasource.app.removeAbandoned=true
spring.datasource.app.filters=stat 
```

### redis配置

```properties
spring.redis.host=172.30.2.134
spring.redis.port=6379
spring.redis.timeOut=5000
spring.redis.maxIdle=50
spring.redis.maxWaitMillis=5000
spring.redis.maxActive=300
```

### mybatis配置

```properties
#mybatis
mybatis.mapperLocations=classpath:mapper/*.xml
#mybatis.type-aliases-package=com.mundo.test.pojo
mybatis.configLocation=classpath:mybatis/mybatis-config.xml
```

### mvc配置

```properties
#设定mvc视图的前缀.
spring.view.prefix=/WEB-INF/jsp/.....
#设定mvc视图的后缀.
spring.view.suffix=.html
```

### 日志配置

````properties
#设置文件，可以是绝对路径，也可以是相对路径。
logging.file=my.log
#设置目录，会在该目录下创建spring.log文件，并写入日志内容
logging.path=/var/log
#如果只配置 logging.file，会在项目的当前路径下生成一个 xxx.log 日志文件。
#如果只配置 logging.path，在 /var/log文件夹生成一个日志文件为 spring.log
#日志级别LEVEL=TRACE, DEBUG, INFO, WARN, ERROR, FATAL, OFF
logging.level.* = LEVEL
````


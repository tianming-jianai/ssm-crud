# 尚硅谷SSM整合视频



##### 功能点：

1、分页

2、数据校验

​	JQuery前端校验+JSR303后端校验

3、ajax

4、Rest风格的URI；使用HTTP协议请求方式的动词，来标识对资源的操作GET(查询)，POST(新增),PUT(修改),DELETE(删除)

##### 技术点：

基础框架-ssm(SpringMVC+Spring+MyBatis)

数据库-MySQL

前端框架-bootstrap快速搭建简洁美观的界面

项目的依赖管理-Maven

分页-pagehelper(插件)

逆向工程-Mybatis Generator

<hr>

##### 基础环境搭建：

###### 1、创建一个maven工程

​	配置maven的settings.xml文件

mirror

```xml
<mirror>
		<id>alimaven</id>
		<name>aliyun maven</name>
		<url>http://maven.aliyun.com/nexus/content/groups/public/<url>
		<mirror>central</mirror>
	 </mirror>
```

profile

```xml
<profile>    
		<id>jdk-1.8</id>    
		<activation>    
			<activeByDefault>true</activeByDefault>    
			<jdk>1.8</jdk>    
		</activation>    
		<properties>    
			<maven.compiler.source>1.8</maven.compiler.source>    
			<maven.compiler.target>1.8</maven.compiler.target>    
			<maven.compiler.compilerVersion>1.8</maven.compiler.compilerVersion>    
		</properties>    
	</profile>
```

###### 2、引入项目依赖的jar包

spring、springmvc、mybatis、数据库连接池，驱动包、其他(jstl,servlet-api,junit)

[mave仓库]: https://mvnrepository.com/

```xml
Spring 4.3.7.RELEASE
<!-- SpringMVC,Spring -->
spring-webmvc
<!-- Spring-Jdbc事务控制 -->
spring-jdbc
<!-- Spring面向切面编程，基于配置的事务控制 -->
spring-aspects
```

```xml
MyBatis
<!-- mybatis -->
mybatis 3.4.2
<!-- MyBatis整合Springde的适配包 -->
mybatis-spring 1.3.1
```

```xml
<!-- 数据库连接池、驱动 -->
c3p0 0.9.2
mysql-connector-java 5.1.41
```

```xml
其他：
<!-- jstl/servlet-api/junit -->
jstl 1.2
servlet-api 2.5	<scope>provided</scope>
junit 4.12
```


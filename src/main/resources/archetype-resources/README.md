##README
This repository is a skeleton of java web project organized by Rugal Bernstein.  
Integreted Spring-webmvc, Spring-framework and mybatis, so I will call it as SSM for short.  
This skeleton use HikariCP as data source.  
Deployment descriptor version is already 3.0, so it could support most of new features on Oracle JVM.  
All maven dependencies are reduced to simplest form, no need of worrying about the dependency redundancy.  
Use Tomcat as embedded Servlet container configured in `pom.xml`.   
Use spring-framework's jdbc `DataSourceTransactionManager` as Transaction Manage, with some default transaction advices given.  
Use slf4j as log adapter and logger in Log4j. You can change it as you want.  
This project's controller return JSON as default response body, customize it in springmvc configuration file if you need to change.  
Provided base test file and template test file from both server side integretion test and unit test.  


1. JDBC properties  already rather generic
2. applicationContext  defines mybatis and data source properties. You NEED to do some change in this file as some package scan bean need directed.   
3. springmvc  Just one place needs change: `base-package` of component-scan tag
4. log4j  is rather generic
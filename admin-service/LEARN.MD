# Spring Boot Microservices Spring Admin Server

## Setup Admin Server

- [一篇带你了解Spring Boot Admin，贼好使！](https://www.51cto.com/article/699076.html)
- [使用spring-boot-admin报错failed to resolve ‘DESKTOP-DHHU94O‘ after 2 queries](https://blog.csdn.net/qq_38279833/article/details/119325864)
- [win10-以管理员身份打开hosts文件并编辑保存](https://www.cnblogs.com/eosclover/p/16111898.html)

In Admin Server Module

### Step.1 Install Server Dependency

```xml
<dependency> 
   <groupId>org.springframework.boot</groupId> 
   <artifactId>spring-boot-starter-web</artifactId> 
</dependency> 
<dependency> 
  <groupId>de.codecentric</groupId> 
  <artifactId>spring-boot-admin-starter-server</artifactId>
  <version>2.5.4</version>
</dependency> 
```

### Step.2 Register Admin Server Service in Application 

```java
package com.nils.microservices.adminservice;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@EnableAdminServer
@SpringBootApplication
public class AdminServiceApplication {

    public static void main(String[] args) {
        SpringApplication.run(AdminServiceApplication.class, args);
    }

}
```

### Step.3 Config Server Service Port
In application.properties

```properties
server.port=9001 
```

## Setup Admin Client

### Step.1 Install Client Dependency

```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-starter-web</artifactId>
</dependency>
<dependency>
    <groupId>de.codecentric</groupId>
    <artifactId>spring-boot-admin-starter-client</artifactId>
    <version>2.5.3</version>
</dependency>
```

### Step.2 
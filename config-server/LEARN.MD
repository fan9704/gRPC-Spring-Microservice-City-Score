# Spring Boot Config Server Learn Note

Base on Spring Cloud

---

- [Spring Cloud Config](https://docs.spring.io/spring-cloud-config/docs/current/reference/html/)
- [Building a Microservice with Spring Boot Config Server: A Step-by-Step Guide with Code Explanation.](https://medium.com/@erayaraz10/building-a-microservice-with-spring-boot-config-server-a-step-by-step-guide-with-code-explanation-769d548cd71d)
- [Day 15 - 組態控制中心 Config Server](https://ithelp.ithome.com.tw/articles/10192773)

## Config Server

### Step.1 Install Dependencies

Describe Spring Cloud Version in properties

```xml
<properties>
    <java.version>16</java.version>
    <maven.compiler.source>16</maven.compiler.source>
    <maven.compiler.target>16</maven.compiler.target>
    <spring-cloud.version>2020.0.3</spring-cloud.version>
</properties>
```

Add Spring Cloud Dependencies Management

```xml
    <dependencyManagement>
        <dependencies>
            <dependency>
                <groupId>org.springframework.cloud</groupId>
                <artifactId>spring-cloud-dependencies</artifactId>
                <version>${spring-cloud.version}</version>
                <type>pom</type>
                <scope>import</scope>
            </dependency>
        </dependencies>
    </dependencyManagement>
```

Install Spring Cloud and Config Server

```xml
<dependencies>
    <!--Config Server-->
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.cloud</groupId>
        <artifactId>spring-cloud-config-server</artifactId>
    </dependency>
    <!--Config Server-->
</dependencies>
```

### Step.2 Config Server Config Resource

Describe Config Server Port and Resource in application.properties

```properties
server.port=9010
spring.cloud.config.server.git.uri= file://${user.home}/spring-config-repo
```

## Config Client

### Step.1 Same as Config Server

### Step.2 Same As Config Server

### Step.3 Config Server Config 


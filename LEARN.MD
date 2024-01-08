# Spring Boot Microservices gRPC Project Learning Note

---

## Microservices

### Generate Service Unit in Parent Project

Step.1 Right Click Parent Project in IDEA

![](/doc/CreateNewSpringBootModule-Open.png)

Step.2 Describe Service Unit
![](/doc/CreateNewSpringBootModule.png)

Or user Maven Command Generate Service Unit

```shell 
mvn archetype:generate -DgroupId=[GROUP ID]-DartifactId=[PARNET PROJECT NAME] -DarchetypeArtifactId=[MODULE PROJECT NAME]
```

### Application.properties vs Bootstrap.properties

- [Spring Configuration Bootstrap vs Application Properties](https://www.baeldung.com/spring-cloud-bootstrap-properties)

---

## Spring Boot Admin

[Spring Boot Admin Learning Note](/admin-service/LEARN.MD)
# Lesson 9: Unit Testing for Java Context

## Overview

Instead of using the `springboot-starter-test` dependency, we'll learn how to write a unit test using the Spring test features in this lesson.

## Demonstrated Concepts

### `spring-test` and `junit` dependency

We start by replacing the `springboot-starter-test` dependency — which is automatically included in a Spring Boot project — with the `spring-test` dependency along with the `junit-jupiter-engine` dependency.

```xml
<dependency>
    <groupId>org.springframework</groupId>
    <artifactId>spring-test</artifactId>
    <scope>test</scope>
</dependency>
```
```xml
<dependency>
    <groupId>org.junit.jupiter</groupId>
    <artifactId>junit-jupiter-engine</artifactId>
    <scope>test</scope>
</dependency>
```

Since the project was built using Spring Boot, removing the `springboot-starter-test` dependency leads to __compilation errors__ due to usage of the `@SpringBootTest` annotation in __src/test/java__. To remove the errors, we can comment out the `@SpringBootTest` annotation.



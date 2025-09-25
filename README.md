# 📌 Spring Boot AutoConfig Demo

This project demonstrates how Spring Boot AutoConfiguration works, allowing configurations to be applied automatically and overridden with custom properties.

## 🎯 Objectives

- Demonstrate the use of AutoConfiguration in Spring Boot.
- Create conditional beans with @ConditionalOnProperty.
- Show how to override default settings in application.properties.

## 🏗️ Project Structure

```plaintext
spring-boot-autoconfig-demo
 ├── build.gradle.kts
 ├── settings.gradle.kts
 └── src
     ├── main
     │   ├── java/com/example/autoconfigdemo
     │   │   ├── AutoconfigDemoApplication.java
     │   │   ├── controller/GreetingController.java
     │   │   └── config/CustomAutoConfig.java
     │   └── resources/application.properties
     └── test/java/com/example/autoconfigdemo/AutoconfigDemoApplicationTests.java

```

## 🚀 Running the Project

```bash

./gradlew bootRun

```

## 📊 Flowchart – AutoConfiguration Flow

```mermaid
flowchart TD
    A[Start Application] --> B[Spring Boot AutoConfiguration]
    B --> C{application.properties}
    C -->|feature.custom.enabled=true| D[Load Custom Bean]
    C -->|feature.custom.enabled=false| E[Skip Custom Bean]
    D --> F[Application Running on Port 8082]
    E --> F
```

---

**Kleber Vales**  

*Back-end Software Developer*  








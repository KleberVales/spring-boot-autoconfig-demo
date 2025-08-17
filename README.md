# 📌 Spring Boot AutoConfig Demo

Este projeto demonstra como o Spring Boot AutoConfiguration funciona, permitindo que configurações sejam aplicadas automaticamente e sobrescritas com propriedades customizadas.

## 🎯 Objetivos

- Demonstrar o uso de AutoConfiguration no Spring Boot.
- Criar beans condicionais com @ConditionalOnProperty.
- Mostrar como sobrescrever configurações padrão no application.properties.

## 🏗️ Estrutura do Projeto

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

## 🚀 Executando o Projeto

```bash

./gradlew bootRun

```

## 📊 Fluxograma – AutoConfiguration Flow

```mermaid
flowchart TD
    A[Start Application] --> B[Spring Boot AutoConfiguration]
    B --> C{application.properties}
    C -->|feature.custom.enabled=true| D[Load Custom Bean]
    C -->|feature.custom.enabled=false| E[Skip Custom Bean]
    D --> F[Application Running on Port 8082]
    E --> F
```




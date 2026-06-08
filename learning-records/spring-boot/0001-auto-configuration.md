# 0001 — Spring Boot Auto-Configuration

**Date:** 2026-06-08
**Lesson:** 0001-spring-boot-auto-configuration.html

## What Was Taught

- @SpringBootApplication is shorthand for @SpringBootConfiguration + @EnableAutoConfiguration + @ComponentScan
- Auto-configurations are listed in META-INF/spring/...AutoConfiguration.imports inside starter JARs
- @ConditionalOnClass, @ConditionalOnMissingBean etc. control when each auto-config applies
- Spring Boot backs off automatically when the user defines their own bean
- LabelRadar context: DataSourceAutoConfiguration + HibernateJpaAutoConfiguration activate from pom.xml deps + application.properties

## Key Insight

The entire auto-config system is just: "scan a list of config classes, apply each one only if conditions pass". No real magic.

## Status

Lesson delivered. Quiz not yet attempted by learner.

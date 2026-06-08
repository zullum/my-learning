# 0002 — Spring Data JPA & JpaRepository

**Date:** 2026-06-08
**Lesson:** 0002-spring-data-jpa-repository.html

## What Was Taught

- JpaRepository inherits from CrudRepository + PagingAndSortingRepository — ~18 methods for free
- Spring Data generates SimpleJpaRepository implementation at startup via proxy
- EntityManager is the bridge: object operations → Hibernate → SQL → MySQL 5.7
- Derived query methods: Spring parses method names like findByNameAndActiveTrue into SQL
- @Query for complex cases — JPQL (entity names) vs nativeQuery (table names)
- ddl-auto: never use update/create in production — use validate + Flyway

## Key Insight

You write an interface, Spring writes the class. The method name IS the query.

## Status

Lesson delivered. Quiz included (4 questions).

# 0003 — @Transactional

**Date:** 2026-06-08
**Lesson:** lessons/spring-boot/0003-transactional.html

## What Was Taught

- @Transactional wraps method in AOP proxy: BEGIN → run → COMMIT or ROLLBACK
- Only RuntimeException triggers rollback by default — checked exceptions commit!
- Fix: rollbackFor = Exception.class for checked exceptions
- Self-invocation gotcha: calling @Transactional method from same class bypasses proxy
- @Transactional(readOnly=true) skips Hibernate dirty-checking — use on all read methods
- Best pattern: class-level readOnly=true, override with @Transactional on write methods
- MySQL 5.7: transactions only work on InnoDB tables — verify with SHOW TABLE STATUS

## Key Insight

@Transactional is a proxy — anything that bypasses the proxy (self-invocation, non-public methods) silently has no effect.

## Status

Lesson delivered. Quiz included (4 questions).

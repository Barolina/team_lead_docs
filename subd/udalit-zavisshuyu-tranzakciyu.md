---
description: Просто   update  висить  больше ~3s
---

# Удалить  зависшую транзакцию

### Что  делаем:&#x20;

* выяснить причину  ( pg\_statements,  анализ логов)&#x20;

### Быстро решить проблему

1. Найти ID заблокированной таблицы

```sql
SELECT oid FROM pg_class WHERE relname='book'
```

2. Найти ID  зависшей  транзакции транзакции

```sql
SELECT pid FROM pg_locks WHERE relation={id предыдущего запроса}
```

3. Ос тановить транзакцию&#x20;

```sql
SELECT pg_cancel_backend({id пердыдущего запроса})
```

4. Решаюйщий, если  пунтк  3, не помог

```sql
SELECT pg_terminate_backend({id пердыдущего запроса})
```

---
description: Что  важного в  настройке
---

# Keycloak

### Токены

В OpenID Connect, как положено, имеется Access Token, который нужно включать в заголовок Authorization, чтобы получить те же [сведения о пользователе](https://openid.net/specs/openid-connect-core-1\_0.html#UserInfo), и Refresh Token, который нужен для обновления Access Token. А ещё есть [ID Token](https://openid.net/specs/openid-connect-core-1\_0.html#IDToken).

Именно ID Token является [JWT](http://blog.gelin.ru/2017/09/jwt.html) токеном, который можно проверить публичным RSA ключом. И именно там содержатся некоторые сведения о пользователе. Можно не делать дополнительных запросов на Keycloak, а сразу извлечь всё, что надо, из ID Token.

### Политика

Политика Keycloak  - основана  на   [адаптерах](https://www.keycloak.org/docs/latest/securing\_apps/index.html#what-are-client-adapters).

### Уменьшить кол-во  хождений  по сети&#x20;

Direct Access Grants. Чтобы избежать большого количества хождения по сети сервисов к Keycloakдля валидации токенов при каждом реквесте, забирать из Keycloak публичный ключ при старте сервиса и каждый  сервис   валидирует токен,  этим публичным  ключом.

#### Пример  настройки от сбертеч

{% file src="../.gitbook/assets/Rukovodstvo_po_ekspluataczii_IAM_9e95410b16.pdf" %}

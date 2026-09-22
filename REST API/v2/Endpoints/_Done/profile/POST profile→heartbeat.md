---
aliases:
tags:
  - Endpoint
method: POST
url: /profile/heartbeat
description: Обновляет дату в сети в профиле
---
___
## Auth
Сессия

## Запрос
Нет

## Ответ
```ts
{
	ok: true
}
```

## Ошибки
Нет

## Заметки
Троттлинг 60с;
Обновляет `lastOnlineAt` для авто-статуса (вызывается клиентским `PresenceHeartbeat` при видимой вкладке).
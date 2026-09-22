---
aliases:
tags:
  - Endpoint
method: POST
url: /profile/steam
description: Реимпорт игр из уже привязанного Steam
---
___
## Auth
Сессия

## Запрос
Нет

## Ответ
```ts
{
	imported: number
}
```

## Ошибки
400 `steam_not_linked`;
503 `steam_not_configured`.

## Заметки
Реимпорт игр из уже привязанного Steam.
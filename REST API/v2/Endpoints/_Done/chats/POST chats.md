---
aliases:
tags:
  - Endpoint
method: POST
url: /chats
description: Создать/получить чат
---
___
## Auth
Сессия

## Запрос
```ts
{
	kind: "dm"|"team",
	profileId?,
	teamId?
}
```

## Ответ
```ts
{
	chatId
}
```
(201 создан / 200 уже есть)

## Ошибки
404 таргет не найден / не друг /
не участник команды / таргет запретил DM (`messageVisibility=NONE`);
422 self-DM;
429 (≤10 новых DM/мин).

## Заметки
Создать/получить чат.
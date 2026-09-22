---
aliases:
tags:
  - Endpoint
method: GET
url: /chats/[id]/messages
description: Получить сообщения в чате
---
___
## Auth
Сессия

## Запрос
`limit` (1–50, деф. 30), `cursor` (назад, по createdAt desc),
`after` (вперёд для поллинга, по createdAt asc).

## Ответ
```ts
{
	items: MessageDTO[];
	nextCursor: string|null
}
```
![[MessageDTO]]

## Ошибки
Нет

## Заметки
Получить сообщения в чате. При первой странице/поллинге обновляет
`lastReadAt`; удалённые — `body:null, deleted:true`.
---
aliases:
tags:
  - Endpoint
method: POST
url: /chats/[id]/messages
description: Изменение сообщения в чате
---
___
## Auth
Сессия

## Запрос
```ts
{
	body
}
```
(1–2000 после санации: срез C0-control кроме `\t`/`\n`

## Ответ
`MessageDTO` (201)
![[MessageDTO]]

## Ошибки
422 пусто/длинно;
429 (≤5 сообщений/10с).

## Заметки
Изменение сообщения в чате.
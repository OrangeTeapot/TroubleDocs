---
aliases:
tags:
  - Endpoint
method: DELETE
url: /chats/[id]/messages/[messageId]
description: Soft-удаление своего сообщения в чате
---
___
## Auth
Сессия

## Запрос
Нет

## Ответ
```ts
{
	deleted: true
}
```

## Ошибки
404 не автор / не в этом чате (не палим).

## Заметки
Soft-удаление СВОЕГО сообщения в чате (`deletedAt`, тело стирается).
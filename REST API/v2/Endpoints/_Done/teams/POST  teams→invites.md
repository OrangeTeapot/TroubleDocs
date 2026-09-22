---
aliases:
tags:
  - Endpoint
method: POST
url: /teams/invites
description: Принять/отклонить приглашение в команду
---
___
## Auth
Сессия

## Запрос
```ts
{
	inviteId,
	action: "accept"|"decline"
}
```
`accept` создаёт членство в транзакции.

## Ответ
```ts
{
	status
}
```

## Ошибки
Нет

## Заметки
Принять/отклонить приглашение в команду.
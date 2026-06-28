---
aliases:
tags:
  - Endpoint
method: POST
url: /friends
description: Изменение списка друзей, входящих и исходящих заявок
---
___
## Auth
Сессия

## Запрос
```ts
{
	profileId;
	action: "request"|"accept"|"decline"|"remove"
}
```

## Ответ
```ts
{
	state: "none"|"friends"|"outgoing"|"incoming"
}
```

## Ошибки
409 - действие невалидно для текущего состояния;
422 - self/таргет не найден.

## Заметки
`request` авто-принимает встречную заявку.
Гонка пары разрешается через unique `pairKey`.
`remove` снимает дружбу/заявку в любом направлении (рвёт доступ к DM).
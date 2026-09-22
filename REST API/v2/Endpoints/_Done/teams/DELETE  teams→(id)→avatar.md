---
aliases:
tags:
  - Endpoint
method: DELETE
url: /teams/[id]/avatar
description: Удаление обложки команды
---
___
## Auth
Сессия

## Запрос
Нет

## Ответ
```ts
{
	avatarUrl: null
}
```

## Ошибки
403 не автор

## Заметки
Удаление обложки команды, только автор.
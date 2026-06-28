---
aliases:
tags:
  - Endpoint
method: DELETE
url: /ideas/[id]/avatar
description: Удаление обложки идеи
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
Удаление обложки идеи, только автор.
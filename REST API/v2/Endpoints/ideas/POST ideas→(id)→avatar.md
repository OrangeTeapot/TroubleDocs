---
aliases:
tags:
  - Endpoint
method: POST
url: /ideas/[id]/avatar
description: Изменение обложки идеи
---
___
## Auth
Сессия

## Запрос
`multipart` file

## Ответ
```ts
{
	avatarUrl
}
```

## Ошибки
403 не автор

## Заметки
Изменение обложки идеи, только автор.
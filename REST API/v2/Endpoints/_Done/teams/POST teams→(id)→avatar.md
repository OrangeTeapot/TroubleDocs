---
aliases:
tags:
  - Endpoint
method: POST
url: /teams/[id]/avatar
description: Изменение обложки команды
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
Изменение обложки команды, только автор.
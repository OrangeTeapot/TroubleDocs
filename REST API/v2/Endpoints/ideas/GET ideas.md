---
aliases:
tags:
  - Endpoint
method: GET
url: /ideas
description: Список идей
---
___
## Auth
Сессия

## Запрос
`q`, `visibility`, `suggestGame` (bool),
  `gameId`, `limit` (деф. 24, макс 100), `cursor`.

## Ответ
```ts
{
	items: IdeaDTO[];
	nextCursor: string|null
}
```

## Ошибки
Нет

## Заметки
Видны только доступные пользователю идеи (PUBLIC; свои; TEAM где приглашён).
Курсорная пагинация (createdAt desc, id desc). Фильтры складываются (AND).

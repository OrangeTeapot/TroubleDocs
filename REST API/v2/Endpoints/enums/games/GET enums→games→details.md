---
aliases:
tags:
  - Endpoint
method: GET
url: /enums/games/details
description: Детальная информация о игре из Steam
---
___
## Auth
Сессия

## Запрос
 `?appId=` (Steam appId)

## Ответ
 `SteamAppSummary`:
```ts
{
	appId;
	name;
	iconUrl;
	developer;
	publisher;
	type;
	isFree;
	categories: {
		id;
		description?
	}[] | null
}
```

## Ошибки
400 неверный appId;
404 нет в Steam.

## Заметки
Детальная информация о игре из Steam
---
aliases:
tags:
  - Endpoint
method: GET
url: /dictionaries/games/search
description: Мульти-провайдерный поиск игр
---
___
## Auth
Сессия

## Запрос
`?q=` (≥2 симв.).

## Ответ
 `SearchItem[]` (union по `source`):
  ### BuiltIn
```ts
{
	source,
	name,
	iconUrl,
	developer,
	publisher,
	isFree
}
```
  ### Steam
```ts
{
	source,
	appId,
	name,
	iconUrl
}
```
  ### IGDB
```ts
{
	source,
	igdbId,
	name,
	iconUrl,
	developer,
	publisher,
	isFree: false,
	platforms,
	stores,
	minPlayers,
	maxPlayers
}
```

## Ошибки
502 при сбое Steam, если нет builtin-фолбэка.

## Заметки
Мульти-провайдерный поиск (builtin → steam → igdb, дедуп по нормализованному имени, ≤8).
IGDB env-gated (Twitch).

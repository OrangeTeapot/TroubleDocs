---
aliases:
tags:
  - Endpoint
method: GET
url: /dictionaries/players
description: Поиск игроков (для приглашений в идею)
---
___
## Auth
Сессия

## Запрос
`?q=` (≥2 симв.)

## Ответ
```ts
{
	id;
	displayName;
	username;
	avatarUrl;
	hue:number
}[]
```
 Только публичные профили (`publicProfileWhere`), без себя, до 20.

## Ошибки
Нет

## Заметки
Поиск игроков (для приглашений в идею).
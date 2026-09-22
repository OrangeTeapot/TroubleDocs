---
aliases:
tags:
  - Endpoint
method: GET
url: /profile/xbox
description: Привязка Xbox
---
___
## Auth
Сессия

## Запрос
```ts
{
	action?: "start"|"verify"|"cancel"|"resync",
	gamertag?: string
}
```
`gamertag` обязателен для `start`; `resync` авто-детектится у привязанного

## Ответ
`start`:
```ts
{
	pending: true,
	gamertag,
	code
}
```
Код: `TRBL-XXXXXX`
`verify`:
```ts
{
	linked: true,
	verified: true,
	gamertag
}
```
`cancel`:
```ts
{
	pending: false
}
```
`resync`:
```ts
{
	linked: true,
	verified: true,
	gamertag,
	imported
}
```

## Ошибки
404 `xbox_not_found`;
409 `xbox_taken`;
422 `xbox_code_missing`;
502 `xbox_upstream`;
503 `xbox_not_configured`.

## Заметки
Привязка Xbox по геймертегу через код в bio (3 шага). Требует `XBOX_API_KEY`.
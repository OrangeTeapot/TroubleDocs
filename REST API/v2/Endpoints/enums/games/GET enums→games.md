---
aliases:
tags:
  - Endpoint
method: GET
url: /enums/games
description: Список курируемых игр
---
___
## Auth
Сессия

## Запрос
`?q=` (≥2 симв.).

## Ответ
 До 20 результатов.
```ts
{
	id;
	name;
	iconUrl;
	developer;
	publisher;
	isFree
}[]
```

## Ошибки
Нет

## Заметки
Курируемый встроенный каталог игр (не-Steam).
---
aliases:
tags:
  - Endpoint
method: POST
url: /profile/discord
description: Реимпорт игр из уже привязанного Discord
---
___
## Auth
Сессия

## Запрос
Нет

## Ответ
```ts
{
	platforms: Record<string, boolean>;
	steam: {
		found: boolean;
		id: string|null;
		linked: boolean;
		imported: number;
		taken: boolean
	}
}
```

## Ошибки
400 `discord_not_linked`. 

## Заметки
Реимпорт игр из Discord-connections (нужна привязка Discord).
При наличии Steam-связи авто-импортирует библиотеку.
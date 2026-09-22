---
aliases:
tags:
  - Endpoint
method: GET
url: /subscriptions
description: Получение информации о подписке
---
___
## Auth
Сессия

## Запрос
Нет

## Ответ
```ts
{
	plan:"more_trouble";
	active: boolean;
	currentPeriodEnd: string|null }
```
  `active` = status active И (end null ИЛИ в будущем); null end = бессрочно

## Ошибки
Нет

## Заметки
Получение информации о подписке
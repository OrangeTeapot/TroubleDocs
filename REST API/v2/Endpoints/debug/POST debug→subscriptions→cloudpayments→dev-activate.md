---
aliases:
tags:
  - Endpoint
method: POST
url: /debug/subscriptions/cloudpayments/dev-activate
description: Получение подписки для отладки
---
___
## Auth
Сессия

## Запрос
```ts
{
	period?: "month"|"year"
}
```
(деф. month).

## Ответ
```ts
{
	active: true;
	currentPeriodEnd: string|null
}
```
(без HMAC/вебхука; provider `cloudpayments-dev`).

## Ошибки
Нет

## Заметки
Только для локального теста, при `CLOUDPAYMENTS_DEV_ACTIVATE=true` (иначе `404`).
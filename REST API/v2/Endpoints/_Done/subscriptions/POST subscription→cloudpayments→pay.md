---
aliases:
tags:
  - Endpoint
method: POST
url: /subscriptions/cloudpayments/pay
description: Вебхук CloudPayments
---
___
## Auth
Сессия

## Запрос
`application/x-www-form-urlencoded` — `AccountId`, `TransactionId`, `Amount`,
  `Currency` (RUB), `Data` (JSON `{userId?}`);
  заголовок `Content-HMAC` = Base64(HMAC-SHA256(rawBody, secret)).

## Ответ
НЕ использует конверт `{result,meta}`.
Принято/активировано:
```ts
{
	code: 0
}
```
отбой → CloudPayments повторит:
```ts
{
	code: 13
}
```

## Ошибки
Нет

## Заметки
Вебхук CloudPayments (публичный, защита HMAC;).
HMAC по сырому телу; идемпотентность по `ProcessedPayment(provider,transactionId)`;
период по сумме (month=300 / year=3000 RUB ±0.5), продление от текущего конца.
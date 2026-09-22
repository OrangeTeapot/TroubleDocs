---
aliases:
tags:
  - Endpoint
method: GET
url: /debug/error
description: Тест трекинга ошибок
---
___
## Auth
Сессия

## Запрос
`token` (обяз.). 

## Ответ
Бросает необработанную ошибку → 500.

## Ошибки
404 если `DEBUG_ERROR_TOKEN` не задан/не совпал (timing-safe);
429 (≤5/мин на IP).

## Заметки
Тест трекинга ошибок (GlitchTip). Token-gated.
---
aliases:
tags:
  - Endpoint
method: GET
url: /notifications/events
description: Получение ленты уведомлений
---
___
## Auth
Сессия

## Запрос
Нет

## Ответ
`NotificationDTO[]`
При выключенном флаге → `[]`.
![[NotificationDTO]]

## Ошибки
Нет

## Заметки
Лента уведомлений получателя (recipient-only из сессии, ≤50).
Эмит только внутренний (нет публичного create); сейчас эмитится `request-accepted` (приём заявки в друзья).
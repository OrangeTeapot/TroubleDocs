---
aliases:
tags:
  - Endpoint
method: GET
url: /teams/[id]
description: Получение команды по id
---
___
## Auth
Сессия

## Запрос
Нет

## Ответ
`TeamDTO`
![[TeamDTO]]

## Ошибки
404 если не участник (не палим существование).

## Заметки
Получение одной команды по slug или id.
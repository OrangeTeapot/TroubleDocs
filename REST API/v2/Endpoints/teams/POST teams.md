---
aliases:
tags:
  - Endpoint
method: POST
url: /teams
description: Создание команды
---
___
## Auth
Сессия

## Запрос
`name` (2–60), `description` (≤500, nullable).

## Ответ
`TeamDTO` (создатель → OWNER). Слаг из имени (транслит + уникализация, ретрай при гонке).
![[TeamDTO]]

## Ошибки
Нет

## Заметки
Создание команды
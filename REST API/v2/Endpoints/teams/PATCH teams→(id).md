---
aliases:
tags:
  - Endpoint
method: PATCH
url: /teams/[id]
description: Изменение команды владельцем
---
___
## Auth
Сессия

## Запрос
`name?`, `description?`

## Ответ
`TeamDTO`
![[TeamDTO]]

## Ошибки
403 не владелец.

## Заметки
Изменение команды владельцем. Слаг неизменяем.
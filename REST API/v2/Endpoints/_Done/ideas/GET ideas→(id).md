---
aliases:
tags:
  - Endpoint
method: GET
url: /ideas/[id]
description: Получение идеи по id
---
___
## Auth
Сессия

## Запрос
Нет

## Ответ
`IdeaDTO`
![[IdeaDTO]]

## Ошибки
404 если нет доступа
(`canViewIdea`: PUBLIC всем; PRIVATE только автору; TEAM автору+приглашённым).

## Заметки
Одна идея (slug или id).
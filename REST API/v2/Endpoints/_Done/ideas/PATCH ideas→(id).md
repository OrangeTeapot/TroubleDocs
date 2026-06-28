---
aliases:
tags:
  - Endpoint
method: PATCH
url: /ideas/[id]
description: Изменение идеи
---
___
## Auth
Сессия

## Запрос
поля как в create + `pinned`
![[POST ideas#Запрос]]

## Ответ
`IdeaDTO`
![[IdeaDTO]]

## Ошибки
403 не автор; 
422 валидация.

## Заметки
Только автор идеи может изменить. 
Переданные массивы (gameIds/inviteProfileIds/…) ПОЛНОСТЬЮ замещают прежние (в транзакции).
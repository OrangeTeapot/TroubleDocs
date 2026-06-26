---
aliases:
tags:
  - Endpoint
method: GET
url: /ideas/[id]/matches
description:
---
___
## Auth
Сессия

## Запрос
Нет

## Ответ
`PlayerMatch[]`:
![[PlayerMatchDTO]]

## Ошибки
400 `not_applicable` (visibility≠PUBLIC или peopleScope=NONE);
404 нет доступа.

## Заметки
Прямой подбор игроков.
Охват по `peopleScope` ([[PeopleScopeEnum]]).
Учитывает `matchVisibility` кандидата.
`languages` отдаются только если позволяет приватность.
Cap 500 кандидатов.
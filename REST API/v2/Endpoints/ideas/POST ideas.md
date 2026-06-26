---
aliases:
tags:
  - Endpoint
method: POST
url: /ideas
description:
---
___
## Auth
Сессия

## Запрос
`title` (3–100), `description`
  (≤1000, nullable), `minPlayers`/`maxPlayers` (1–100), `scheduledAt` (ISO, nullable),
  `durationMinutes` (15–1440, деф. 120), `visibility` (деф. PUBLIC), `peopleScope` (деф. ANYONE),
  `withoutGames`, `suggestGame`, `gameIds` (≤50), `inviteProfileIds` (≤50), `requiredSources`, `crossPlayOnly`.

## Ответ
[[IdeaDTO]] (201)
![[IdeaDTO]]

## Ошибки
422 `game_not_found`/`profile_not_found`/
  maxPlayers<minPlayers.

## Заметки
title авто-генерится из первой игры, если не задан.
Слаг уникализируется.
Нужен хотя бы один из title / gameIds / withoutGames / suggestGame.
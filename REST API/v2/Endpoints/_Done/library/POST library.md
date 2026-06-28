---
aliases:
tags:
  - Endpoint
method: POST
url: /library
description:
---
___
## Auth
Сессия

## Запрос
Идентификация — `steamAppId:number` ИЛИ `name:string`; метаданные (опц.)
  `iconUrl` (safe-URL), `developer`, `publisher`, `isFree`, `igdbId`, `platforms` (≤16),
  `stores` (≤16), `minPlayers`, `maxPlayers`; владение (обяз.)
  `sources: { source:GameSource; hasLicense:boolean }[]` (≥1).

## Ответ
`ProfileGameDTO` (201).
![[ProfileGameDTO]]

## Ошибки
Нет

## Заметки
Advisory-lock по nameNormalized
против дублей `Game`.
Авто-дозаполнение из Steam appdetails/IGDB.
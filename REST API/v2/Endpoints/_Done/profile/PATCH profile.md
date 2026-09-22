---
aliases:
tags:
  - Endpoint
method: PATCH
url: /profile
description: Изменение своего профиля
---
___
## Auth
Сессия

## Запрос
Все поля опциональны:
`displayName` (2–32), `bio` (≤256, nullable), `timezone` (≤64, nullable),
`languages` (≤30), `availability` (≤200 слотов), `availabilityDates` (≤60; прошедшие даты отбрасываются), `profilePrivacy`, `bioPrivacy|timezonePrivacy|languagesPrivacy|availabilityPrivacy|gamesPrivacy`, `matchVisibility`, `messageVisibility`, `activityMode`, `busyStatus`.

## Ответ
Полный `ProfileDTO` после обновления.
![[ProfileDTO]]

## Ошибки
400 битый JSON;
422 валидация.

## Заметки
Изменение своего профиля.
Слоты/даты доступности пишутся атомарно (deleteMany+createMany). По-польная приватность ограничена потолком глобальной (поле не может быть публичнее `profilePrivacy`).
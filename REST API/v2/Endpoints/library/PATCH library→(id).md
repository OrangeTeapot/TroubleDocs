---
aliases:
tags:
  - Endpoint
method: PATCH
url: /library/[id]
description: Редактирование свойств игры в библиотеке
---
___
## Auth
Сессия

## Запрос
```ts
{
	preference: GamePreferenceEnum
}
```
![[GamePreferenceEnum]]
или
```ts
{
	action: "addSource",
	source,
	hasLicense
}
```
 или
```ts
{
	action: "removeSource",
	source
}
```
или
```ts
{
	source,
	hasLicense
}
```
(legacy-тоггл лицензии).

## Ответ
Обновлённый [[ProfileGameDTO]]
![[ProfileGameDTO]]

## Ошибки
Нет

## Заметки
Редактирование свойств игры в библиотеке.
---
aliases:
tags:
  - Endpoint
method: GET
url: /dictionaries/languages
description: Публичный справочник языков
---
___
## Auth
Нет

## Запрос
Нет

## Ответ
```ts
{
	code;
	name
}[]
```
 ISO 639-1 + локализованные имена через `Intl.DisplayNames`.

## Ошибки
Нет

## Заметки
Публичный справочник языков.
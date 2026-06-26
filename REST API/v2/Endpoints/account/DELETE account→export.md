---
aliases:
tags:
  - Endpoint
method: DELETE
url: /account/export
description: Получение данных пользователя в виде json
---
___
## Auth
Сессия

## Запрос
Нет

## Ответ
Файл `application/json` (Content-Disposition: attachment, no-store):
  ```ts
  {
	  exportedAt: ISO,
	  account: {
		  …все данные пользователя…
	  }
  }
  ```
  БЕЗ секретов (хэши паролей,
  OAuth-токены, токены сессий). (Переносимость данных.)
## Ошибки
Нет

## Заметки
Нет
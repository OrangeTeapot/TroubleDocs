---
aliases:
tags:
  - Endpoint
method: DELETE
url: /library/[id]
description: Удаление игры из библиотеки пользователя
---
___
## Auth
Сессия

## Запрос
Нет

## Ответ
```ts
{
	id: string
}
```

## Ошибки
Нет

## Заметки
Удалить игру из библиотеки (каталог `Game` не трогается).
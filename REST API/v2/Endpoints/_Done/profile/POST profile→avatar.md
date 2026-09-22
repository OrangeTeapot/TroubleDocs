---
aliases:
tags:
  - Endpoint
method: POST
url: /profile/avatar
description: Изменение аватарки своего профиля
---
___
## Auth
Сессия

## Запрос
`multipart/form-data`, поле `file` — PNG/JPEG/WEBP, ≤2 МБ.

## Ответ
Ссылка на изображение в формате webp.
```ts
{
	avatarUrl: string
}
```
Sharp ре-энкодит/ресайзит/срезает EXIF.

## Ошибки
400 `no_file`;
413 `too_large`;
415 `bad_type`/`bad_image`.

## Заметки
Изменение аватарки своего профиля.
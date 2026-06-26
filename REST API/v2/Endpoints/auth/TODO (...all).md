---
aliases:
tags:
  - Endpoint
method: TODO
url: /auth/[...all]
description:
---
___
## Auth
Сессия

## Запрос
Нет

## Ответ
Нет

## Ошибки
Нет

## Заметки
Catch-all, делегирован библиотеке **Better Auth** (`toNextJsHandler`). Конфиг —
`lib/auth.ts` (email+password, плагин username, Discord-провайдер при заданных
`DISCORD_CLIENT_ID/SECRET`). Не использует конверт `{result,meta}` — формат Better Auth.

Основные эндпоинты:
- `POST /api/auth/sign-up/email` — регистрация email+пароль (в закрытой бете заблокирована
  при `BETA_DISABLE_SIGNUP=true`; публичная регистрация идёт через `/api/v1/beta/signup`).
- `POST /api/auth/sign-in/email` — вход по email+паролю.
- `POST /api/auth/sign-in/username` — вход по нику+паролю (плагин username).
- `POST /api/auth/sign-out` — выход.
- `GET  /api/auth/get-session` — текущая сессия.
- `POST /api/auth/request-password-reset` / `POST /api/auth/reset-password` — сброс пароля по токену.
- `POST /api/auth/change-email` — смена email с подтверждением на новый адрес.
- `POST /api/auth/update-user` — смена `name` / `username` / `displayUsername`.
- `POST /api/auth/sign-in/social` (`provider: "discord"`) + callback — Discord OAuth
  (только при включённом провайдере; новые аккаунты в закрытой бете блокируются хуком).
- `POST /api/auth/link-account` / `unlink-account` — привязка/отвязка соц-провайдера.

Параметры пароля: длина 8–72, проверка состава. Rate-limit Better Auth: 100 запросов / 60с.
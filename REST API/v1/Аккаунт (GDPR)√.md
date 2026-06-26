---
aliases:
tags:
---
___

### DELETE /api/v1/account
- **Auth:** сессия. **Запрос:** нет.
- **Ответ (`result`):** `{ deleted: true }`. Каскадно удаляет профиль и связанные данные,
  гасит cookie. (Право на забвение.)

### GET /api/v1/account/export
- **Auth:** сессия. **Запрос:** нет.
- **Ответ:** файл `application/json` (Content-Disposition: attachment, no-store):
  `{ exportedAt: ISO, account: {…все данные пользователя…} }` БЕЗ секретов (хэши паролей,
  OAuth-токены, токены сессий). (Переносимость данных.)
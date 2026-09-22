---
aliases:
tags:
  - Endpoint
method: POST
url: /teams/[id]/members
description:
---
___
## Auth
Сессия

## Запрос
```ts
{
	profileId
}
```

## Ответ
`TeamDTO` (идемпотентно по unique teamId+profileId, роль MEMBER). 
![[TeamDTO]]

## Ошибки
403; 422 `profile_not_found`.

## Заметки
Добавление участника в команду владельцем.
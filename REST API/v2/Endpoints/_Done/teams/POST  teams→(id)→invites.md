---
aliases:
tags:
  - Endpoint
method: POST
url: /teams/[id]/invites
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
```ts
{
	inviteId;
	status;
	inviteeProfileId
}
```

## Ошибки
409 если уже участник

## Заметки
Владелец приглашает игрока — создаёт PENDING `TeamInvite`.
Идемпотентно (unique teamId+invitee; DECLINED→PENDING);
rate-limit 20/5мин;
только OWNER;
роль всегда MEMBER.
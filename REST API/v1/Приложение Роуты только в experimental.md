---
aliases:
tags:
---
___

Следующие эндпоинты есть в ветке **experimental** и приедут в beta со следующим промоушеном
(на момent написания их НЕТ в beta):

### POST /api/v1/teams/[id]/invites  *(experimental)*
Владелец приглашает игрока — создаёт PENDING `TeamInvite`. **Запрос:** `{ profileId }`.
**Ответ:** `{ inviteId; status; inviteeProfileId }`. Идемпотентно (unique teamId+invitee; DECLINED→PENDING);
409 если уже участник; rate-limit 20/5мин; только OWNER; роль всегда MEMBER.

### GET/POST /api/v1/teams/invites  *(experimental)*
Входящие приглашения в команду. GET → список `IncomingTeamInviteDTO`
(`{ inviteId; teamId; teamSlug; teamName; teamAvatarUrl; role; invitedByName }`).
POST `{ inviteId, action:"accept"|"decline" }` → `{ status }` (accept создаёт членство в транзакции).

### GET /api/v1/notifications/events  *(experimental, флаг NEXT_PUBLIC_NOTIFICATIONS_ENABLED)*
Лента уведомлений получателя (recipient-only из сессии, ≤50). **Ответ (`result`):**
```ts
{ id; kind:"request-accepted"|"idea-response"|"new-match"; text; href;
  actorName; actorAvatarUrl:string|null; actorHue:number; createdAt; read:boolean }[]
```
При выключенном флаге → `[]`. Эмит только внутренний (нет публичного create); сейчас
эмитится `request-accepted` (приём заявки в друзья).

### POST /api/v1/notifications/read  *(experimental)*
Отметить все свои уведомления прочитанными (сброс бейджа). **Ответ:** `{ updated: number }`.
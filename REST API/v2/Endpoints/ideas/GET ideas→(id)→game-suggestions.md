---
aliases:
tags:
  - Endpoint
method: GET
url: /ideas/[id]/game-suggestions
description:
---
___
## Auth
Сессия

## Запрос
Нет

## Ответ
```ts
{
	participants: {
		id;
		displayName
	}[];
	suggestions: GameSuggetionDTO[]
}
```
![[GameSuggestionDTO]]

## Ошибки
400 `not_applicable` (suggestGame=false);
404 нет доступа.

## Заметки
Обратный подбор игр под ростер.
Ростер по visibility (PRIVATE=автор;
TEAM/приглашённые=автор+invites;
PUBLIC без invites=публичные профили);
Группировка по сигнатуре, топ-20.
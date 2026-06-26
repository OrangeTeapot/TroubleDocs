---
aliases:
tags:
  - Endpoint
method: GET
url: /ideas/[id]/suggest
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
	players: PlayerMatchDTO[];        // пусто если visibility≠PUBLIC или peopleScope=NONE
	games: GameSuggestionDTO[];       // пусто если suggestGame=false
	participants: {
		id;
		displayName
	}[];
	group: {
		size;
		score;
		belowMin;
		players: PlayerMatchDTO[];
		games: GameSuggestionDTO[]
	} | null;
	peopleScope: string
}
```
![[PlayerMatchDTO]]
![[GameSuggestionDTO]]

## Ошибки
  Нет

## Заметки
Единый эндпоинт: игроки + игры + лучшая группа. `group=null`, если нет кандидатов с `percent>0`; лучшая группа = топ-N (N≤maxPlayers) с `percent>0` + игры под состав (автор + выбранные).
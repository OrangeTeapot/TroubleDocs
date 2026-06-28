---
aliases:
tags:
  - Endpoint
method: GET
url: /friends
description: Список друзей, входящих и исходящих запросов
---
___
## Auth
Сессия

## Запрос
Нет

## Ответ
```ts
{
	friends: FriendDTO[];
	incoming: FriendDTO[];
	outgoing: FriendDTO[]
},
```
![[FriendDTO]]

## Ошибки
Нет

## Заметки
  `friends` = ACCEPTED; 
  `incoming` = PENDING ко мне;
  `outgoing` = PENDING от меня.
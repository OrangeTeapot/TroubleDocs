---
aliases:
tags:
  - DTO
---
___
```ts
{
	chatId;
	kind: ChatKindEnum;
	title;
	slug: string|null;
	avatarUrl;
	hue;
	lastMessage:{
		body: string|null;
		createdAt;
		mine
	}|null;
	unreadCount: number
}
```
![[ChatKindEnum]]
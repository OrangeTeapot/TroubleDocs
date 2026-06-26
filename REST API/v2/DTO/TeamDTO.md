---
aliases:
tags:
  - DTO
---
___
```ts
{
	id;
	slug;
	name;
	description;
	avatarUrl;
	createdAt;
	memberCount;
	viewerRole: "OWNER"|"MEMBER"|null;
	members: TeamMemberDTO[]
}
```
![[TeamMemberDTO]]
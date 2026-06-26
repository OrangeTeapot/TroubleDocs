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
	title;
	description;
	minPlayers;
	maxPlayers;
	scheduledAt;
	durationMinutes;
	status;
	visibility: VisibilityEnum;
	peopleScope: PeopleScopeEnum;
	withoutGames;
	suggestGame;
	pinned;
	avatarUrl;
	requiredSources: GameSourceEnum[];
	crossPlayOnly;
	games: {
		id;
		name;
		iconUrl
	}[];
	invites: {
		profileId;
		profileSlug;
		displayName;
		username;
		avatarUrl
	}[];
	inviteProfileIds: string[];
	author: {
		id;
		slug;
		displayName;
		avatarUrl
	};
	createdAt
}
```
![[VisibilityEnum]]
![[GameSourceEnum]]
---
aliases:
tags:
  - DTO
---
___
```ts
{
	id: string;
	gameId: string;
	name: string;
	iconUrl: string|null;
    steamAppId: number|null;
    developer: string|null;
    publisher: string|null;
    isFree: boolean;
    preference: GamePreferenceEnum;
    playtimeMinutes: number;
    sources: {
	    source: GameSourceEnum;
	    hasLicense: Boolean
	}[];
    platforms: string[];
    stores: string[];
    minPlayers: number|null;
    maxPlayers: number|null
}
```

![[GameSourceEnum]]
![[GamePreferenceEnum]]
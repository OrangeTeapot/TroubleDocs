---
aliases:
tags:
  - DTO
---
___
```ts
{
	id: string;
	slug: string|null;
	displayName: string;
	username: string|null;
	displayUsername: string|null;
	email: string;
	bio: string|null;
	timezone: string|null;
	avatarUrl: string|null;
	activityMode: "AUTO"|"UNKNOWN";
	busyStatus: "FREE"|"BUSY"|"DND"|"LOOKING";
	lastOnlineAt: string|null;
	// ISO
	profilePrivacy: "PUBLIC"|"FRIENDS"|"FRIENDS_OF_FRIENDS"|"PRIVATE";
	bioPrivacy: PrivacyEnum;
	timezonePrivacy: PrivacyEnum;
	languagesPrivacy: PrivacyEnum;
	availabilityPrivacy: PrivacyEnum;
	gamesPrivacy: PrivacyEnum;
				
	matchVisibility: "EVERYONE"|"FRIENDS"|"FRIENDS_OF_FRIENDS"|"NONE";
	messageVisibility: "EVERYONE"|"FRIENDS"|"FRIENDS_OF_FRIENDS"|"NONE";
	steamId: string|null;
	moreTrouble: boolean;
	languages: string[];
	availability: {
		dayOfWeek:0..6;
		startMinute: number;
		endMinute: number;
		status: "FREE"|"BUSY"|"UNSURE"
	}[];
	availabilityDates: {
		date: string;
		slots: {
			startMinute;
			endMinute;
			status
		}[]
	}[];
	// только владельцу:
	discordLinked: boolean;
	xboxEnabled: boolean;
	xboxOauthEnabled: boolean;
	xboxGamertag: string|null;
	xboxVerified: boolean;
	xboxVerifyCode: string|null;
	xboxVerifyGamertag: string|null;
}
```
![[PrivacyEnum]]
![[VisibilityEnum]]
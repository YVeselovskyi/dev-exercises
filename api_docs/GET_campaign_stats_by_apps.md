# Campaigns Resources

    GET campaigns/{campaignId}/stats/apps

## Description
Returns a list of stats grouped by app for a given campaign.

***

## Return format
An array of stats.

***

## Errors
None

***

## Example
**Request**

    https://5cd3f999-f49f-4e42-8b8b-173c7185f093.mock.pstmn.io/campaigns/fc23c87a-fb0d-4315-aa2b-854f68e88f6a/stats/apps

**Return** __shortened for example purpose__
``` json
[{
	"app_id": "org.telegram.messenger.erick",
	"opportunities": 7112916,
	"impressions": 5090368
}, {
	"app_id": "bdmusic25.cam",
	"opportunities": 3338971,
	"impressions": 2210038
}, {
	"app_id": "mineworld.mwpe.gpen",
	"opportunities": 6008960,
	"impressions": 4540133
}]
```
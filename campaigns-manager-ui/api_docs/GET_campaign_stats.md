# Campaigns Resources

    GET campaigns/{campaignId}/stats

## Description
Returns a list of stats by a given campaign ID.

***

## Return format
An array of stats.

***

## Errors
None

***

## Example
**Request**

    https://5cd3f999-f49f-4e42-8b8b-173c7185f093.mock.pstmn.io/campaigns/fc23c87a-fb0d-4315-aa2b-854f68e88f6a/stats

**Return** __shortened for example purpose__
``` json
[{
	"date": "2017-10-18",
	"impressions": 66010,
	"clicks": 607
}, {
	"date": "2017-10-17",
	"impressions": 949396,
	"clicks": 152
}, {
	"date": "2017-10-16",
	"impressions": 172071,
	"clicks": 110
}, {
	"date": "2017-10-15",
	"impressions": 341037,
	"clicks": 665
}]
```
# Campaigns Resources

    GET campaigns

## Description
Returns a list of campaigns in the account.

***

## Return format
An array of campaigns.

***

## Errors
None

***

## Example
**Request**

    https://5cd3f999-f49f-4e42-8b8b-173c7185f093.mock.pstmn.io/campaigns

**Return** __shortened for example purpose__
``` json
[{
	"id": "fc23c87a-fb0d-4315-aa2b-854f68e88f6a",
	"name": "My first campaign",
	"total_budget": 1000,
	"daily_budget": 100,
	"budget_daily_left": 100,
	"views": 150,
	"clicks_today": 0,
	"clicks_yesterday": 0,
	"clicks": 8,
	"views_yesterday": 0,
	"status": "ACTIVE",
	"spending": 264600,
	"spending_today": 0
}, {
	"id": "98f7de85-ecd6-4916-9021-686371347284",
	"name": "The biggest campaign ever",
	"total_budget": 1000,
	"daily_budget": 10,
	"budget_daily_left": 10,
	"views": 1046,
	"clicks_today": 0,
	"clicks_yesterday": 0,
	"clicks": 2,
	"views_yesterday": 0,
	"status": "INACTIVE",
	"spending": 1020319,
	"spending_today": 0
}]
```
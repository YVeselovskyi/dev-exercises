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

    https://112823f5-6f6e-4e89-848d-966ba4479185.mock.pstmn.io/campaigns

**Return** __shortened for example purpose__
``` json
[{
	"id": "campaign_mEzxAQF3XbdhSzj39hnytPHhg6mbc",
	"name": "My first campaign",
	"total_budget": 1000,
	"daily_budget": 100,
	"budget_daily_left": 100,
	"views": 150,
	"clicks_today": 0,
	"clicks_yesterday": 0,
	"clicks": 8,
	"views_yesterday": 0,
	"status": "INACTIVE",
	"spending": 264600,
	"spending_today": 0
}, {
	"id": "campaign_oUJ7jIimwxtfEXr3cC7KeeaIxiNAkD",
	"name": "Just a test campaign",
	"total_budget": 1000,
	"daily_budget": 10,
	"budget_daily_left": 10,
	"views": 1046,
	"clicks_today": 0,
	"clicks_yesterday": 0,
	"clicks": 2,
	"views_yesterday": 0,
	"status": "ACTIVE",
	"spending": 1020319,
	"spending_today": 0
}]
```
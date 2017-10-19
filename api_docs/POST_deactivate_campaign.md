# Campaigns Resources

    POST campaigns/{campaignId}/deactivate

## Description
Deactivate a single campaign by a given ID.

***

## Parameters
- **campaignId** _(required)_ — The ID of the campaign.

***

## Return format
Object contains the result of the process.

***

## Errors
None

***

## Example
**Request**

    https://5cd3f999-f49f-4e42-8b8b-173c7185f093.mock.pstmn.io/campaigns/fc23c87a-fb0d-4315-aa2b-854f68e88f6a/deactivate

**Return** __shortened for example purpose__
``` json
{
    "message": "Campaign has been deactivated"
}
```
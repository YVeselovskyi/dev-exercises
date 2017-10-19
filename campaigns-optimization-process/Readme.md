# Campaign optimization process

## The problem

We need a process which will automatically improve the configuration of our campaigns based on previous stats and let us consume the logs of the service by API.

## Solution

**Create the following process:**

 * Get a list of campaigns from the NUVIAD API (see **[<code>GET</code> campaigns](../api_docs/GET_campaigns.md)**)
    * For each campaign, perform the following:
        * Get campaign stats from the NUVIAD API (see **[<code>GET</code> campaign stats by apps](../api_docs/GET_campaign_stats_by_apps.md)**)
        * Analyze stats rows and decide whether to update the campaign's "max bid" (which represents the max amount the advertiser is willing to pay in order to advertise in a certain app) by calculating the ratio between `opportunities` and `impressions` (`impressions`/`opportunities`):
            * If the result is less than 0.5, than increase `max_bid` value of the related row and perform the following:
                * Update NUVIAD API with the new `bid` value for the realted `app_id` (see **[<code>PUT</code> update campaign bid](../api_docs/PUT_update_campaign_bid.md)**)
                * Create a new log record in the provided MySQL DB. see our log schema

**Create API endpoint for getting a list of logs:**

This endpoint should return a list of logs stored in DB. each row should contain all the properties (according to [Log Schema](#log-schema)).

This endpoint should support the following query parameters:

 * `campaign_id` - A campaign ID for filtering the results.

## Log Schema

Use the following schema to update MySQL for each new log record:

| Column      | Description                                                                                |
|-------------|--------------------------------------------------------------------------------------------|
| campaign_id | The ID of the related campaign.                                                            |
| app_id      | The related `app_id` taken from the campaign's stats.                                      |
| old_bid     | The campaign's bid for the related hour before making the update.                          |
| new_bid     | The new campaign's bid for the related hour.                                               |
| ratio       | The ratio between `opportunities` and `impressions` which tells the reason for the update. |
| created_at  | The exact time when the update has been accord.                                            |

## Your mission

 * Use the provided API endpoints described in [API Endpoints](#api-endpoints).
 * Implement the solution using NodeJS.
 * Keep the code clean and reviewable.
 * When you're done, upload your solution to Github and share it with us.
 * Have fun!

## Resources

### API Endpoints

- **[<code>GET</code> campaigns](../api_docs/GET_campaigns.md)**
- **[<code>PUT</code> update campaign bid](../api_docs/PUT_update_campaign_bid.md)**
- **[<code>GET</code> campaign stats by apps](../api_docs/GET_campaign_stats_by_apps.md)**
# Campaign Manager UI

## The problem

Our advertisers need a simple solution to view and manage the campaigns in their account and also get some stats.

## Solution

Create a small SPA (Single-page application) containing two screens:

### Main screen: Camapigns list

This screen contains a list of campaigns (represents in a table) within the account, provided by the API.

Each row in the table, which represents a single campaign, should contain a few columns with data and two actions to perform on the campaign.

Table columns:
 * Status
Display the status of the campaign. This value stored in `status` attribute.
 * Campaign name
Display the name of the campaign stored in `name` attribute.
 * Total budget
Display the total budget of the campaign stored in `total_budget` attribute.
The value should be formatted to a number with “$” sign.
 * Daily budget
Display the daily budget of the campaign stored in `daily_budget` attribute.
The value should be formatted to a number with “$” sign.
 * Actions
This column should contain two buttons, each trigger an “action”:
Activate / Deactivate: this button should be changed according to the status of the campaign. In case the `status` is “ACTIVE”, than the button should be “Deactivate”, in case the `status` is “INACTIVE” than the button should be “Activate”.
Open campaign status: this button open a new screen which display the campaign’s stats.


## Your mission

 * Use the files located in [/templates](/templates) as templates for the app's screens.
 * Choose between one of the following solutions: AngularJS or ReactJS.
 * Keep the code clean and reviewable.
 * When you're done, upload it somewhere where it can be viewable by the world.
 * Have fun!

 ## Endpoints

## Resources

### API Endpoints

- **[<code>GET</code> photos](api_docs/GET_campaigns.md)**
- **[<code>POST</code> photos](api_docs/POST_activate_campaign.md)**
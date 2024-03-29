- [Overview](#overview)
- [Event List](#event-list)
- [Super Property List](#super-property-list)
- [Property List](#property-list)
- [View List](#view-list)

## Overview
Documentation for iOS Mixpanel events. Web events can be found [here](https://github.com/Morsel/morsel-web/tree/master/docs/mixpanel.md)

### Event List
This is a table of all event names, properties and descriptions that are being tracked. It should be kept up to date whenever events are added/altered

| Event Name (case sensitive) | Description                  | Properties      | Date Started |
| ------------------ | ---------------------------- | ------------ | ------------ |
| Tapped Log In      | User tapped a button to log in |   | 3/18/2014    |
| Tapped Take a Picture      | User tapped shutter button | picture_count | 3/18/2014    |
| Error - API  | An error was received with key="api" | error_message, http_status | 4/9/2014 |
| Displayed Alert to User | An message was display to a user | message | 4/9/2014 |
| Tapped Check Username Availability | User tapped to check whether their username is available | | 4/9/2014 |
| Tapped Reserve Username | User tapped to reserve their username (after inputting their email) | | 4/9/2014 |
| Tapped User Industry | User chose their associated industry | industry | 4/9/2014 |
| Tapped Share Username on Social | User shared their username reservation on social | social_type | 4/9/2014 |
| Scroll Morsel Down | A user scrolls down (sees content below) on a morsel | morsel_scroll_index, morsel_item_id, on_share, morsel_id | 4/9/2014 |
| Scroll Morsel Up | A user scrolls up (sees previous content) on a morsel | morsel_scroll_index, morsel_item_id, on_share, morsel_id | 4/9/2014 |
| Scroll Feed Left | A user scrolls left (sees previous content) on a feed | morsel_id, morsel_loaded, is_last, morsels_viewed | 4/9/2014 |
| Scroll Feed Right | A user scrolls right (sees next content) on a feed | morsel_id, morsel_loaded, is_last, morsels_viewed | 4/9/2014 |
| Tapped Prev Morsel | A user taps previous morsel button on a feed | morsel_id, morsel_loaded, is_last, morsels_viewed | 4/9/2014 |
| Tapped Next Morsel | A user taps next morsel button on a feed | morsel_id, morsel_loaded, is_last, morsels_viewed | 4/9/2014 |
| Tapped Morsel Item Thumbnail | User tapped a morsel item's thumbnail | morsel_id, morsel_item_id | 4/9/2014 |
| Tapped Share Own Morsel | User taps to share their own morsel during Add process | morsel_id, social_type, creator_id | 4/9/2014 |
| Tapped View More Description | User taps to view full description of a morsel | morsel_id | 4/9/2014 |
| Tapped Profile Picture | User taps a user's profile pic | user_action_id | 4/9/2014 |
| Tapped Profile Name | User taps a user's profile pic | user_action_id | 4/9/2014 |
| Tapped Comments | User taps to view morsel item's comments | morsel_id, morsel_item_id | 4/9/2014 |
| Tapped Share | User taps to share something | morsel_id, social_type, creator_id, share_type, event_name | 4/9/2014 |
| Tapped iTunes Link | User taps the link to go to iTunes | | 8/6/2014 |
| Authenticated with Social | User authenticates with social | social_type | 10/6/2014 |
| Signs Up | User completes a part of the signup flow | signup_step | 10/6/2014 |
| Tapped Menu Bar Icon | When a user taps the hamburger bar | menu_state | 8/19/2014 |
| Tapped Menu Option | When a user selects something from the main menu | menu_option | 8/15/2014 |

### Super Property List
This is a table of all super properties (properties that are sent with every event) names and descriptions that are being tracked. It should be kept up to date whenever super properties are added/altered

| Super Property Name | Description                  | Options      | Date Started |
| ------------------- | ---------------------------- | ------------ | ------------ |
| client_device       | Device user is using | "iphone", "web" | 3/18/2014 |
| client_version      | Version of client's code | "1.0.1" | 4/9/2014 |
| $screen_width       | Width of user's screen   | numeric | 4/9/2014 |
| $screen_height      | Height of user's screen  | numeric | 4/9/2014 |
| user_id             | User's id (if logged in) - should be set with mixpanel.identify | numeric | 4/9/2014 |
| is_staff            | Is user a staff member   | boolean | 4/9/2014 |
| is_pro              | Does user have pro account | boolean | 8/1/2014 |

### Property List
This is a table of all property names and descriptions that are being tracked. It should be kept up to date whenever properties are added/altered

| Property Name      | Description                  | Options      | Date Started |
| ------------------ | ---------------------------- | ------------ | ------------ |
| morsel_id          | The id of a morsel           | numeric      | 3/18/2014    |
| story_draft        | Whether a story is a draft (vs being published) | boolean | 3/18/2014    |
| picture_count      | Number of pictures present   | numeric      | 3/18/2014    |
| error_message      | The error passed from the API | string       | 4/9/2014    |
| http_status        | The HTTP status passed along with an error | numeric | 4/22/2014 |
| message            | The string message | string       | 4/9/2014    |
| on_share           | The user is on the morsel share page | boolean | 4/9/2014 |
| morsel_item_id     | The id of a morsel item | numeric | 4/9/2014 |
| morsel_scroll_index| The index of the item (or page) in a morsel | numeric | 4/9/2014 |
| morsel_item_count  | The number of items in a morsel | numeric | 4/9/2014 |
| morsel_loaded      | Whether the morsel has its data loaded | boolean | 4/9/2014 |
| is_last            | Whether something is the last in its list | boolean | 4/9/2014 |
| morsels_viewed     | Number of morsels a user has viewed in a feed in current session | numeric | 4/9/2014 |
| social_type        | Type of social media | "facebook", "twitter", "linkedin", "pinterest", "google_plus" | 4/9/2014 |
| user_action_id     | Id of a user who is being acted upon | numeric | 4/9/2014 |
| industry           | The industry a user associates with | "chef", "media", "diner" | 4/9/2014 |
| view                | The "view" that an event occurred on | see full table below | 3/18/2014 |
| login_type         | How does the user log in? | "facebook", "twitter", "email" | 10/6/2014 |
| signup_step | The step of the signup flow the user completed | "initial", "basic info" | 10/6/2014 |
| menu_state | whether user is opening or closing menu | "opening", "closing" | 10/6/2014 |
| menu_option | An option from the nav menu | | 10/6/2014 |
| share_subject | What type of subject was shared | "event", "morsel-detail" | 10/7/2014 |
| event_name | The title of an event | string | 10/7/2014 |

### View List
This is a table of all "views" that appear in both the app and the web version so that we have a consistent way to refer to views across our platforms for reporting. The "property name" column is what will appear in Mixpanel under the "view" property. It should be kept up to date whenever new "views" are added/altered

| Property Name      | Description                  | Date Started |
| ------------------ | ---------------------------- | ------------ |
| login_screen       | Screen where user is able to log in         | 3/18/2014    |
| your_story_edit    | View that allows users to update title, reorder morsels | 3/18/2014    |
| claim_username | User's can claim their username with email | 4/9/2014 |
| main_feed | A user's "home" feed | 4/9/2014 |
| morsel_details | The details page of a single morsel | 4/9/2014 |

- [Overview](#overview)
- [Event List](#event-list)
- [Super Property List](#super-property-list)
- [Property List](#property-list)
- [View List](#view-list)

## Overview
Documentation for Mixpanel

### Event List
This is a table of all event names, properties and descriptions that are being tracked. It should be kept up to date whenever events are added/altered

| Event Name (case sensitive) | Description                  | Properties      | Date Started |
| ------------------ | ---------------------------- | ------------ | ------------ |
| Tapped Log In      | User tapped a button to log in |   | 3/18/2014    |
| Tapped Take a Picture      | User tapped shutter button | picture_count | 3/18/2014    |
| Error - API  | An error was received with key="api" | error_message | 4/9/2014 |

### Super Property List
This is a table of all super properties (properties that are sent with every event) names and descriptions that are being tracked. It should be kept up to date whenever super properties are added/altered

| Super Property Name | Description                  | Options      | Date Started |
| ------------------- | ---------------------------- | ------------ | ------------ |
| view                | The "view" that an event occurred on | see full table below | 3/18/2014    |
| client_device       | Device user is using | "iphone", "web" | 3/18/2014    |
| client_version      | Version of client's code | "1.0.1" | 4/9/2014 |
| $screen_width       | Width of user's screen   | numeric | 4/9/2014 |
| $screen_height      | Height of user's screen  | numeric | 4/9/2014 |

### Property List
This is a table of all property names and descriptions that are being tracked. It should be kept up to date whenever properties are added/altered

| Property Name      | Description                  | Options      | Date Started |
| ------------------ | ---------------------------- | ------------ | ------------ |
| morsel_id          | The id of a morsel           | numeric      | 3/18/2014    |
| story_draft        | Whether a story is a draft (vs being published) | boolean | 3/18/2014    |
| picture_count      | Number of pictures present   | numeric      | 3/18/2014    |
| error_message      | The error passed from the API | string       | 4/9/2014    |

### View List
This is a table of all "views" that appear in both the app and the web version so that we have a consistent way to refer to views across our platforms for reporting. The "property name" column is what will appear in Mixpanel under the "view" property. It should be kept up to date whenever new "views" are added/altered

| Property Name      | Description                  | Date Started |
| ------------------ | ---------------------------- | ------------ |
| login_screen       | Screen where user is able to log in         | 3/18/2014    |
| your_story_edit    | View that allows users to update title, reorder morsels | 3/18/2014    |
| claim_username | User's can claim their username with email | 4/9/2014 |

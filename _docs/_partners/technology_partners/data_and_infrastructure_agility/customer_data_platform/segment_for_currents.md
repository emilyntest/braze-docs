---
nav_title: Segment for Currents
page_order: 2
alias: /partners/segment_for_currents/
---

# About Segment & Currents

[Segment](https://segment.com) is a customer data platform that collects and routes information from multiple sources to a variety of other locations in your marketing stack.

To get started, find the following information from your Segment dashboard:

-   Segment Write Key

Add this information to the Segment integration page on the dashboard, and press save.

![Segment]({% image_buster /assets/img_archive/currents-segment-edit.png %})

All events sent to Segment will include the user's `external_user_id` as the `userId`. At this time, Braze does not send event data for users who do not have their `external_user_id` set.

Segment's documentation is available [here](https://segment.com/docs/sources/cloud-apps/appboy/).

# Integration Details

You can export the following data from Braze to Segment:

| Event Name                | Description                                                                               |
| ------------------------- | ----------------------------------------------------------------------------------------- |
| Push Notification Sent    | A push notification was successfully sent.                                                |
| Push Notification Tapped  | User opened a push notification.                                                          |
| Push Notification Bounced | Braze was not able to send a push notification to this User.                              |
| Email Sent                | An email was successfully sent.                                                           |
| Email Delivered           | An email was successfully delivered to a User’s mail server.                              |
| Email Opened              | User opened an email.                                                                     |
| Email Link Clicked        | User clicked a link in an email. Email click tracking must be enabled.                    |
| Email Bounced             | Braze attempted to send an email, but the User’s receiving mail server did not accept it. |
| Email Marked As Spam      | User marked an email as spam.                                                             |
| Email Unsubscribed        | User clicked the unsubscribe link in an email.                                            |
| In-App Message Viewed     | User viewed an In-App Message.                                                            |
| In-App Message Clicked    | User tapped or clicked a button in an In-App Message.                                     |
| News Feed Viewed          | User viewed the native Braze News Feed.                                                   |
| News Feed Card Viewed     | User viewed a Card within the native Braze News Feed.                                     |
| News Feed Card Clicked    | User clicked on a Card within the native Braze News Feed.                                 |
| Application Uninstalled   | User uninstalled the App.                                                                 |

The following properties will be included with all Braze events sent to Segment:

| Property Name          | Type     | Description                                                                                             |
| ---------------------- | -------- | ------------------------------------------------------------------------------------------------------- |
| `app_id`               | `String` | The API Identifier of the App on which a user received a message or performed an action, if applicable. |
| `campaign_id`          | `String` | The API Identifier of the Campaign associated with the event, if applicable.                            |
| `campaign_name`        | `String` | The name of the Campaign associated with the event, if applicable.                                      |
| `message_variation_id` | `String` | The API Identifier of the Message Variation for the Campaign associated with the event, if applicable.  |
| `canvas_id`            | `String` | The API Identifier of the Canvas associated with the event, if applicable.                              |
| `canvas_name`          | `String` | The name of the Canvas associated with the event, if applicable.                                        |
| `canvas_variation_id`  | `String` | The API Identifier of the Canvas Variation associated with the event, if applicable.                    |
| `canvas_step_id`       | `String` | The API Identifier of the Canvas Step associated with the event, if applicable.                         |
| `context.traits.email` | `String` | For Email events, the email address that the email was sent to.                                         |
| `link_url`             | `String` | For Email Clicked events, the URL of the link that the user clicked on.                                 |
| `button_id`            | `String` | For In-App Message Clicked events, the index of the button the user clicked on.                         |
| `card_id`              | `String` | For News Feed Card Viewed and News Feed Card Clicked events, the API Identifier of the News Feed Card.  |

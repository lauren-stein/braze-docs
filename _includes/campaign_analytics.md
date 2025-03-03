## Campaign Analytics

Once you've launched your campaign, you can return to the details page for that campaign to view key metrics. Navigate to the **Campaigns** page and select your campaign to open the details page. For {% if include.channel == "Content Card" %}Content Cards {% elsif include.channel == "email" %}email {% elsif include.channel == "in-app message" %}in-app messages {% elsif include.channel == "push" %}push messages {% elsif include.channel == "SMS" %}SMS messages {% elsif include.channel == "whatsapp" %}WhatsApp messages {% elsif include.channel == "webhook" %}webhooks {% endif %}sent in Canvas, refer to [Canvas Analytics]({{site.baseurl}}/user_guide/engagement_tools/canvas/testing_canvases/measuring_and_testing_with_canvas_analytics/).

{% alert tip %}
Looking for definitions for the terms and metrics listed in your report? Refer to our 
  {% if include.channel == "email" %}[Email Analytics Glossary]({{site.baseurl}}/user_guide/message_building_by_channel/email/reporting_and_analytics/analytics_glossary/)
  {% elsif include.channel == "Content Card" %}[Report Metrics Glossary]({{site.baseurl}}/user_guide/data_and_analytics/report_metrics/) and filter by Content Cards
  {% elsif include.channel == "in-app message" %}[Report Metrics Glossary]({{site.baseurl}}/user_guide/data_and_analytics/report_metrics/) and filter by in-app message
  {% elsif include.channel == "push" %}[Report Metrics Glossary]({{site.baseurl}}/user_guide/data_and_analytics/report_metrics/) and filter by Push
  {% elsif include.channel == "SMS" %}[Report Metrics Glossary]({{site.baseurl}}/user_guide/data_and_analytics/report_metrics/) and filter by SMS
  {% elsif include.channel == "whatsapp" %}[Report Metrics Glossary]({{site.baseurl}}/user_guide/data_and_analytics/report_metrics/) and filter by WhatsApp
  {% elsif include.channel == "webhook" %}[Report Metrics Glossary]({{site.baseurl}}/user_guide/data_and_analytics/report_metrics/) and filter by Webhook{% endif %}.
{% endalert %}

From the **Campaign Analytics** tab, you can view your reports in a series of panels. You may see more or less than those listed in the sections below, but each has its own useful purpose.

### Campaign Details

The **Campaign Details** panel shows a high-level overview of the entire performance for your 
  {% if include.channel == "Content Card" %}Content Card.
  {% elsif include.channel == "email" %}email.
  {% elsif include.channel == "in-app message" %}in-app message.
  {% elsif include.channel == "push" %}push message.
  {% elsif include.channel == "SMS" %}SMS.
  {% elsif include.channel == "whatsapp" %}WhatApp messages.
  {% elsif include.channel == "webhook" %}webhook.
  {% endif %}

Review this panel to see overall metrics such as how many messages have been sent to how many recipients, the primary conversion rate, and the total revenue generated by this message. You can also review your general settings from this page: Delivery Settings, Audience Settings, and Conversion Settings.

{% if include.channel == "whatsapp" %}
{% alert note %}
The WhatsApp channel includes read rate. This metric is only delivered for users with read receipts on, which can vary.
{% endalert %}
{% endif %}

{% if include.channel == "Content Card" %}
![Campaign Details panel with an overview of metrics used to determine campaign performance.]({% image_buster /assets/img/cc-campaign-details.png %})

{% elsif include.channel == "email" %}
![Campaign Details panel with an overview of metrics used to determine campaign performance.]({% image_buster /assets/img/campaign_details_email.png %})

{% elsif include.channel == "push" %}
![Campaign Details panel with an overview of metrics used to determine campaign performance.]({% image_buster /assets/img/campaign_details_push.png %})

{% elsif include.channel == "SMS" %}
![Campaign Details panel with an overview of metrics used to determine campaign performance.]({% image_buster /assets/img/campaign_details_sms.png %})

{% elsif include.channel == "in-app message" %}
![Campaign Details panel with an overview of metrics used to determine campaign performance.]({% image_buster /assets/img/campaign_details_iam.png %})

In Canvas, you'll see in-app message performance mapped onto the Canvas you've created. You can use the control panel at the top of the page to clear other messaging types (channels) and only view the in-app messages in your Canvas.

![]({% image_buster /assets/img/in-app_message_canvas_reporting.png %})

{% elsif include.channel == "webhook" %}
![Campaign Details panel with an overview of metrics used to determine campaign performance.]({% image_buster /assets/img/campaign_details_webhook.png %})

{% endif %}

{% if include.channel == "Content Card" %}

#### Control groups {#cc-control-group}

To measure the impact of an individual Content Card, you can add a [control group][2] to an A/B Test. The top-level **Campaign Details** panel doesn't include metrics from the Control Group variant.

{% elsif include.channel == "SMS" %}

#### Control groups {#sms-control-group}

To measure the impact of an individual SMS message, you can add a [control group][2] to an A/B Test. The top-level **Campaign Details** panel doesn't include metrics from the Control Group variant.

{% elsif include.channel == "whatsapp" %}

#### Control groups {#whatsapp-control-group}

To measure the impact of an individual WhatsApp message, you can add a [control group][2] to an A/B Test. The top-level **Campaign Details** panel doesn't include metrics from the Control Group variant.

{% elsif include.channel == "webhook" %}

#### Control groups {#webhook-control-group}

To measure the impact of an individual webhook message, you can add a [control group][2] to an A/B Test. The top-level **Campaign Details** panel doesn't include metrics from the Control Group variant.

{% endif %}
<!--
### Message Performance

The **Message Performance** panel outlines how well your message has performed across various dimensions. The metrics in this panel vary depending on your chosen messaging channel, and whether or not you are running a multivariate test. You can click on the <i class="fa fa-eye preview-icon"></i> **Preview** icon to view your message for each variant or channel.
-->
{% if include.channel == "Content Card" %}
### Content Card Performance

The **Content Card Performance** panel outlines how well your message has performed across various dimensions. The metrics in this panel vary depending on your chosen messaging channel, and whether or not you are running a multivariate test. You can click on the <i class="fa fa-eye preview-icon"></i> **Preview** icon to view your message for each variant or channel.

![Content Card message performance analytics]({% image_buster /assets/img/cc-message-performance.png %})

{% elsif include.channel == "email" %}
### Email Performance

The **Email Performance** panel outlines how well your message has performed across various dimensions. The metrics in this panel vary depending on your chosen messaging channel, and whether or not you are running a multivariate test. You can click on the <i class="fa fa-eye preview-icon"></i> **Preview** icon to view your message for each variant or channel.

![Email message performance analytics]({% image_buster /assets/img_archive/email_message_performance.png %})

{% elsif include.channel == "in-app message" %}
### In-App Message Performance

The **In-App Message Performance** panel outlines how well your message has performed across various dimensions. The metrics in this panel vary depending on your chosen messaging channel, and whether or not you are running a multivariate test. You can click on the <i class="fa fa-eye preview-icon"></i> **Preview** icon to view your message for each variant or channel.

![In-app message performance analytics]({% image_buster /assets/img_archive/iam_message_performance.png %})

{% elsif include.channel == "push" %}
### Push Performance

The **Push Performance** panel outlines how well your message has performed across various dimensions. The metrics in this panel vary depending on your chosen messaging channel, and whether or not you are running a multivariate test. You can click on the <i class="fa fa-eye preview-icon"></i> **Preview** icon to view your message for each variant or channel.

![Push message performance analytics]({% image_buster /assets/img_archive/push_message_performance.png %})

{% elsif include.channel == "SMS" %}
### SMS Performance

The **SMS Performance** panel outlines how well your message has performed across various dimensions. The metrics in this panel vary depending on your chosen messaging channel, and whether or not you are running a multivariate test. You can click on the <i class="fa fa-eye preview-icon"></i> **Preview** icon to view your message for each variant or channel.

![SMS/MMS Performance panel that includes a table of metrics for a control group, Variant 1, and Variant 2.]({% image_buster /assets/img_archive/sms_message_performance.png %})

{% elsif include.channel == "webhook" %}
### Webhook Performance

The **Webhook Performance** panel outlines how well your message has performed across various dimensions. The metrics in this panel vary depending on your chosen messaging channel, and whether or not you are running a multivariate test. You can click on the <i class="fa fa-eye preview-icon"></i> **Preview** icon to view your message for each variant or channel.

![Webhook performance panel that includes a table of metrics for a control group and Variant 1.]({% image_buster /assets/img/webhook_message_performance.png %})

{% elsif include.channel == "whatsapp" %}
### WhatsApp Performance

The **WhatsApp Performance** panel outlines how well your message has performed across various dimensions. The metrics in this panel vary depending on your chosen messaging channel, and whether or not you are running a multivariate test. You can click on the <i class="fa fa-eye preview-icon"></i> **Preview** icon to view your message for each variant or channel.

![WhatsApp performance panel that includes a table of metrics for Variant 1.]({% image_buster /assets/img/whatsapp_message_performance.png %})

{% endif %}

If you want to simplify your view, click <i class="fas fa-plus"></i> **Add/Remove Columns** and clear any metrics as desired. By default, all metrics are displayed.

{% if include.channel == "email" %}

#### Heatmaps

Using heatmaps, you can see how successful different links in a single email campaign. From the **Message Analytics** section, go to the **Email Performance** panel. Click **Preview & Heatmap** to view a preview of your email campaign and the heatmap. Alternatively, you can click the hyperlink in the variant name to view the heatmap.

In this view, you can use the **Show Heatmap** toggle to bring up a visual view of your email that shows the overall frequency and location of clicks within the lifespan of the campaign. In the **Link Table by Total Clicks** panel, you can view all of the links in your email campaign and sort by total clicks. This can provide additional insight on where your users navigate. To save a copy of the heatmap for reference, click the download button.

![Example of the Preview and Heatmap page that includes an email campaign, and a panel with link alias examples with their total clicks.]({% image_buster /assets/img_archive/email_heatmap_example.png %})

{% endif %}

{% if include.channel == "Content Card" %}

#### Content Card metrics

Here is a breakdown of some key metrics you may see while reviewing your message performance. For the definitions of all Content Cards metrics, refer to the [Report Metrics Glossary][1] and filter by Content Cards.

| Term | Definition |
| -- | -- |
| Messages Sent | This is calculated differently depending on what you selected for [Card creation]({{site.baseurl}}/user_guide/message_building_by_channel/content_cards/create/card_creation/#differences-between-creating-cards-at-launch-or-entry-versus-at-first-impression):<br><br>  {::nomarkdown}<ul><li><b>At launch or step entry:</b> The number of cards created and available to be seen. This doesn't count whether the users viewed the card.</li><li><b>At first impression:</b> The number of cards displayed to users.</li></ul>{:/} |
| Total Impressions | The total count of impressions logged for a given Content Card. This can increment multiple times for the same user. |
| Unique Impressions | The number of users who have viewed a given card. This count doesn't increment the second time that a user views a card. |
| Unique Recipients | The total number of viewers (unique, but only unique per day) that have viewed the particular card. Because a viewer can be a unique recipient every day, you should expect this to be higher than Unique Impressions. |
| Unique Clicks | The number of recipients who have clicked the CTA link of a Content Card at least once—excluding clicks on Braze-provided unsubscribe links. |
Unique Dismissals | The number of users who have dismissed Content Cards from a campaign. A user dismissing a Content Card from a campaign multiple times represents one unique dismissal. |
{: .reset-td-br-1 .reset-td-br-2}

{% alert note %}
Regarding how impressions are logged, there are some nuances between web, Android, and iOS. Generally speaking, Braze logs an impression when a card is seen, which is after a user scrolls to the specific Content Card in their feed.
{% endalert %}

#### Unique Recipients versus Unique Impressions

There are a few metrics available that cover the visibility of your message. This includes Messages Sent, Unique Recipients, and Unique Impressions. In particular, the difference between Unique Recipients and Unique Impressions can be a bit confusing. Let's use a few example scenarios to understand these metrics better.

Let's say you view a Content Card today, then view the same card tomorrow, and again the day after tomorrow—you will be counted as a Unique Recipient three times. However, you will only be counted for one Unique Impression. You'll also be included in the number of Messages Sent, as the card was available on your device.

As another example, suppose you see five Unique Impressions on a Content Card campaign showing 150,000 Messages Sent. This means the card was made available (on the backend) to an audience of 150,000 users, but only five users' devices performed all of the following steps after that send occurred:

1. Started a session or the app explicitly requested a Content Cards sync (or both)
2. Navigated to the Content Cards view
3. SDK recorded an impression and logged it to the server

Your Messages Sent refers to Content Cards available to be seen, while Unique Recipients refers to Content Cards that were actually seen.

{% elsif include.channel == "email" %}

#### Email metrics

Here are some key email-specific metrics that you won't see in other channels. To see the definitions of all email metrics used in Braze, refer to our [Email Analytics Glossary]({{site.baseurl}}/user_guide/message_building_by_channel/email/reporting_and_analytics/analytics_glossary/).

| Term | Definition |
| --- | --- |
| Spam | The percentage of users that marked your email as spam, or the email was designated as spam. If this metric is greater than 0.08, that could be a sign that either your message copy is too salesy or you should reconsider your email address collection methods (to confirm you're messaging those who are interested in your correspondence). |
| Unique opens | The percentage of recipients that opened your email. This can also include emails that are machine opened. This number should be between 10–20%. Anything greater than 20% is exceptional! |
| Unique clicks | The percentage of recipients that clicked within the email sent. This number should be between 5–10%. Anything greater than 10% is exceptional! |
| Click to open | The percentage of recipients that opened your email and then clicked on it. |
| Estimated real opens  | This is an estimate of how many unique opens there would be if machine opens did not exist. This is the result of a proprietary Braze statistical model. See the following section for details. |
| Machine opens | Includes the proportion of “opens” that are affected by Apple's Mail Privacy Protection (MPP) for iOS 15. <br>For example, if a user opens an email using the Mail app on an Apple device, this will be logged as a "Machine Opens". This metric is tracked starting November 11, 2021 for Sendgrid and December 2, 2021 for SparkPost. |
| Other opens | Includes emails that haven't been identified as "Machine opens". <br>For example, when a user opens an email on another platform (such as Gmail app on a phone, Gmail on desktop browser), this will be logged as an "Other opens". Note that a user can also open an email (such as the open counts toward "Other opens") before a "Machine open" count is logged. If a user opens an email once (or more) after a machine open event from a non-Apple Mail inbox, then the amount of times that the user opens the email is calculated towards “Other Opens” and only once towards “Unique Opens”. |
| Unsubs | The percentage of recipients that clicked the "Unsubscribe" link in your email. |
{: .reset-td-br-1 .reset-td-br-2}

##### Estimated real open rate {#estimated-real-open-rate}

This statistic uses a proprietary analytical model created by Braze to reconstruct an estimate of the campaign's unique open rate as if machine opens did not exist. While we receive labels of "Machine Opens" on some open events from email senders (see above), these labels can often label actual opens as real opens. In other words, the "Other Opens" are likely an underestimate of real opens (by actual users). Instead, Braze uses click data from each campaign to infer the rate at which actual humans opened the message. This compensates for various machine opening mechanisms, including Apple’s MPP.

The displayed statistic is generated 36 hours after email sending has begun. It will only run for scheduled email campaigns (one-time or recurring). If a campaign recurs, the estimate will be recalculated 36 hours after another send occurs.

###### Limitations

- Estimated Real Open Rate is being gradually rolled out and may not appear in your campaign analytics just yet.
- Additionally, Estimated Real Open Rate is:
   - Only available in campaigns
   - Not reported in Current events
   - Not retroactively calculated for past campaigns

{% elsif include.channel == "in-app message" %}

#### In-app message metrics

Here are some key in-app message metrics you may see in your analytics. To see the definitions of all in-app message metrics used in Braze, refer to our [Report Metrics Glossary][1].

| Term                   | Definition                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------|
| Body clicks*           | Occurs when a user clicks on the message itself and not one of the buttons. This only applies to messages created with the traditional editor. |
| Button 1 and Button 2 clicks | The percentage of recipients that pressed that specific button.                                                |
| Unique impressions     | The total number of people who actually received and viewed the in-app message. If a user receives the message twice within 24 hours, only one impression is counted that day. <br><br> **If re-eligibility is on:** {::nomarkdown}<ul><li>Unique impressions can be incremented again after 24 hours if re-eligibility is on and a user performs the trigger action again.</li><li>For in-app messages, *Unique Impressions* = *Unique Recipients* since impressions and recipients both increment after 24 hours.</li></ul>{:/} |
| Total Impressions            | The number of users whose devices reported that the message had been delivered. If a user receives the message twice, they are counted twice. <br><br> **If there are multiple devices:** {::nomarkdown}<ul><li>If re-eligibility is off, the user should only see the in-app message once. Even if the user uses multiple devices, they will only see it on the first device that is targeted. This assumes that the profile has consolidated devices and a user has one user ID that they are logged into across devices. </li></ul>{:/} **If re-eligibility is on:** {::nomarkdown}<ul><li>An impression is logged for every time that user sees the in-app message.</li></ul>{:/} |
| Conversion             | Conversion tracking starts once a user logs an impression of an in-app message. A conversion is counted if the user has received and viewed the in-app message campaign, and subsequently performs the specific conversion event within the defined conversion window, regardless of whether they clicked on the message or not. <br><br> Conversions are attributed to the most recently received message. If re-eligibility is enabled, the conversion will be assigned to the latest in-app message received, provided that it occurs within the defined conversion window. However, if the in-app message has already been assigned a conversion, then the new conversion cannot be logged for that specific message. This ensures that each in-app message delivery is associated with only one conversion. |
| Total Conversions      | When a user views an in-app message campaign only once, only one conversion is counted, even if they perform the conversion event multiple times later on. However, if re-eligibility is turned on and the user sees the in-app message campaign multiple times, *Total Conversions* can increase once for each time the user logs an impression for a new instance of the in-app message campaign. <br><br> For example, if a user triggers an in-app message twice and converts after each in-app message impression (resulting in two conversions), then *Total Conversions* will increase by two. However, if there was only one in-app message impression followed by two conversion events, only one conversion will be logged, and *Total Conversions* will increase by one. |
| Conversion Rate        | The metric of total daily unique impressions (*Unique Impressions*) is used to calculate the conversion rate. <br><br> Conversion Rate = (Primary Conversions) / (Unique Impressions) <br><br> Impressions for in-app messages can only be counted once per day. On the other hand, the number of times a user completes a desired action (a "conversion") can increase within a 24-hour period. While conversions can happen more than once per day, impressions cannot. Therefore, if a user completes a conversion multiple times within a day, the Conversion Rate can increase accordingly, but impressions will only be counted once. |
{: .reset-td-br-1 .reset-td-br-2}

{% alert note %}
*Body clicks are not automatically collected for in-app messages created with the Drag-and-Drop Editor and the Custom Code Editor. For more details, refer to the SDK changelogs for [iOS]({{site.baseurl}}/developer_guide/platform_integration_guides/ios/changelog/objc_changelog#3310) and [Android]({{site.baseurl}}/developer_guide/platform_integration_guides/android/changelog#1100).
{% endalert %}

{% elsif include.channel == "push" %}

#### Push metrics

Here is a breakdown of some key metrics you may see while reviewing your message performance. For the definitions of all push metrics, refer to the [Report Metrics Glossary][1] and filter by push.

| Term | Description |
| --------- | --- |
| Bounces | The push notifications sent to these users were undeliverable. These users have been automatically unsubscribed from all future push notifications. See [Bounced push notifications](#bounced-push). |
| Direct Opens | Instances in which a user opened your app by interacting directly with a push notification. |
| Opens | Instances including both Direct Opens and Influenced Opens in which the Braze SDK has determined, using a proprietary algorithm, that a push notification has caused a user to open the app. |
{: .reset-td-br-1 .reset-td-br-2}

{% alert tip %}
Even though _Direct Opens_ and _Influenced Opens_ include the word "opens", they're actually different metrics. _Direct Opens_ refers to the direct opening of a push notification, as stated in the table above. _Influenced Opens_ refers to the opening of an app, without opening a push notification within a specific timeframe after receiving it. So, _Influenced Opens_ refers to the app opens, not push notification opens.
{% endalert %}

> Delivery of notifications is a “best effort” by APNs. It is not intended to deliver data to your app, only to notify the user that there is new data available. The important distinction is that we will display how many messages we successfully delivered to APNs, not necessarily how many APNs successfully delivered to devices.

#### Bounced push notifications {#bounced-push}

##### Apple push notification service

Bounces occur in the APNs when a push notification attempts delivery to a device that does not have the intended app installed. APNs also has the right to change tokens for devices arbitrarily. If you attempt to send to a user’s device in which their push token has changed in between when we previously registered their token (such as at the beginning of each session when we register a user for a push token) and the time of send, this would cause a bounce.

If a user disables push within their device settings on subsequent app open the SDK will detect that push has been disabled and notify Braze. At this point we will update the push enabled state to be disabled. When a disabled user receives a push campaign before having a new session, the campaign would successfully send and appear as delivered. The push will not bounce for this user. Following a subsequent session, when you attempt to send a push to the user Braze is already aware of whether we have a foreground token as such no notification is sent.

Push notifications that expire before delivery are not considered as failed and will not be recorded as a bounce.

##### Firebase Cloud Messaging

Firebase Cloud Messaging (FCM) bounces could occur in three cases:

| Scenario | Description |
| -- | -- |
| Uninstalled applications | When a message attempts delivery to a device and the intended app is uninstalled on that device, the message will be discarded and the device's registration ID will be invalidated. Any future attempts at messaging the device will return a NotRegistered error. |
| Backed up application | When an application is backed up, its registration ID could become invalid before the application is restored. In this case, FCM will no longer store the application's registration ID and the application will no longer receive messages. As such, registration IDs should _not_ be saved when an application is backed up. |
| Updated application | When an application is updated, the previous version's registration ID may no longer work. As such, an updated application should replace its existing registration ID. |
{: .reset-td-br-1 .reset-td-br-2}

{% elsif include.channel == "SMS" %}

#### SMS metrics

Here is a breakdown of some key metrics you may see while reviewing your message performance. For the definitions of all SMS metrics, refer to the [Report Metrics Glossary][1] and filter by SMS.

| Term | Definition |
| -- | -- |
| Sent | A campaign or Canvas step has been launched or triggered, and an SMS has been sent from Braze. It is possible that the SMS does not reach a user's device due to errors, as explained below.
| Sent to Carrier | Braze has attempted to send the SMS through to the carriers. This stat is the sum of Confirmed Deliveries, Rejections, and sends where the carrier did not confirm delivery or rejection. There are instances where carriers do not provide delivery or rejected confirmation, as some carriers do not provide this confirmation or were unable to do so at the time of sending. Note that this metric does not exist for all Braze mobile aggregators. |
| Delivery Failures | Messages that were not attempted to be sent due to a failed outcome within aggregator logs. This could be due to queue overflow or invalid recipient number, depending on the associated aggregator error code. Please reach out to Braze [support]({{site.baseurl}}/braze_support/) for assistance in understanding the reasons for delivery failures.
| Confirmed Delivery | The carrier has confirmed that the SMS was delivered to the target phone number. As a Braze customer, deliveries are charged toward your SMS allotment.
| Rejections | The SMS has been rejected by the carrier. This can happen for several reasons, including carrier content filtering, availability of the destination device, the phone number is no longer in service, etc. As a Braze customer, rejections are charged toward your SMS allotment.
| Opt-Out | A user replied to your message with an [Opt-Out Keyword]({{site.baseurl}}/user_guide/message_building_by_channel/sms/keywords/keyword_handling/#default-opt-in-opt-out-keywords) and was unsubscribed from your SMS program. A user reply is measured anytime a user sends an inbound message within four hours of receiving your message.
| Help | A user replied to your message with a [HELP Keyword]({{site.baseurl}}/user_guide/message_building_by_channel/sms/keywords/keyword_handling/#default-opt-in-opt-out-keywords) and was dispatched a HELP auto-response. A user reply is measured anytime a user sends an inbound message within four hours of receiving your message.
{: .reset-td-br-1 .reset-td-br-2}

{% elsif include.channel == "webhook" %}

#### Webhook metrics

Here are some key webhook metrics you may see in your analytics. To see the definitions of all webhook metrics used in Braze, refer to our [Report Metrics Glossary][1].

| Term | Definition |
| --- | --- |
| Unique Recipients | The total number of users (unique, but only unique per day) that have received the particular webhook. 
| Sends | Sends (and Messages Sent) include all attempted sends, successful and unsuccessful. This metric counts when a webhook was processed and sent to the third party specified in that webhook, and does not signify whether or not the request was received. |
| Errors | The total number of sends that were not successful. Errors are included in the _Sends_ count but are not included in the _Unique Recipients_ count.
{: .reset-td-br-1 .reset-td-br-2}

{% elsif include.channel == "whatsapp" %}

#### WhatsApp metrics

Here are some key WhatsApp metrics you may see in your analytics. To see the definitions of all WhatsApp metrics used in Braze, refer to our [Report Metrics Glossary][1].

| Term | Definition |
| --- | --- |
| Sends | The total number of sends successfully communicated between Braze and WhatsApp. However, this does not necessarily mean the message was received by the end user. |
| Deliveries | The total number of WhatsApp messages sent that successfully made it to the end user's device. |
| Reads | When a WhatsApp message is read by the end user. The end user's read receipts must be “On” for Braze to track reads. |
| Failures | The total number of sends that were not successful because the Internet Service Provider returned a hard bounce. A hard bounce signifies a permanent deliverability failure. Failures are included in the _Sends_ count but are not included in the _Deliveries_ count.
{: .reset-td-br-1 .reset-td-br-2}

#### End-user blocking and reporting metrics
Additional metrics may be accessed via the [WhatsApp Manager dashboard](https://www.facebook.com/business/help/683499390267496?content_id=NZUBj7XjkYjYuWx), though [confirmation of your access](https://www.facebook.com/business/help/218116047387456) is necessary to access all available insights. 

{% endif %}

### Historical Performance

The **Historical Performance** panel allows you to view the metrics from the **Message Performance** panel as a graph over time. Use the filters at the top of the panel to modify the stats and channels shown in the graph. The time range of this graph will always mirror the time range specified at the top of the page. 

To get a day-by-day breakdown, click the <i class="fas fa-bars"></i> hamburger menu and select **Download CSV** to receive a CSV export of the report.

![A graph of the Historical Performance panel with example statistics for an email from February 2021 to May 2022.]({% image_buster /assets/img/cc-historical-performance.png %})

{% if include.channel == "in-app message" %}

{% alert note %}
If you select to only send to users who can see the latest Braze version of in-app messages (Generation 3), your **Target Audience** does not adjust to reflect your choice.
{% endalert %}

{% endif %}

{% if include.channel == "SMS" %}

### Keyword Responses

The **Keyword Responses** panel shows you a timeline of the inbound keywords users replied with after receiving your message.  

![Campaign Level SMS/MMS Keyword Responses panel that includes a line graph of keyword distribution over time, and a Keywords Categories section with selected checkboxes for Opt-In, Opt-Out, Help, Other, More, and Coaching.]({% image_buster /assets/img/sms/keyword_responses.png %})

Here, you can also view the response distribution of each keyword category to determine next steps for [retargeting]({{site.baseurl}}/user_guide/engagement_tools/campaigns/ideas_and_strategies/retargeting_campaigns) and to conveniently [create a segment]({{site.baseurl}}/user_guide/engagement_tools/segments/creating_a_segment).

![The table below the line graph that has columns for Keyword Category, Response Distribution, and Retargeting, where you are given the option to create a segment with the keyword category.]({% image_buster /assets/img/sms/keyword_segments.png %})

{% endif %}

### Conversion Event Details

The **Conversion Event Details** panel shows you the performance of your conversion events for your campaign. For more information, refer to [Conversion Events]({{site.baseurl}}/user_guide/engagement_tools/campaigns/building_campaigns/conversion_events/#step-3-view-results).

![The Conversion Event Details panel.]({% image_buster /assets/img/cc-conversion.png %})

### Conversion Correlation

The **Conversion Correlation** panel gives you insight into what user attributes and behaviors help or hurt the outcomes you set for campaigns. For more information, refer to [Conversion Correlation]({{site.baseurl}}/user_guide/engagement_tools/testing/conversion_correlation/).

![The Conversion Correlation panel with an analysis on user attributes and behavior from the Primary Conversion Event - A.]({% image_buster /assets/img/convcorr.png %})

{% if include.channel == "SMS" %}

### SMS Currents events

Like email, Braze receives user-level events related to an SMS message as it makes its journey to a user. Any inbound SMS event will also be sent as a Currents event through the [SMS InboundReceived]({{site.baseurl}}/user_guide/data_and_analytics/braze_currents/event_glossary/message_engagement_events/#sms-inbound-received-events) event. This will allow you to perform additional actions or reporting on the messages your users are texting in outside of the Braze platform. 

{% alert note %}
Inbound messages are truncated past 1600 characters.
{% endalert %}

{% endif %}

{% if include.channel != "whatsapp" %}

## Retention Report

Retention reports show you the rates at which your users have performed a selected retention event over time periods in a specific campaign or Canvas. For more information, refer to [Retention Reports]({{site.baseurl}}/user_guide/data_and_analytics/reporting/retention_reports/).

## Funnel Report

Funnel reporting offers a visual report that allows you to analyze the journeys your customers take after receiving a campaign or Canvas. If your campaign or Canvas uses a control group or multiple variants, you will be able to understand how the different variants have impacted the conversion funnel at a more granular level and optimize based on this data.

For more information, refer to [Funnel Reports]({{site.baseurl}}/user_guide/data_and_analytics/reporting/funnel_reports/).

{% endif %}

[1]: {{site.baseurl}}/user_guide/data_and_analytics/report_metrics/
[2]: {{site.baseurl}}/user_guide/intelligence/multivariate_testing/#step-4-choose-a-segment-and-distribute-your-users-across-variants

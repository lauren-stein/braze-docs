---
nav_title: Overview
article_title: Overview
description: "This reference article will cover how to use Braze Audience Sync to Facebook, to deliver advertisements based upon behavioral triggers, segmentation, and more."
page_order: 0
Tool:
  - Canvas

---

# Audience sync overview

> The Braze Audience Sync feature helps you extend the reach of your campaigns to many of the top social and advertising technologies. Through [Braze Canvas]({{site.baseurl}}/user_guide/engagement_tools/canvas), brands can dynamically and securely sync first-party user data into the advertising ecosystem to drive marketing and operational efficiencies.

## Use cases

- Targeting high-value users via owned and paid channels to drive incremental purchases or engagement.
- Creating lookalike audiences of your high-value users to optimize new user acquisition costs and conversions.
- Retargeting users with ads who are less responsive to other marketing channels.
- Creating suppression audiences to prevent users from receiving advertisements when they’re already loyal consumers of your brand.

## How it works

To get started, add an Audience Sync step within your Canvas journey. 

![][18]{: style="max-width:35%;"} ![][20]{: style="max-width:28%;"}

Next, select one or multiple Audience Sync destinations to sync to. 

![][19]{: style="max-width:80%;"}

After selecting a destination, you must configure each partner with the appropriate ad account, audience, and user fields to match, along with specifying whether to add or remove users from the audience. 

![][21]

Keep in mind that Braze will sync users as soon as they enter the Audience Sync step within your Canvas. 

For each Audience Sync destination, the partner may have different requirements for which fields we can send. Refer to the specific partner documentation for more details. 

## Data privacy considerations

When building audiences for Ad Tracking, you may wish to include or exclude certain users based on their preferences, and to comply with privacy laws, such as the “Do Not Sell or Share” right under the [CCPA](https://oag.ca.gov/privacy/ccpa). Marketers should implement the relevant filters for users’ eligibility within their Canvas entry criteria. Below we list some options.

If you have collected the [iOS IDFA through the Braze SDK]({{site.baseurl}}/developer_guide/platform_integration_guides/ios/initial_sdk_setup/other_sdk_customizations/#optional-idfa-collection), you will be able to use the "Ads Tracking Enabled" filter. Select the value as `true` to only send users into Audience Sync destinations where they have opted in.

![][2]

If you are collecting `opt-ins`, `opt-outs`, `Do Not Sell Or Share`, or any other relevant custom attributes, you should include these within your Canvas entry criteria as a filter:

![A Canvas with an entry audience of "opted_in_marketing" equals "true".][1]

To learn more on how to comply with these Data Protection laws within the Braze platform, see [Data Protection Technical Assistance]({{site.baseurl}}/dp-technical-assistance/).

[1]: {% image_buster /assets/img/audience_sync/audience_sync.png %}
[2]: {% image_buster /assets/img/audience_sync/audience_sync2.png %}
[18]: {% image_buster /assets/img/audience_sync/audience_sync3.png %}
[19]: {% image_buster /assets/img/audience_sync/audience_sync4.png %}
[20]: {% image_buster /assets/img/audience_sync/audience_sync5.png %}
[21]: {% image_buster /assets/img/audience_sync/audience_sync6.png %}

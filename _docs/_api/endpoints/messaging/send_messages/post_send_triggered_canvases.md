---
nav_title: "POST: Send Canvas Messages via API-Triggered Delivery"
article_title: "POST: Send Canvas Messages via API-Triggered Delivery"
search_tag: Endpoint
page_order: 4
layout: api_page
page_type: reference
description: "This article outlines details about the Send Canvases via API-triggered delivery Braze endpoint."

---
{% api %}
# Send Canvas messages via API-triggered delivery
{% apimethod post core_endpoint|https://www.braze.com/docs/core_endpoints %} 
/canvas/trigger/send
{% endapimethod %}

> Use this endpoint to send Canvas messages via API-triggered delivery. 

API-triggered Delivery allows you to store message content in the Braze dashboard while dictating when a message is sent, and to whom via your API.

Note that to send messages with this endpoint, you must have a [Canvas ID]({{site.baseurl}}/api/identifier_types/#canvas-api-identifier), created when you build a Canvas.

{% apiref postman %}https://documenter.getpostman.com/view/4689407/SVYrsdsG?version=latest#c9a8a5fe-a101-4755-99f2-73aa8fc146fe {% endapiref %}

{% alert note %}
To use this endpoint, you'll need to generate an API key with the `canvas.trigger.send` permission.
{% endalert %}

## Rate limit

{% multi_lang_include rate_limits.md endpoint='send endpoints' category='message endpoints' %}

## Request body

```
Content-Type: application/json
Authorization: Bearer YOUR-REST-API-KEY
```

```json
{
  "canvas_id": (required, string) see Canvas identifier,
  "canvas_entry_properties": (optional, object) personalization key-value pairs that will apply to all users in this request,
  "broadcast": (optional, boolean) see Broadcast -- defaults to false on 8/31/17, must be set to true if `recipients` is omitted,
  "audience": (optional, connected audience object) see connected audience,
  // Including 'audience' will only send to users in the audience
  "recipients": (optional, array; if not provided and broadcast is not set to 'false', message will send to the entire segment targeted by the Canvas)
    [{
      // Either "external_user_id" or "user_alias" is required. Requests must specify only one.
      "user_alias": (optional, user alias object) user alias of user to receive message,
      "external_user_id": (optional, string) external identifier of user to receive message,
      "canvas_entry_properties": (optional, object) personalization key-value pairs that will apply to this user (these key-value pairs will override any keys that conflict with the parent `canvas_entry_properties`)
      "send_to_existing_only": (optional, boolean) defaults to true, can't be used with user aliases
      "attributes": (optional, object) fields in the attributes object will create or update an attribute of that name with the given value on the specified user profile before the message is sent and existing values will be overwritten
    }],
    ...
}
```

## Request parameters

| Parameter | Required | Data Type | Description |
| --------- | ---------| --------- | ----------- |
|`canvas_id`| Required | String | See [Canvas identifier]({{site.baseurl}}/api/identifier_types/). |
|`canvas_entry_properties`| Optional | Object | See [Canvas entry properties]({{site.baseurl}}/api/objects_filters/canvas_entry_properties_object/). Personalization key-value pairs that will apply to all users in this request. The Canvas entry properties object has a maximum size limit of 50 KB. |
|`broadcast`| Optional | Boolean | You must set `broadcast` to true when sending a message to an entire segment that a campaign or Canvas targets. This parameter defaults to false (as of August 31, 2017). <br><br> If `broadcast` is set to true, a `recipients` list cannot be included. However, use caution when setting `broadcast: true`, as unintentionally setting this flag may cause you to send your message to a larger than expected audience. |
|`audience`| Optional| Connected audience object | See [Connected audience]({{site.baseurl}}/api/objects_filters/connected_audience/). |
|`recipients`| Optional | Array | See [Recipients object]({{site.baseurl}}/api/objects_filters/recipient_object/). If not provided and `broadcast` is set to true, the message will send to the entire segment targeted by the Canvas.<br><br> The `recipients` array may contain up to 50 objects, with each object containing a single `external_user_id` string and `canvas_entry_properties` object. Either `external_user_id` or `user_alias` is required for this call. Requests must specify only one. <br><br> When `send_to_existing_only` is `true`, Braze will only send the message to existing users—however this flag can't be used with user aliases. When `send_to_existing_only` is `false` and a user with the given `id` does not exist, Braze will create a user with that ID and attributes before sending the message.|
{: .reset-td-br-1 .reset-td-br-2 .reset-td-br-3  .reset-td-br-4}

Customers using the API for server-to-server calls may need to allowlist the appropriate API URL if they're behind a firewall.

{% alert note %}
If you include both specific users in your API call and a target segment in the dashboard, the message will send to specifically the user profiles that are both in the API call and qualify for the segment filters.
{% endalert %}

## Example request
```
curl --location --request POST 'https://rest.iad-01.braze.com/canvas/trigger/send' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer YOUR-REST-API-KEY' \
--data-raw '{
  "canvas_id": "canvas_identifier",
  "canvas_entry_properties": {"product_name" : "shoes", "product_price" : 79.99},
  "broadcast": false,
  "audience": {
    "AND": [
      {
        "custom_attribute": {
          "custom_attribute_name": "eye_color",
          "comparison": "equals",
          "value": "blue"
        }
      },
      {
        "custom_attribute": {
          "custom_attribute_name": "favorite_foods",
          "comparison": "includes_value",
          "value": "pizza"
        }
      },
      {
        "OR": [
          {
            "custom_attribute": {
              "custom_attribute_name": "last_purchase_time",
              "comparison": "less_than_x_days_ago",
              "value": 2
            }
          },
          {
            "push_subscription_status": {
              "comparison": "is",
              "value": "opted_in"
            }
          }
        ]
      },
      {
        "email_subscription_status": {
          "comparison": "is_not",
          "value": "subscribed"
        }
      },
      {
        "last_used_app": {
          "comparison": "after",
          "value": "2019-07-22T13:17:55+0000"
        }
      }
    ]
  },
  "recipients": [
    {
      "user_alias": {
        "alias_name" : "example_name",
        "alias_label" : "example_label"
      },
      "external_user_id": "user_identifier",
      "trigger_properties": "",
      "canvas_entry_properties": "",
      "send_to_existing_only": true,
      "attributes": {
          "first_name" : "Alex"
      }
    }
  ]
}'
```

## Response details

Message sending endpoint responses will include the message's `dispatch_id` for reference back to the dispatch of the message. The `dispatch_id` is the ID of the message dispatch (unique ID for each "transmission" sent from the Braze platform). Check out [Dispatch ID behavior]({{site.baseurl}}/help/help_articles/data/dispatch_id/) for more information.

## Create send endpoint

**Using the Attributes Object in Canvas**

Braze has a Messaging Object called `Attributes` that allows you to add, create, or update attributes and values for a user before sending them an API-Triggered Canvas using the `canvas/trigger/send` endpoint as this API call will process the User Attributes object before it processes and sends the Canvas. This helps minimize the risk of there being issues caused by [race conditions]({{site.baseurl}}/help/best_practices/race_conditions/).

{% alert important %}
Looking for the campaigns version of this endpoint? Check out [Sending campaign messages via API-triggered delivery]({{site.baseurl}}/api/endpoints/messaging/send_messages/post_send_triggered_campaigns/).
{% endalert %}

{% endapi %}


# Messaging Services

Call                                                      | Description
----------------------------------------------------------|---------------------------------
[TrollBox](#trollbox)                                     | View TrollBox chat.
[TrollBoxMsg](#trollboxmsg)                               | Send message to the TrollBox chat.
[TwilioSMSStatus](#twiliosmsstatus)                       | View delivery status information of any SMS sent.
[TwilioSendSMS](#twiliosendsms)                           | Send SMS message.





## TrollBox

View TrollBox chat.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '[]' https://api.maplenodes.com/v1/TrollBox
```

<code class="api-call">TrollBox</code>

This call does not take parameters.


### Response

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "date": "1585609790",
    "alias": "aderks",
    "message": "Welcome to Blocknet's XCloud TrollBox"
  },
  {
    "date": "1585610004",
    "alias": "aderks",
    "message": "Send messages through wallet console, CLI, or HTTP"
  },
  {
    "date": "1585610031",
    "alias": "aderks",
    "message": "Max message count is 200. When 200 hits, the oldest message will be removed as new messages come in."
  },
  {
    "date": "1585610052",
    "alias": "aderks",
    "message": "Alias can be whoever you want to be."
  },
  {
    "date": "1585610070",
    "alias": "aderks",
    "message": "Ensure you message is in quotations!"
  },
  {
    "date": "1585610084",
    "alias": "super_anon",
    "message": "Hi there"
  },
  {
    "date": "1585674897",
    "alias": "aderks",
    "message": "testing here"
  },
  {
    "date": "1585675488",
    "alias": "anon",
    "message": "hi there, how's it going"
  }
]
```


Parameter     | Type          | Description
--------------|---------------|-------------
timestamp     | string        | Timestamp of message.
alias         | string        | Username alias.
message       | string        | Message string.





## TrollBoxMsg

> Sample Data

```cli
{
  "alias": "anon",
  "message": "Hi there, testing things out!"
}
```
Send message to the TrollBox chat. View chat via [TrollBox](#trollbox). 



### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["anon","Hi there, testing things out!"]' https://api.maplenodes.com/v1/TrollBoxMsg
```

<code class="api-call">TrollBoxMsg [alias] ["message"]</code>

Parameter          | Type       | Description
-------------------|------------|-------------
alias              | string     | Username alias.
message            | string     | Message to send to the TrollBox chat.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "date": "1588727785",
  "alias": "anon",
  "message": "Hi there, testing things out!"
}
```


Parameter     | Type          | Description
--------------|---------------|-------------
timestamp     | string        | Timestamp of message.
alias         | string        | Username alias.
message       | string        | Message string.





## TwilioSMSStatus

> Sample Data

```cli
{
  "sms_id": "SM8f39577bd098429f853a48e6b898471f"
}
```
View delivery status information of any SMS sent.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["SM8f39577bd098429f853a48e6b898471f"]' https://api.maplenodes.com/v1/TwilioSMSStatus
```

<code class="api-call">TwilioSMSStatus [sms_id]</code>

Parameter          | Type       | Description
-------------------|------------|-------------
sms_id             | string     | Unique ID per SMS.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "sms_id": "SM8f39577bd098429f853a48e6b898471f",
    "date_created": "Sat, 15 Jun 2019 02:30:27 +0000",
    "date_updated": "Sat, 15 Jun 2019 02:30:28 +0000",
    "status": "delivered",
    "date_sent": "Sat, 15 Jun 2019 02:30:27 +0000"
  }
]
```


Parameter     | Type          | Description
--------------|---------------|-------------
sms_id        | string        | Unique ID per SMS.
date_created  | string        | Date timestamp of SMS creation.
date_updated  | string        | Date timestamp of last status update.
status        | string        | Status of outgoing message.
date_sent     | string        | Date timestamp of delivered SMS.





## TwilioSendSMS

> Sample Data

```cli
{
  "to_phone_number": "+15551234567",
  "message": "Hi there, testing things out!"
}
```
Send SMS message.

**Note:** Message body needs to be encased in double quotes.


### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["+15551234567","Hi there, testing things out!"]' https://api.maplenodes.com/v1/TwilioSendSMS
```

<code class="api-call">TwilioSendSMS [to_phone_number] ["message"]</code>

Parameter          | Type       | Description
-------------------|------------|-------------
to_phone_number    | string     | Phone number using “+” and country code in E.164 format.
message            | string     | Message body.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
[
  {
    "sms_id" : "SM8f39577bd098429f853a48e6b898471f",
    "date_created" : "Sat, 15 Jun 2019 02:30:27 +0000",
    "status" : "queued",
    "error_code" : null,
    "error_message" : null,
    "error_help" : null
  }
]
```


Parameter     | Type          | Description
--------------|---------------|-------------
sms_id        | string        | Unique ID per SMS.
date_created  | string        | Date timestamp of SMS creation.
status        | string        | Status of outgoing message.
error_code    | string        | Twilio error code.
error_message | string        | Error message.
error_help    | string        | URL for error resolution.

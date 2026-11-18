

# WebhookEvent

The `request.completed` webhook. Signed: `X-ScrapeBadger-Signature` is `sha256=` + hex HMAC-SHA256 of the raw body with the account's webhook secret (`GET /v1/account/webhook-secret`). Deliveries can repeat: deduplicate on `request_id`.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**event** | [**EventEnum**](#EventEnum) |  |  |
|**requestId** | **String** |  |  |
|**batchId** | **String** |  |  |
|**status** | **Integer** | The call&#39;s own HTTP status. |  |
|**headers** | **Map&lt;String, String&gt;** | The call&#39;s kept response headers, lower-case (content-type, x-credits-used, x-request-duration-ms, x-api-tier). |  |
|**resultUrl** | **String** |  |  |
|**resultExpiresAt** | **Integer** | Unix time. |  |
|**bodySize** | **Integer** |  |  |
|**body** | **Object** |  |  |
|**bodyOmitted** | **Boolean** | Present (true) when the body was over 1 MB: fetch &#x60;result_url&#x60;. |  [optional] |
|**attempt** | **Integer** |  |  |
|**sentAt** | **Integer** | Unix time of this attempt. |  |



## Enum: EventEnum

| Name | Value |
|---- | -----|
| REQUEST_COMPLETED | &quot;request.completed&quot; |




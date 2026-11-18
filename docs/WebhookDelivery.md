

# WebhookDelivery


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**requestId** | **String** |  |  |
|**endpoint** | **String** | Path of the call, e.g. &#x60;/v1/perplexity/ask&#x60; (never its query). |  |
|**state** | [**StateEnum**](#StateEnum) | &#x60;pending&#x60;: the call is still running. &#x60;delivering&#x60;: an attempt is under way or the next retry is due at &#x60;next_attempt_at&#x60;. &#x60;delivered&#x60;: the endpoint answered 2xx. &#x60;failed&#x60;: every attempt failed, a final status (not 408/429/5xx) came back, or a gateway restart interrupted the delivery (&#x60;last_error&#x60; \&quot;interrupted (gateway restart)\&quot;). |  |
|**attempts** | **Integer** |  |  |
|**lastStatus** | **Integer** |  |  [optional] |
|**lastError** | **String** |  |  [optional] |
|**createdAt** | **Integer** | Unix time the call was submitted. |  |
|**deliveredAt** | **Integer** |  |  [optional] |
|**callbackHost** | **String** |  |  |



## Enum: StateEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;pending&quot; |
| DELIVERING | &quot;delivering&quot; |
| DELIVERED | &quot;delivered&quot; |
| FAILED | &quot;failed&quot; |




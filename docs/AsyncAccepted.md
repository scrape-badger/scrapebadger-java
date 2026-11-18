

# AsyncAccepted

The call is still running. Poll `next_action.url` (free) until it answers with the call's own status and body; do not re-submit the call (that would run and bill it again).

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**requestId** | **String** |  |  |
|**status** | [**StatusEnum**](#StatusEnum) |  |  |
|**retryAfterSeconds** | **Integer** |  |  |
|**nextAction** | [**AsyncAcceptedNextAction**](AsyncAcceptedNextAction.md) |  |  |
|**detail** | **String** |  |  [optional] |
|**callback** | **Object** | Only on a poll of a call submitted with a callback: the delivery state so far (&#x60;status&#x60;, &#x60;attempts&#x60;, &#x60;last_error&#x60;). |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| RUNNING | &quot;running&quot; |




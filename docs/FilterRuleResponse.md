

# FilterRuleResponse

Filter rule response.  Per-poll billing — see ``GET /v1/twitter/filter-rules/pricing`` for the rates that apply globally to every rule.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** |  |  |
|**tag** | **String** |  |  |
|**query** | **String** |  |  |
|**intervalSeconds** | **BigDecimal** |  |  |
|**maxResultsPerPoll** | **Integer** |  |  |
|**status** | **String** |  |  |
|**statusReason** | **String** |  |  |
|**webhookUrl** | **String** |  |  |
|**webhookSecretSet** | **Boolean** |  |  |
|**totalCreditsBurned** | **BigDecimal** |  |  |
|**createdAt** | **OffsetDateTime** |  |  |
|**updatedAt** | **OffsetDateTime** |  |  |




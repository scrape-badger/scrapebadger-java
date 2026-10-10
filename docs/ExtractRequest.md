

# ExtractRequest


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**url** | **String** | The page to fetch. |  |
|**waitFor** | **String** |  |  [optional] |
|**country** | **String** |  |  [optional] |
|**proxyTier** | [**ProxyTierEnum**](#ProxyTierEnum) | Proxy pool: simple, premium or ultra. |  [optional] |
|**extractRules** | [**Map&lt;String, ExtractRequestExtractRulesValue&gt;**](ExtractRequestExtractRulesValue.md) |  |  [optional] |
|**aiExtractRules** | **Map&lt;String, String&gt;** |  |  [optional] |
|**aiQuery** | **String** |  |  [optional] |
|**renderJs** | **Boolean** | Render the page in a browser first. |  [optional] |



## Enum: ProxyTierEnum

| Name | Value |
|---- | -----|
| SIMPLE | &quot;simple&quot; |
| PREMIUM | &quot;premium&quot; |
| ULTRA | &quot;ultra&quot; |




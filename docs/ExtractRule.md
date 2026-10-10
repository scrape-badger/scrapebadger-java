

# ExtractRule


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**selector** | **String** | CSS or XPath selector. |  |
|**type** | [**TypeEnum**](#TypeEnum) |  |  [optional] |
|**all** | **Boolean** | Return every match as a list, not just the first. |  [optional] |
|**output** | [**OutputEnum**](#OutputEnum) | An element&#39;s text content, or its outer HTML. |  [optional] |



## Enum: TypeEnum

| Name | Value |
|---- | -----|
| CSS | &quot;css&quot; |
| XPATH | &quot;xpath&quot; |



## Enum: OutputEnum

| Name | Value |
|---- | -----|
| TEXT | &quot;text&quot; |
| HTML | &quot;html&quot; |




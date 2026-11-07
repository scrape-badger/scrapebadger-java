

# YelpSearchResponse


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**market** | **String** |  |  |
|**query** | **String** |  |  |
|**location** | **String** |  |  |
|**locationResolved** | **YelpResolvedLocation** |  |  |
|**didYouMean** | **String** |  |  [optional] |
|**queryMatched** | **Boolean** | False when Yelp could not place the query; results are then Yelp&#39;s broader ranking for the location, as Yelp shows them. |  |
|**totalResults** | **Integer** | Yelp&#39;s reported total; at most 110 are browsable. |  |
|**page** | **Integer** |  |  |
|**pageSize** | **Integer** |  |  |
|**totalPages** | **Integer** |  |  |
|**hasNextPage** | **Boolean** |  |  |
|**nextPage** | **Integer** |  |  [optional] |
|**results** | **List&lt;YelpBusiness&gt;** |  |  |
|**ads** | **List&lt;YelpBusiness&gt;** |  |  |
|**filters** | **Map&lt;String, YelpFilterGroup&gt;** |  |  |
|**relatedSearches** | **List&lt;YelpLink&gt;** |  |  |
|**sourceUrl** | **String** |  |  |
|**fetchedAt** | **String** |  |  |
|**fetchedUtc** | **BigDecimal** |  |  |




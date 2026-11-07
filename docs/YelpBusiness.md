

# YelpBusiness

A business card as ranked on the search page; nullable fields are absent from some cards.

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**position** | **Integer** | 1-based place in Yelp&#39;s organic order across pages (page 2 starts at 11): Yelp&#39;s own number where it numbers the results; services searches are unnumbered and keep Yelp&#39;s order. For ads, the slot order. |  |
|**isAd** | **Boolean** |  |  |
|**id** | **String** | Yelp encrypted business ID. |  |
|**alias** | **String** | Business slug used in /biz/&lt;alias&gt;. |  |
|**name** | **String** |  |  |
|**url** | **String** |  |  |
|**rating** | **BigDecimal** |  |  [optional] |
|**reviewCount** | **Integer** |  |  [optional] |
|**price** | **String** |  |  [optional] |
|**priceLevel** | **Integer** |  |  [optional] |
|**categories** | **List&lt;YelpCategory&gt;** |  |  [optional] |
|**neighborhoods** | **List&lt;String&gt;** |  |  [optional] |
|**address** | **String** |  |  [optional] |
|**city** | **String** |  |  [optional] |
|**phone** | **String** |  |  [optional] |
|**timezone** | **String** |  |  [optional] |
|**openingHours** | **List&lt;YelpHours&gt;** |  |  [optional] |
|**snippet** | **String** |  |  [optional] |
|**snippetType** | **String** |  |  [optional] |
|**highlights** | **List&lt;String&gt;** |  |  [optional] |
|**tags** | **List&lt;String&gt;** |  |  [optional] |
|**photos** | **List&lt;String&gt;** |  |  [optional] |
|**alternateNames** | **List&lt;String&gt;** |  |  [optional] |
|**isServiceAreaBusiness** | **Boolean** |  |  [optional] |
|**isYelpGuaranteed** | **Boolean** |  |  [optional] |
|**hasVerifiedLicense** | **Boolean** |  |  [optional] |
|**adPlacement** | **String** |  |  [optional] |




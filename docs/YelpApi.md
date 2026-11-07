# YelpApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**yelpListMarkets**](YelpApi.md#yelpListMarkets) | **GET** /v1/yelp/markets | List markets |
| [**yelpSearchBusinesses**](YelpApi.md#yelpSearchBusinesses) | **GET** /v1/yelp/search | Search businesses |


<a id="yelpListMarkets"></a>
# **yelpListMarkets**
> YelpMarketsResponse yelpListMarkets()

List markets

Yelp sites this API verifiably searches. Free.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YelpApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YelpApi apiInstance = new YelpApi(defaultClient);
    try {
      YelpMarketsResponse result = apiInstance.yelpListMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YelpApi#yelpListMarkets");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**YelpMarketsResponse**](YelpMarketsResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="yelpSearchBusinesses"></a>
# **yelpSearchBusinesses**
> YelpSearchResponse yelpSearchBusinesses(location, query, market, category, sortBy, price, features, page)

Search businesses

Ranked Yelp businesses for a location, with ads kept separate. 15 credits; empty results free.  Ten businesses per page, pages 1-11. Narrow the location, category or filters to reach more businesses. Business detail and reviews are not part of this API.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YelpApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YelpApi apiInstance = new YelpApi(defaultClient);
    String location = "location_example"; // String | Where to search, as typed into Yelp: city, neighbourhood, address or postcode.
    String query = "query_example"; // String | What to search for (e.g. pizza, plumbers). Optional when category is set.
    String market = "us"; // String | Yelp site to search; see /markets.
    String category = "category_example"; // String | Yelp category alias, e.g. pizza, coffee, plumbing.
    String sortBy = "recommended"; // String | 
    String price = "price_example"; // String | Comma-separated price levels 1-4 ($ to $$$$).
    String features = "features_example"; // String | Comma-separated refinements: delivery, takeout, reservations, outdoor_seating, good_for_kids, dogs_allowed, free_wifi, wheelchair_accessible.
    Integer page = 1; // Integer | 1-based page, ten businesses each; pages 1-11.
    try {
      YelpSearchResponse result = apiInstance.yelpSearchBusinesses(location, query, market, category, sortBy, price, features, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YelpApi#yelpSearchBusinesses");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **location** | **String**| Where to search, as typed into Yelp: city, neighbourhood, address or postcode. | |
| **query** | **String**| What to search for (e.g. pizza, plumbers). Optional when category is set. | [optional] |
| **market** | **String**| Yelp site to search; see /markets. | [optional] [default to us] [enum: us, ca] |
| **category** | **String**| Yelp category alias, e.g. pizza, coffee, plumbing. | [optional] |
| **sortBy** | **String**|  | [optional] [default to recommended] [enum: recommended, rating, review_count] |
| **price** | **String**| Comma-separated price levels 1-4 ($ to $$$$). | [optional] |
| **features** | **String**| Comma-separated refinements: delivery, takeout, reservations, outdoor_seating, good_for_kids, dogs_allowed, free_wifi, wheelchair_accessible. | [optional] |
| **page** | **Integer**| 1-based page, ten businesses each; pages 1-11. | [optional] [default to 1] |

### Return type

[**YelpSearchResponse**](YelpSearchResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |


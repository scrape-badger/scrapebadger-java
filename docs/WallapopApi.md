# WallapopApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**wallapopAutocomplete**](WallapopApi.md#wallapopAutocomplete) | **GET** /v1/wallapop/autocomplete | Autocomplete |
| [**wallapopGetListingDetail**](WallapopApi.md#wallapopGetListingDetail) | **GET** /v1/wallapop/items/{item_id} | Get listing detail |
| [**wallapopGetUserListings**](WallapopApi.md#wallapopGetUserListings) | **GET** /v1/wallapop/users/{user_id}/items | Get user listings |
| [**wallapopGetUserProfile**](WallapopApi.md#wallapopGetUserProfile) | **GET** /v1/wallapop/users/{user_id} | Get user profile |
| [**wallapopGetUserReviews**](WallapopApi.md#wallapopGetUserReviews) | **GET** /v1/wallapop/users/{user_id}/reviews | Get user reviews |
| [**wallapopListCategories**](WallapopApi.md#wallapopListCategories) | **GET** /v1/wallapop/categories | List categories |
| [**wallapopListFilterOptions**](WallapopApi.md#wallapopListFilterOptions) | **GET** /v1/wallapop/filters/{filter_id}/options | List filter options |
| [**wallapopListMarkets**](WallapopApi.md#wallapopListMarkets) | **GET** /v1/wallapop/markets | List markets |
| [**wallapopListSearchFilters**](WallapopApi.md#wallapopListSearchFilters) | **GET** /v1/wallapop/filters | List search filters |
| [**wallapopSearchListings**](WallapopApi.md#wallapopSearchListings) | **GET** /v1/wallapop/search | Search listings |
| [**wallapopWallapopScraperHealthCheck**](WallapopApi.md#wallapopWallapopScraperHealthCheck) | **GET** /v1/wallapop/health | Wallapop scraper health check |
| [**wallapopWallapopScraperHealthCheckHead**](WallapopApi.md#wallapopWallapopScraperHealthCheckHead) | **HEAD** /v1/wallapop/health | Wallapop scraper health check |


<a id="wallapopAutocomplete"></a>
# **wallapopAutocomplete**
> Object wallapopAutocomplete(query, market)

Autocomplete

Wallapop&#39;s search-box suggestions for a partial query.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WallapopApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WallapopApi apiInstance = new WallapopApi(defaultClient);
    String query = "query_example"; // String | Partial search text, e.g. 'bici'
    String market = "es"; // String | Market: es (Spain), it (Italy), pt (Portugal)
    try {
      Object result = apiInstance.wallapopAutocomplete(query, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WallapopApi#wallapopAutocomplete");
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
| **query** | **String**| Partial search text, e.g. &#39;bici&#39; | |
| **market** | **String**| Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to es] |

### Return type

**Object**

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

<a id="wallapopGetListingDetail"></a>
# **wallapopGetListingDetail**
> Object wallapopGetListingDetail(itemId, market)

Get listing detail

Full listing detail by id (e.g. nzxeknm5x562) or listing slug.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WallapopApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WallapopApi apiInstance = new WallapopApi(defaultClient);
    String itemId = "itemId_example"; // String | 
    String market = "es"; // String | Market: es (Spain), it (Italy), pt (Portugal)
    try {
      Object result = apiInstance.wallapopGetListingDetail(itemId, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WallapopApi#wallapopGetListingDetail");
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
| **itemId** | **String**|  | |
| **market** | **String**| Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to es] |

### Return type

**Object**

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

<a id="wallapopGetUserListings"></a>
# **wallapopGetUserListings**
> Object wallapopGetUserListings(userId, market, nextPage)

Get user listings

A seller&#39;s live listings, 40 per page.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WallapopApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WallapopApi apiInstance = new WallapopApi(defaultClient);
    String userId = "userId_example"; // String | 
    String market = "es"; // String | Market: es (Spain), it (Italy), pt (Portugal)
    String nextPage = "nextPage_example"; // String | Cursor from the previous page's next_page
    try {
      Object result = apiInstance.wallapopGetUserListings(userId, market, nextPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WallapopApi#wallapopGetUserListings");
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
| **userId** | **String**|  | |
| **market** | **String**| Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to es] |
| **nextPage** | **String**| Cursor from the previous page&#39;s next_page | [optional] |

### Return type

**Object**

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

<a id="wallapopGetUserProfile"></a>
# **wallapopGetUserProfile**
> Object wallapopGetUserProfile(userId, market)

Get user profile

Seller profile with ratings, sales counters, response rate and verifications.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WallapopApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WallapopApi apiInstance = new WallapopApi(defaultClient);
    String userId = "userId_example"; // String | 
    String market = "es"; // String | Market: es (Spain), it (Italy), pt (Portugal)
    try {
      Object result = apiInstance.wallapopGetUserProfile(userId, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WallapopApi#wallapopGetUserProfile");
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
| **userId** | **String**|  | |
| **market** | **String**| Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to es] |

### Return type

**Object**

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

<a id="wallapopGetUserReviews"></a>
# **wallapopGetUserReviews**
> Object wallapopGetUserReviews(userId, market, nextPage)

Get user reviews

Reviews a seller received, newest first, 40 per page.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WallapopApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WallapopApi apiInstance = new WallapopApi(defaultClient);
    String userId = "userId_example"; // String | 
    String market = "es"; // String | Market: es (Spain), it (Italy), pt (Portugal)
    String nextPage = "nextPage_example"; // String | Cursor from the previous page's next_page
    try {
      Object result = apiInstance.wallapopGetUserReviews(userId, market, nextPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WallapopApi#wallapopGetUserReviews");
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
| **userId** | **String**|  | |
| **market** | **String**| Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to es] |
| **nextPage** | **String**| Cursor from the previous page&#39;s next_page | [optional] |

### Return type

**Object**

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

<a id="wallapopListCategories"></a>
# **wallapopListCategories**
> Object wallapopListCategories(market)

List categories

The full category tree; ids are usable as the search category_id.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WallapopApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WallapopApi apiInstance = new WallapopApi(defaultClient);
    String market = "es"; // String | Market: es (Spain), it (Italy), pt (Portugal)
    try {
      Object result = apiInstance.wallapopListCategories(market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WallapopApi#wallapopListCategories");
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
| **market** | **String**| Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to es] |

### Return type

**Object**

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

<a id="wallapopListFilterOptions"></a>
# **wallapopListFilterOptions**
> Object wallapopListFilterOptions(filterId, categoryId, query, market)

List filter options

Long option lists (e.g. brand, model) for filters flagged options_endpoint.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WallapopApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WallapopApi apiInstance = new WallapopApi(defaultClient);
    String filterId = "filterId_example"; // String | 
    Integer categoryId = 56; // Integer | Category to scope options to
    String query = "query_example"; // String | Search text to scope options to
    String market = "es"; // String | Market: es (Spain), it (Italy), pt (Portugal)
    try {
      Object result = apiInstance.wallapopListFilterOptions(filterId, categoryId, query, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WallapopApi#wallapopListFilterOptions");
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
| **filterId** | **String**|  | |
| **categoryId** | **Integer**| Category to scope options to | [optional] |
| **query** | **String**| Search text to scope options to | [optional] |
| **market** | **String**| Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to es] |

### Return type

**Object**

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

<a id="wallapopListMarkets"></a>
# **wallapopListMarkets**
> Object wallapopListMarkets()

List markets

Supported Wallapop markets and their default search location.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WallapopApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WallapopApi apiInstance = new WallapopApi(defaultClient);
    try {
      Object result = apiInstance.wallapopListMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WallapopApi#wallapopListMarkets");
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

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="wallapopListSearchFilters"></a>
# **wallapopListSearchFilters**
> Object wallapopListSearchFilters(categoryId, query, market)

List search filters

The filters Wallapop offers for a category or query, with option ids.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WallapopApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WallapopApi apiInstance = new WallapopApi(defaultClient);
    Integer categoryId = 56; // Integer | Category the filters apply to
    String query = "query_example"; // String | Search text the filters apply to
    String market = "es"; // String | Market: es (Spain), it (Italy), pt (Portugal)
    try {
      Object result = apiInstance.wallapopListSearchFilters(categoryId, query, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WallapopApi#wallapopListSearchFilters");
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
| **categoryId** | **Integer**| Category the filters apply to | [optional] |
| **query** | **String**| Search text the filters apply to | [optional] |
| **market** | **String**| Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to es] |

### Return type

**Object**

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

<a id="wallapopSearchListings"></a>
# **wallapopSearchListings**
> Object wallapopSearchListings(query, market, latitude, longitude, distanceKm, categoryId, minPrice, maxPrice, condition, brand, model, color, timeFilter, shippable, hasWarranty, refurbished, minYear, maxYear, minKm, maxKm, gearbox, minHorsepower, maxHorsepower, orderBy, nextPage)

Search listings

Search Wallapop listings (40 per page). Needs a query, a category_id, or both.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WallapopApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WallapopApi apiInstance = new WallapopApi(defaultClient);
    String query = "query_example"; // String | Search text, e.g. 'iphone 14'
    String market = "es"; // String | Market: es (Spain), it (Italy), pt (Portugal)
    BigDecimal latitude = new BigDecimal(78); // BigDecimal | Search centre latitude (defaults to the market capital)
    BigDecimal longitude = new BigDecimal(78); // BigDecimal | Search centre longitude
    Integer distanceKm = 56; // Integer | Search radius
    Integer categoryId = 56; // Integer | Category id from /categories
    BigDecimal minPrice = new BigDecimal(78); // BigDecimal | Minimum price (EUR)
    BigDecimal maxPrice = new BigDecimal(78); // BigDecimal | Maximum price (EUR)
    String condition = "condition_example"; // String | Comma-separated: un_opened, in_box, new, as_good_as_new, good, fair, has_given_it_all
    String brand = "brand_example"; // String | Brand, e.g. Apple
    String model = "model_example"; // String | Model, e.g. iPhone 14
    String color = "color_example"; // String | Colour id, e.g. black
    String timeFilter = "today"; // String | Only listings published within this window
    Boolean shippable = false; // Boolean | Only listings that ship
    Boolean hasWarranty = false; // Boolean | Only listings with a warranty
    Boolean refurbished = false; // Boolean | Only refurbished listings
    Integer minYear = 56; // Integer | Cars: earliest model year
    Integer maxYear = 56; // Integer | Cars: latest model year
    Integer minKm = 56; // Integer | Cars: minimum mileage
    Integer maxKm = 56; // Integer | Cars: maximum mileage
    String gearbox = "manual"; // String | Cars
    Integer minHorsepower = 56; // Integer | Cars: minimum power
    Integer maxHorsepower = 56; // Integer | Cars: maximum power
    String orderBy = "most_relevance"; // String | Sort order
    String nextPage = "nextPage_example"; // String | Cursor from the previous page's next_page; other parameters are then ignored
    try {
      Object result = apiInstance.wallapopSearchListings(query, market, latitude, longitude, distanceKm, categoryId, minPrice, maxPrice, condition, brand, model, color, timeFilter, shippable, hasWarranty, refurbished, minYear, maxYear, minKm, maxKm, gearbox, minHorsepower, maxHorsepower, orderBy, nextPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WallapopApi#wallapopSearchListings");
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
| **query** | **String**| Search text, e.g. &#39;iphone 14&#39; | [optional] |
| **market** | **String**| Market: es (Spain), it (Italy), pt (Portugal) | [optional] [default to es] |
| **latitude** | **BigDecimal**| Search centre latitude (defaults to the market capital) | [optional] |
| **longitude** | **BigDecimal**| Search centre longitude | [optional] |
| **distanceKm** | **Integer**| Search radius | [optional] |
| **categoryId** | **Integer**| Category id from /categories | [optional] |
| **minPrice** | **BigDecimal**| Minimum price (EUR) | [optional] |
| **maxPrice** | **BigDecimal**| Maximum price (EUR) | [optional] |
| **condition** | **String**| Comma-separated: un_opened, in_box, new, as_good_as_new, good, fair, has_given_it_all | [optional] |
| **brand** | **String**| Brand, e.g. Apple | [optional] |
| **model** | **String**| Model, e.g. iPhone 14 | [optional] |
| **color** | **String**| Colour id, e.g. black | [optional] |
| **timeFilter** | **String**| Only listings published within this window | [optional] [enum: today, lastWeek, lastMonth] |
| **shippable** | **Boolean**| Only listings that ship | [optional] [default to false] |
| **hasWarranty** | **Boolean**| Only listings with a warranty | [optional] [default to false] |
| **refurbished** | **Boolean**| Only refurbished listings | [optional] [default to false] |
| **minYear** | **Integer**| Cars: earliest model year | [optional] |
| **maxYear** | **Integer**| Cars: latest model year | [optional] |
| **minKm** | **Integer**| Cars: minimum mileage | [optional] |
| **maxKm** | **Integer**| Cars: maximum mileage | [optional] |
| **gearbox** | **String**| Cars | [optional] [enum: manual, automatic] |
| **minHorsepower** | **Integer**| Cars: minimum power | [optional] |
| **maxHorsepower** | **Integer**| Cars: maximum power | [optional] |
| **orderBy** | **String**| Sort order | [optional] [default to most_relevance] [enum: most_relevance, newest, closest, price_low_to_high, price_high_to_low] |
| **nextPage** | **String**| Cursor from the previous page&#39;s next_page; other parameters are then ignored | [optional] |

### Return type

**Object**

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

<a id="wallapopWallapopScraperHealthCheck"></a>
# **wallapopWallapopScraperHealthCheck**
> Object wallapopWallapopScraperHealthCheck()

Wallapop scraper health check

Check health of the Wallapop scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WallapopApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WallapopApi apiInstance = new WallapopApi(defaultClient);
    try {
      Object result = apiInstance.wallapopWallapopScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WallapopApi#wallapopWallapopScraperHealthCheck");
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

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |

<a id="wallapopWallapopScraperHealthCheckHead"></a>
# **wallapopWallapopScraperHealthCheckHead**
> Object wallapopWallapopScraperHealthCheckHead()

Wallapop scraper health check

Check health of the Wallapop scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WallapopApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WallapopApi apiInstance = new WallapopApi(defaultClient);
    try {
      Object result = apiInstance.wallapopWallapopScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WallapopApi#wallapopWallapopScraperHealthCheckHead");
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

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |


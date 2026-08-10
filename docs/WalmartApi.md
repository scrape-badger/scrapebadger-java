# WalmartApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**walmartBrowseACategory**](WalmartApi.md#walmartBrowseACategory) | **GET** /v1/walmart/category | Browse a category |
| [**walmartDealsRollbacksAndClearance**](WalmartApi.md#walmartDealsRollbacksAndClearance) | **GET** /v1/walmart/deals | Deals, rollbacks and clearance |
| [**walmartGetASellerSCatalogue**](WalmartApi.md#walmartGetASellerSCatalogue) | **GET** /v1/walmart/sellers/{seller_id}/products | Get a seller&#39;s catalogue |
| [**walmartGetProductDetail**](WalmartApi.md#walmartGetProductDetail) | **GET** /v1/walmart/products/{item_id} | Get product detail |
| [**walmartGetProductReviews**](WalmartApi.md#walmartGetProductReviews) | **GET** /v1/walmart/products/{item_id}/reviews | Get product reviews |
| [**walmartGetSellerProfile**](WalmartApi.md#walmartGetSellerProfile) | **GET** /v1/walmart/sellers/{seller_id} | Get seller profile |
| [**walmartGetStoreNearbyStores**](WalmartApi.md#walmartGetStoreNearbyStores) | **GET** /v1/walmart/stores/{store_id} | Get store + nearby stores |
| [**walmartListSupportedMarkets**](WalmartApi.md#walmartListSupportedMarkets) | **GET** /v1/walmart/markets | List supported markets |
| [**walmartSearchProducts**](WalmartApi.md#walmartSearchProducts) | **GET** /v1/walmart/search | Search products |
| [**walmartSearchSuggestions**](WalmartApi.md#walmartSearchSuggestions) | **GET** /v1/walmart/autocomplete | Search suggestions |
| [**walmartWalmartScraperHealthCheck**](WalmartApi.md#walmartWalmartScraperHealthCheck) | **GET** /v1/walmart/health | Walmart scraper health check |
| [**walmartWalmartScraperHealthCheckHead**](WalmartApi.md#walmartWalmartScraperHealthCheckHead) | **HEAD** /v1/walmart/health | Walmart scraper health check |


<a id="walmartBrowseACategory"></a>
# **walmartBrowseACategory**
> Object walmartBrowseACategory(path, page, minPrice, maxPrice, facet)

Browse a category

Browse a Walmart category. Same result shape as search.  No &#x60;sort&#x60;: Walmart&#39;s browse pages ignore it. Sort on &#x60;/search&#x60; instead.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WalmartApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WalmartApi apiInstance = new WalmartApi(defaultClient);
    String path = "path_example"; // String | Browse path, e.g. 'electronics/3944', or a '/cp/...' path
    Integer page = 1; // Integer | 
    BigDecimal minPrice = new BigDecimal(78); // BigDecimal | 
    BigDecimal maxPrice = new BigDecimal(78); // BigDecimal | 
    String facet = "facet_example"; // String | 
    try {
      Object result = apiInstance.walmartBrowseACategory(path, page, minPrice, maxPrice, facet);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WalmartApi#walmartBrowseACategory");
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
| **path** | **String**| Browse path, e.g. &#39;electronics/3944&#39;, or a &#39;/cp/...&#39; path | |
| **page** | **Integer**|  | [optional] [default to 1] |
| **minPrice** | **BigDecimal**|  | [optional] |
| **maxPrice** | **BigDecimal**|  | [optional] |
| **facet** | **String**|  | [optional] |

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

<a id="walmartDealsRollbacksAndClearance"></a>
# **walmartDealsRollbacksAndClearance**
> Object walmartDealsRollbacksAndClearance(page, minPrice, maxPrice)

Deals, rollbacks and clearance

Walmart&#39;s current deals, rollbacks and clearance.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WalmartApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WalmartApi apiInstance = new WalmartApi(defaultClient);
    Integer page = 1; // Integer | 
    BigDecimal minPrice = new BigDecimal(78); // BigDecimal | 
    BigDecimal maxPrice = new BigDecimal(78); // BigDecimal | 
    try {
      Object result = apiInstance.walmartDealsRollbacksAndClearance(page, minPrice, maxPrice);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WalmartApi#walmartDealsRollbacksAndClearance");
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
| **page** | **Integer**|  | [optional] [default to 1] |
| **minPrice** | **BigDecimal**|  | [optional] |
| **maxPrice** | **BigDecimal**|  | [optional] |

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

<a id="walmartGetASellerSCatalogue"></a>
# **walmartGetASellerSCatalogue**
> Object walmartGetASellerSCatalogue(sellerId, query, page, sort)

Get a seller&#39;s catalogue

A marketplace seller&#39;s catalogue, scoped by a search term.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WalmartApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WalmartApi apiInstance = new WalmartApi(defaultClient);
    String sellerId = "sellerId_example"; // String | Numeric catalog seller id, e.g. '101040442' — the `catalog_seller_id` on a product, NOT the 32-char hex `seller_id` (which 404s).
    String query = "query_example"; // String | Required — Walmart returns nothing for a seller facet alone
    Integer page = 1; // Integer | 
    String sort = "sort_example"; // String | 
    try {
      Object result = apiInstance.walmartGetASellerSCatalogue(sellerId, query, page, sort);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WalmartApi#walmartGetASellerSCatalogue");
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
| **sellerId** | **String**| Numeric catalog seller id, e.g. &#39;101040442&#39; — the &#x60;catalog_seller_id&#x60; on a product, NOT the 32-char hex &#x60;seller_id&#x60; (which 404s). | |
| **query** | **String**| Required — Walmart returns nothing for a seller facet alone | |
| **page** | **Integer**|  | [optional] [default to 1] |
| **sort** | **String**|  | [optional] |

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

<a id="walmartGetProductDetail"></a>
# **walmartGetProductDetail**
> Object walmartGetProductDetail(itemId)

Get product detail

Full product detail — price, stock, specs, variants, seller, reviews sample.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WalmartApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WalmartApi apiInstance = new WalmartApi(defaultClient);
    String itemId = "itemId_example"; // String | Walmart usItemId, e.g. '5689919121'
    try {
      Object result = apiInstance.walmartGetProductDetail(itemId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WalmartApi#walmartGetProductDetail");
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
| **itemId** | **String**| Walmart usItemId, e.g. &#39;5689919121&#39; | |

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

<a id="walmartGetProductReviews"></a>
# **walmartGetProductReviews**
> Object walmartGetProductReviews(itemId, page, sort)

Get product reviews

Paginated reviews with the full star histogram. 10 per page.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WalmartApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WalmartApi apiInstance = new WalmartApi(defaultClient);
    String itemId = "itemId_example"; // String | Walmart usItemId, e.g. '5689919121'
    Integer page = 1; // Integer | 
    String sort = "sort_example"; // String | relevancy | submission-desc | submission-asc | rating-desc | rating-asc | helpful
    try {
      Object result = apiInstance.walmartGetProductReviews(itemId, page, sort);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WalmartApi#walmartGetProductReviews");
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
| **itemId** | **String**| Walmart usItemId, e.g. &#39;5689919121&#39; | |
| **page** | **Integer**|  | [optional] [default to 1] |
| **sort** | **String**| relevancy | submission-desc | submission-asc | rating-desc | rating-asc | helpful | [optional] |

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

<a id="walmartGetSellerProfile"></a>
# **walmartGetSellerProfile**
> Object walmartGetSellerProfile(sellerId)

Get seller profile

Marketplace seller profile — contact details, address, rating, policies.  No &#x60;page&#x60;: adding one makes Walmart&#39;s own SSR throw. Use &#x60;/sellers/{id}/products&#x60; for the catalogue.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WalmartApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WalmartApi apiInstance = new WalmartApi(defaultClient);
    String sellerId = "sellerId_example"; // String | Numeric catalog seller id, e.g. '101040442' — the `catalog_seller_id` on a product, NOT the 32-char hex `seller_id` (which 404s).
    try {
      Object result = apiInstance.walmartGetSellerProfile(sellerId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WalmartApi#walmartGetSellerProfile");
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
| **sellerId** | **String**| Numeric catalog seller id, e.g. &#39;101040442&#39; — the &#x60;catalog_seller_id&#x60; on a product, NOT the 32-char hex &#x60;seller_id&#x60; (which 404s). | |

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

<a id="walmartGetStoreNearbyStores"></a>
# **walmartGetStoreNearbyStores**
> Object walmartGetStoreNearbyStores(storeId)

Get store + nearby stores

Store detail with hours, per-department services, and nearby stores.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WalmartApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WalmartApi apiInstance = new WalmartApi(defaultClient);
    String storeId = "storeId_example"; // String | Walmart store number, e.g. '100'
    try {
      Object result = apiInstance.walmartGetStoreNearbyStores(storeId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WalmartApi#walmartGetStoreNearbyStores");
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
| **storeId** | **String**| Walmart store number, e.g. &#39;100&#39; | |

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

<a id="walmartListSupportedMarkets"></a>
# **walmartListSupportedMarkets**
> Object walmartListSupportedMarkets()

List supported markets

Supported Walmart markets.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WalmartApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WalmartApi apiInstance = new WalmartApi(defaultClient);
    try {
      Object result = apiInstance.walmartListSupportedMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WalmartApi#walmartListSupportedMarkets");
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

<a id="walmartSearchProducts"></a>
# **walmartSearchProducts**
> Object walmartSearchProducts(query, page, sort, minPrice, maxPrice, facet)

Search products

Search walmart.com. ~40-60 organic products per page; ad tiles are dropped.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WalmartApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WalmartApi apiInstance = new WalmartApi(defaultClient);
    String query = "query_example"; // String | Search keywords, e.g. 'laptop'
    Integer page = 1; // Integer | Results dry up after page 10
    String sort = "sort_example"; // String | best_match | best_seller | price_low | price_high | rating_high | new
    BigDecimal minPrice = new BigDecimal(78); // BigDecimal | 
    BigDecimal maxPrice = new BigDecimal(78); // BigDecimal | 
    String facet = "facet_example"; // String | Facet filter, e.g. 'brand:HP'
    try {
      Object result = apiInstance.walmartSearchProducts(query, page, sort, minPrice, maxPrice, facet);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WalmartApi#walmartSearchProducts");
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
| **query** | **String**| Search keywords, e.g. &#39;laptop&#39; | |
| **page** | **Integer**| Results dry up after page 10 | [optional] [default to 1] |
| **sort** | **String**| best_match | best_seller | price_low | price_high | rating_high | new | [optional] |
| **minPrice** | **BigDecimal**|  | [optional] |
| **maxPrice** | **BigDecimal**|  | [optional] |
| **facet** | **String**| Facet filter, e.g. &#39;brand:HP&#39; | [optional] |

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

<a id="walmartSearchSuggestions"></a>
# **walmartSearchSuggestions**
> Object walmartSearchSuggestions(query)

Search suggestions

Walmart search-box suggestions.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WalmartApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WalmartApi apiInstance = new WalmartApi(defaultClient);
    String query = "query_example"; // String | Partial search term, e.g. 'lapt'
    try {
      Object result = apiInstance.walmartSearchSuggestions(query);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WalmartApi#walmartSearchSuggestions");
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
| **query** | **String**| Partial search term, e.g. &#39;lapt&#39; | |

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

<a id="walmartWalmartScraperHealthCheck"></a>
# **walmartWalmartScraperHealthCheck**
> Object walmartWalmartScraperHealthCheck()

Walmart scraper health check

Check health of the Walmart scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WalmartApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WalmartApi apiInstance = new WalmartApi(defaultClient);
    try {
      Object result = apiInstance.walmartWalmartScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WalmartApi#walmartWalmartScraperHealthCheck");
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

<a id="walmartWalmartScraperHealthCheckHead"></a>
# **walmartWalmartScraperHealthCheckHead**
> Object walmartWalmartScraperHealthCheckHead()

Walmart scraper health check

Check health of the Walmart scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.WalmartApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    WalmartApi apiInstance = new WalmartApi(defaultClient);
    try {
      Object result = apiInstance.walmartWalmartScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WalmartApi#walmartWalmartScraperHealthCheckHead");
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


# EBayApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**ebayBrowseACategory**](EBayApi.md#ebayBrowseACategory) | **GET** /v1/ebay/categories/{category_id}/items | Browse a category |
| [**ebayCompletedSoldListings**](EBayApi.md#ebayCompletedSoldListings) | **GET** /v1/ebay/completed | Completed / sold listings |
| [**ebayEbayScraperHealthCheck**](EBayApi.md#ebayEbayScraperHealthCheck) | **GET** /v1/ebay/health | eBay scraper health check |
| [**ebayEbayScraperHealthCheckHead**](EBayApi.md#ebayEbayScraperHealthCheckHead) | **HEAD** /v1/ebay/health | eBay scraper health check |
| [**ebayGetItemDetail**](EBayApi.md#ebayGetItemDetail) | **GET** /v1/ebay/items/{item_id} | Get item detail |
| [**ebayGetItemReviews**](EBayApi.md#ebayGetItemReviews) | **GET** /v1/ebay/items/{item_id}/reviews | Get item reviews |
| [**ebayGetSellerFeedback**](EBayApi.md#ebayGetSellerFeedback) | **GET** /v1/ebay/sellers/{username}/feedback | Get seller feedback |
| [**ebayGetSellerListings**](EBayApi.md#ebayGetSellerListings) | **GET** /v1/ebay/sellers/{username}/items | Get seller listings |
| [**ebayGetSellerProfile**](EBayApi.md#ebayGetSellerProfile) | **GET** /v1/ebay/sellers/{username} | Get seller profile |
| [**ebayKeywordSuggestions**](EBayApi.md#ebayKeywordSuggestions) | **GET** /v1/ebay/autocomplete | Keyword suggestions |
| [**ebayListCategories**](EBayApi.md#ebayListCategories) | **GET** /v1/ebay/categories | List categories |
| [**ebayListMarkets**](EBayApi.md#ebayListMarkets) | **GET** /v1/ebay/markets | List markets |
| [**ebaySearchByImage**](EBayApi.md#ebaySearchByImage) | **POST** /v1/ebay/search/by-image | Search by image |
| [**ebaySearchListings**](EBayApi.md#ebaySearchListings) | **GET** /v1/ebay/search | Search listings |


<a id="ebayBrowseACategory"></a>
# **ebayBrowseACategory**
> Object ebayBrowseACategory(categoryId, domain, page, perPage, sortBy, minPrice, maxPrice)

Browse a category

List active listings within an eBay category.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EBayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EBayApi apiInstance = new EBayApi(defaultClient);
    String categoryId = "categoryId_example"; // String | 
    String domain = "com"; // String | 
    Integer page = 1; // Integer | 
    Integer perPage = 56; // Integer | 
    String sortBy = "best_match"; // String | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low
    BigDecimal minPrice = new BigDecimal(78); // BigDecimal | 
    BigDecimal maxPrice = new BigDecimal(78); // BigDecimal | 
    try {
      Object result = apiInstance.ebayBrowseACategory(categoryId, domain, page, perPage, sortBy, minPrice, maxPrice);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EBayApi#ebayBrowseACategory");
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
| **categoryId** | **String**|  | |
| **domain** | **String**|  | [optional] [default to com] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **perPage** | **Integer**|  | [optional] |
| **sortBy** | **String**| best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low | [optional] [default to best_match] |
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

<a id="ebayCompletedSoldListings"></a>
# **ebayCompletedSoldListings**
> Object ebayCompletedSoldListings(query, domain, categoryId, page, perPage, sortBy, condition, minPrice, maxPrice, location, language)

Completed / sold listings

Search completed/sold listings — eBay&#39;s sold-price history.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EBayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EBayApi apiInstance = new EBayApi(defaultClient);
    String query = "query_example"; // String | Search keywords
    String domain = "com"; // String | Marketplace domain (com, co.uk, de …)
    String categoryId = "categoryId_example"; // String | Restrict to a category id
    Integer page = 1; // Integer | 
    Integer perPage = 56; // Integer | 60, 120 or 240
    String sortBy = "best_match"; // String | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low
    String condition = "condition_example"; // String | new|open_box|refurbished|used|for_parts|graded|ungraded
    BigDecimal minPrice = new BigDecimal(78); // BigDecimal | 
    BigDecimal maxPrice = new BigDecimal(78); // BigDecimal | 
    String location = "location_example"; // String | domestic|worldwide
    String language = "language_example"; // String | english|japanese|chinese|korean
    try {
      Object result = apiInstance.ebayCompletedSoldListings(query, domain, categoryId, page, perPage, sortBy, condition, minPrice, maxPrice, location, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EBayApi#ebayCompletedSoldListings");
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
| **query** | **String**| Search keywords | |
| **domain** | **String**| Marketplace domain (com, co.uk, de …) | [optional] [default to com] |
| **categoryId** | **String**| Restrict to a category id | [optional] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **perPage** | **Integer**| 60, 120 or 240 | [optional] |
| **sortBy** | **String**| best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low | [optional] [default to best_match] |
| **condition** | **String**| new|open_box|refurbished|used|for_parts|graded|ungraded | [optional] |
| **minPrice** | **BigDecimal**|  | [optional] |
| **maxPrice** | **BigDecimal**|  | [optional] |
| **location** | **String**| domestic|worldwide | [optional] |
| **language** | **String**| english|japanese|chinese|korean | [optional] |

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

<a id="ebayEbayScraperHealthCheck"></a>
# **ebayEbayScraperHealthCheck**
> Object ebayEbayScraperHealthCheck()

eBay scraper health check

Check health of the eBay scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EBayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EBayApi apiInstance = new EBayApi(defaultClient);
    try {
      Object result = apiInstance.ebayEbayScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EBayApi#ebayEbayScraperHealthCheck");
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

<a id="ebayEbayScraperHealthCheckHead"></a>
# **ebayEbayScraperHealthCheckHead**
> Object ebayEbayScraperHealthCheckHead()

eBay scraper health check

Check health of the eBay scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EBayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EBayApi apiInstance = new EBayApi(defaultClient);
    try {
      Object result = apiInstance.ebayEbayScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EBayApi#ebayEbayScraperHealthCheckHead");
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

<a id="ebayGetItemDetail"></a>
# **ebayGetItemDetail**
> Object ebayGetItemDetail(itemId, domain)

Get item detail

Get a single eBay listing&#39;s full detail.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EBayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EBayApi apiInstance = new EBayApi(defaultClient);
    String itemId = "itemId_example"; // String | 
    String domain = "com"; // String | 
    try {
      Object result = apiInstance.ebayGetItemDetail(itemId, domain);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EBayApi#ebayGetItemDetail");
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
| **domain** | **String**|  | [optional] [default to com] |

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

<a id="ebayGetItemReviews"></a>
# **ebayGetItemReviews**
> Object ebayGetItemReviews(itemId, domain, page)

Get item reviews

Get catalog product reviews shown on an eBay listing.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EBayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EBayApi apiInstance = new EBayApi(defaultClient);
    String itemId = "itemId_example"; // String | 
    String domain = "com"; // String | 
    Integer page = 1; // Integer | 
    try {
      Object result = apiInstance.ebayGetItemReviews(itemId, domain, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EBayApi#ebayGetItemReviews");
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
| **domain** | **String**|  | [optional] [default to com] |
| **page** | **Integer**|  | [optional] [default to 1] |

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

<a id="ebayGetSellerFeedback"></a>
# **ebayGetSellerFeedback**
> Object ebayGetSellerFeedback(username, domain, page)

Get seller feedback

Get a seller&#39;s recent feedback comments.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EBayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EBayApi apiInstance = new EBayApi(defaultClient);
    String username = "username_example"; // String | 
    String domain = "com"; // String | 
    Integer page = 1; // Integer | 
    try {
      Object result = apiInstance.ebayGetSellerFeedback(username, domain, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EBayApi#ebayGetSellerFeedback");
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
| **username** | **String**|  | |
| **domain** | **String**|  | [optional] [default to com] |
| **page** | **Integer**|  | [optional] [default to 1] |

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

<a id="ebayGetSellerListings"></a>
# **ebayGetSellerListings**
> Object ebayGetSellerListings(username, domain, query, page, perPage)

Get seller listings

List the active listings of a single eBay seller.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EBayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EBayApi apiInstance = new EBayApi(defaultClient);
    String username = "username_example"; // String | 
    String domain = "com"; // String | 
    String query = "query_example"; // String | 
    Integer page = 1; // Integer | 
    Integer perPage = 56; // Integer | 
    try {
      Object result = apiInstance.ebayGetSellerListings(username, domain, query, page, perPage);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EBayApi#ebayGetSellerListings");
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
| **username** | **String**|  | |
| **domain** | **String**|  | [optional] [default to com] |
| **query** | **String**|  | [optional] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **perPage** | **Integer**|  | [optional] |

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

<a id="ebayGetSellerProfile"></a>
# **ebayGetSellerProfile**
> Object ebayGetSellerProfile(username, domain)

Get seller profile

Get an eBay seller&#39;s public profile.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EBayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EBayApi apiInstance = new EBayApi(defaultClient);
    String username = "username_example"; // String | 
    String domain = "com"; // String | 
    try {
      Object result = apiInstance.ebayGetSellerProfile(username, domain);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EBayApi#ebayGetSellerProfile");
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
| **username** | **String**|  | |
| **domain** | **String**|  | [optional] [default to com] |

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

<a id="ebayKeywordSuggestions"></a>
# **ebayKeywordSuggestions**
> Object ebayKeywordSuggestions(query, domain)

Keyword suggestions

Return eBay keyword autocomplete suggestions.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EBayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EBayApi apiInstance = new EBayApi(defaultClient);
    String query = "query_example"; // String | Partial query prefix
    String domain = "com"; // String | 
    try {
      Object result = apiInstance.ebayKeywordSuggestions(query, domain);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EBayApi#ebayKeywordSuggestions");
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
| **query** | **String**| Partial query prefix | |
| **domain** | **String**|  | [optional] [default to com] |

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

<a id="ebayListCategories"></a>
# **ebayListCategories**
> Object ebayListCategories()

List categories

List eBay&#39;s top-level category ids.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EBayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EBayApi apiInstance = new EBayApi(defaultClient);
    try {
      Object result = apiInstance.ebayListCategories();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EBayApi#ebayListCategories");
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

<a id="ebayListMarkets"></a>
# **ebayListMarkets**
> Object ebayListMarkets()

List markets

List all supported eBay marketplaces.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EBayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EBayApi apiInstance = new EBayApi(defaultClient);
    try {
      Object result = apiInstance.ebayListMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EBayApi#ebayListMarkets");
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

<a id="ebaySearchByImage"></a>
# **ebaySearchByImage**
> Object ebaySearchByImage(requestBody)

Search by image

Search active listings by image, the way eBay&#39;s camera icon does.  No &#x60;&#x60;sort_by&#x60;&#x60;: eBay ignores it on a visual results page.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EBayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EBayApi apiInstance = new EBayApi(defaultClient);
    Map<String, Object> requestBody = null; // Map<String, Object> | 
    try {
      Object result = apiInstance.ebaySearchByImage(requestBody);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EBayApi#ebaySearchByImage");
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
| **requestBody** | [**Map&lt;String, Object&gt;**](Object.md)|  | |

### Return type

**Object**

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="ebaySearchListings"></a>
# **ebaySearchListings**
> Object ebaySearchListings(query, domain, categoryId, page, perPage, sortBy, condition, buyingFormat, minPrice, maxPrice, freeShipping, location, language)

Search listings

Search an eBay marketplace for active listings.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EBayApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EBayApi apiInstance = new EBayApi(defaultClient);
    String query = "query_example"; // String | Search keywords
    String domain = "com"; // String | Marketplace domain (com, co.uk, de …)
    String categoryId = "categoryId_example"; // String | Restrict to a category id
    Integer page = 1; // Integer | 
    Integer perPage = 56; // Integer | 60, 120 or 240
    String sortBy = "best_match"; // String | best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low
    String condition = "condition_example"; // String | new|open_box|refurbished|used|for_parts|graded|ungraded
    String buyingFormat = "buyingFormat_example"; // String | auction|buy_it_now|best_offer
    BigDecimal minPrice = new BigDecimal(78); // BigDecimal | 
    BigDecimal maxPrice = new BigDecimal(78); // BigDecimal | 
    Boolean freeShipping = false; // Boolean | 
    String location = "location_example"; // String | domestic|worldwide
    String language = "language_example"; // String | english|japanese|chinese|korean
    try {
      Object result = apiInstance.ebaySearchListings(query, domain, categoryId, page, perPage, sortBy, condition, buyingFormat, minPrice, maxPrice, freeShipping, location, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EBayApi#ebaySearchListings");
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
| **query** | **String**| Search keywords | |
| **domain** | **String**| Marketplace domain (com, co.uk, de …) | [optional] [default to com] |
| **categoryId** | **String**| Restrict to a category id | [optional] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **perPage** | **Integer**| 60, 120 or 240 | [optional] |
| **sortBy** | **String**| best_match|ending_soonest|newly_listed|price_low_to_high|price_high_to_low | [optional] [default to best_match] |
| **condition** | **String**| new|open_box|refurbished|used|for_parts|graded|ungraded | [optional] |
| **buyingFormat** | **String**| auction|buy_it_now|best_offer | [optional] |
| **minPrice** | **BigDecimal**|  | [optional] |
| **maxPrice** | **BigDecimal**|  | [optional] |
| **freeShipping** | **Boolean**|  | [optional] [default to false] |
| **location** | **String**| domestic|worldwide | [optional] |
| **language** | **String**| english|japanese|chinese|korean | [optional] |

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


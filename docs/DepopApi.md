# DepopApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**depopDepopScraperHealthCheck**](DepopApi.md#depopDepopScraperHealthCheck) | **GET** /v1/depop/health | Depop scraper health check |
| [**depopDepopScraperHealthCheckHead**](DepopApi.md#depopDepopScraperHealthCheckHead) | **HEAD** /v1/depop/health | Depop scraper health check |
| [**depopGetAUserSProducts**](DepopApi.md#depopGetAUserSProducts) | **GET** /v1/depop/users/{username}/products | Get a user&#39;s products |
| [**depopGetProductDetail**](DepopApi.md#depopGetProductDetail) | **GET** /v1/depop/products/{product_id} | Get product detail |
| [**depopGetShopUserProfile**](DepopApi.md#depopGetShopUserProfile) | **GET** /v1/depop/users/{username} | Get shop/user profile |
| [**depopListMarkets**](DepopApi.md#depopListMarkets) | **GET** /v1/depop/markets | List markets |
| [**depopSearchDepopProducts**](DepopApi.md#depopSearchDepopProducts) | **GET** /v1/depop/search | Search Depop products |


<a id="depopDepopScraperHealthCheck"></a>
# **depopDepopScraperHealthCheck**
> Object depopDepopScraperHealthCheck()

Depop scraper health check

Check health of the Depop scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.DepopApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DepopApi apiInstance = new DepopApi(defaultClient);
    try {
      Object result = apiInstance.depopDepopScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DepopApi#depopDepopScraperHealthCheck");
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

<a id="depopDepopScraperHealthCheckHead"></a>
# **depopDepopScraperHealthCheckHead**
> Object depopDepopScraperHealthCheckHead()

Depop scraper health check

Check health of the Depop scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.DepopApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DepopApi apiInstance = new DepopApi(defaultClient);
    try {
      Object result = apiInstance.depopDepopScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DepopApi#depopDepopScraperHealthCheckHead");
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

<a id="depopGetAUserSProducts"></a>
# **depopGetAUserSProducts**
> Object depopGetAUserSProducts(username, market, perPage, cursor)

Get a user&#39;s products

A user&#39;s active listings (cursor-paginated).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.DepopApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DepopApi apiInstance = new DepopApi(defaultClient);
    String username = "username_example"; // String | 
    String market = "us"; // String | Market code
    Integer perPage = 24; // Integer | 
    String cursor = "cursor_example"; // String | Pagination cursor
    try {
      Object result = apiInstance.depopGetAUserSProducts(username, market, perPage, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DepopApi#depopGetAUserSProducts");
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
| **market** | **String**| Market code | [optional] [default to us] |
| **perPage** | **Integer**|  | [optional] [default to 24] |
| **cursor** | **String**| Pagination cursor | [optional] |

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

<a id="depopGetProductDetail"></a>
# **depopGetProductDetail**
> Object depopGetProductDetail(productId, market)

Get product detail

Full detail for a single product (by numeric id or slug).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.DepopApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DepopApi apiInstance = new DepopApi(defaultClient);
    String productId = "productId_example"; // String | 
    String market = "us"; // String | Market code
    try {
      Object result = apiInstance.depopGetProductDetail(productId, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DepopApi#depopGetProductDetail");
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
| **productId** | **String**|  | |
| **market** | **String**| Market code | [optional] [default to us] |

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

<a id="depopGetShopUserProfile"></a>
# **depopGetShopUserProfile**
> Object depopGetShopUserProfile(username, market)

Get shop/user profile

Public shop/user profile by username.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.DepopApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DepopApi apiInstance = new DepopApi(defaultClient);
    String username = "username_example"; // String | 
    String market = "us"; // String | Market code
    try {
      Object result = apiInstance.depopGetShopUserProfile(username, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DepopApi#depopGetShopUserProfile");
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
| **market** | **String**| Market code | [optional] [default to us] |

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

<a id="depopListMarkets"></a>
# **depopListMarkets**
> Object depopListMarkets()

List markets

List supported Depop markets (country + currency).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.DepopApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DepopApi apiInstance = new DepopApi(defaultClient);
    try {
      Object result = apiInstance.depopListMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DepopApi#depopListMarkets");
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

<a id="depopSearchDepopProducts"></a>
# **depopSearchDepopProducts**
> Object depopSearchDepopProducts(query, market, perPage, cursor, priceMin, priceMax, brands, categories, sizes, conditions, gender, sort)

Search Depop products

Search the Depop catalog with filters (cursor-paginated).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.DepopApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DepopApi apiInstance = new DepopApi(defaultClient);
    String query = "query_example"; // String | Search text, e.g. 'nike vintage'
    String market = "us"; // String | Market code (us, gb, au, it, fr, ...)
    Integer perPage = 24; // Integer | Results per page
    String cursor = "cursor_example"; // String | Pagination cursor (from previous page)
    BigDecimal priceMin = new BigDecimal(78); // BigDecimal | Minimum price
    BigDecimal priceMax = new BigDecimal(78); // BigDecimal | Maximum price
    String brands = "brands_example"; // String | Comma-separated brand IDs
    String categories = "categories_example"; // String | Comma-separated category IDs
    String sizes = "sizes_example"; // String | Comma-separated size IDs
    String conditions = "conditions_example"; // String | Comma-separated condition slugs (brand_new, used_excellent, ...)
    String gender = "gender_example"; // String | male | female
    String sort = "sort_example"; // String | relevance | newlyListed | priceAscending | priceDescending
    try {
      Object result = apiInstance.depopSearchDepopProducts(query, market, perPage, cursor, priceMin, priceMax, brands, categories, sizes, conditions, gender, sort);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DepopApi#depopSearchDepopProducts");
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
| **query** | **String**| Search text, e.g. &#39;nike vintage&#39; | |
| **market** | **String**| Market code (us, gb, au, it, fr, ...) | [optional] [default to us] |
| **perPage** | **Integer**| Results per page | [optional] [default to 24] |
| **cursor** | **String**| Pagination cursor (from previous page) | [optional] |
| **priceMin** | **BigDecimal**| Minimum price | [optional] |
| **priceMax** | **BigDecimal**| Maximum price | [optional] |
| **brands** | **String**| Comma-separated brand IDs | [optional] |
| **categories** | **String**| Comma-separated category IDs | [optional] |
| **sizes** | **String**| Comma-separated size IDs | [optional] |
| **conditions** | **String**| Comma-separated condition slugs (brand_new, used_excellent, ...) | [optional] |
| **gender** | **String**| male | female | [optional] |
| **sort** | **String**| relevance | newlyListed | priceAscending | priceDescending | [optional] |

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


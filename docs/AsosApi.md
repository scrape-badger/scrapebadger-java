# AsosApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**asosGetProductDetail**](AsosApi.md#asosGetProductDetail) | **GET** /v1/asos/products/{product_id} | Get product detail |
| [**asosGetStockAndPrices**](AsosApi.md#asosGetStockAndPrices) | **GET** /v1/asos/stock-price | Get stock and prices |
| [**asosListCategories**](AsosApi.md#asosListCategories) | **GET** /v1/asos/categories | List categories |
| [**asosListMarkets**](AsosApi.md#asosListMarkets) | **GET** /v1/asos/markets | List markets |
| [**asosListSearchFilters**](AsosApi.md#asosListSearchFilters) | **GET** /v1/asos/filters | List search filters |
| [**asosSearchProducts**](AsosApi.md#asosSearchProducts) | **GET** /v1/asos/search | Search products |
| [**asosSearchSuggestions**](AsosApi.md#asosSearchSuggestions) | **GET** /v1/asos/autocomplete | Search suggestions |


<a id="asosGetProductDetail"></a>
# **asosGetProductDetail**
> ProductResponse asosGetProductDetail(productId, market, store, country, currency, language)

Get product detail

Product, live per-size stock and price, images, descriptions, reviews and breadcrumbs.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AsosApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AsosApi apiInstance = new AsosApi(defaultClient);
    Integer productId = 56; // Integer | 
    String market = "uk"; // String | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl
    String store = "store_example"; // String | Override store, e.g. COM or US
    String country = "country_example"; // String | ISO country override
    String currency = "currency_example"; // String | Currency override
    String language = "language_example"; // String | Locale override, e.g. en-GB
    try {
      ProductResponse result = apiInstance.asosGetProductDetail(productId, market, store, country, currency, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AsosApi#asosGetProductDetail");
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
| **productId** | **Integer**|  | |
| **market** | **String**| Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to uk] |
| **store** | **String**| Override store, e.g. COM or US | [optional] |
| **country** | **String**| ISO country override | [optional] |
| **currency** | **String**| Currency override | [optional] |
| **language** | **String**| Locale override, e.g. en-GB | [optional] |

### Return type

[**ProductResponse**](ProductResponse.md)

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

<a id="asosGetStockAndPrices"></a>
# **asosGetStockAndPrices**
> StockResponse asosGetStockAndPrices(productIds, market, store, country, currency, language)

Get stock and prices

Refresh product and variant stock/prices; reports missing product ids explicitly.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AsosApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AsosApi apiInstance = new AsosApi(defaultClient);
    String productIds = "productIds_example"; // String | 1–50 comma-separated product ids
    String market = "uk"; // String | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl
    String store = "store_example"; // String | Override store, e.g. COM or US
    String country = "country_example"; // String | ISO country override
    String currency = "currency_example"; // String | Currency override
    String language = "language_example"; // String | Locale override, e.g. en-GB
    try {
      StockResponse result = apiInstance.asosGetStockAndPrices(productIds, market, store, country, currency, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AsosApi#asosGetStockAndPrices");
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
| **productIds** | **String**| 1–50 comma-separated product ids | |
| **market** | **String**| Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to uk] |
| **store** | **String**| Override store, e.g. COM or US | [optional] |
| **country** | **String**| ISO country override | [optional] |
| **currency** | **String**| Currency override | [optional] |
| **language** | **String**| Locale override, e.g. en-GB | [optional] |

### Return type

[**StockResponse**](StockResponse.md)

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

<a id="asosListCategories"></a>
# **asosListCategories**
> Object asosListCategories(gender, market, store, country, currency, language)

List categories

Full nested navigation with category ids, names, images and links.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AsosApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AsosApi apiInstance = new AsosApi(defaultClient);
    String gender = "men"; // String | 
    String market = "uk"; // String | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl
    String store = "store_example"; // String | Override store, e.g. COM or US
    String country = "country_example"; // String | ISO country override
    String currency = "currency_example"; // String | Currency override
    String language = "language_example"; // String | Locale override, e.g. en-GB
    try {
      Object result = apiInstance.asosListCategories(gender, market, store, country, currency, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AsosApi#asosListCategories");
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
| **gender** | **String**|  | [optional] [default to men] [enum: men, women] |
| **market** | **String**| Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to uk] |
| **store** | **String**| Override store, e.g. COM or US | [optional] |
| **country** | **String**| ISO country override | [optional] |
| **currency** | **String**| Currency override | [optional] |
| **language** | **String**| Locale override, e.g. en-GB | [optional] |

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

<a id="asosListMarkets"></a>
# **asosListMarkets**
> Object asosListMarkets()

List markets

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AsosApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AsosApi apiInstance = new AsosApi(defaultClient);
    try {
      Object result = apiInstance.asosListMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AsosApi#asosListMarkets");
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

<a id="asosListSearchFilters"></a>
# **asosListSearchFilters**
> Object asosListSearchFilters(query, categoryId, market, store, country, currency, language)

List search filters

Facet ids, labels, option counts and selections for a query or category.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AsosApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AsosApi apiInstance = new AsosApi(defaultClient);
    String query = "query_example"; // String | 
    Integer categoryId = 56; // Integer | 
    String market = "uk"; // String | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl
    String store = "store_example"; // String | Override store, e.g. COM or US
    String country = "country_example"; // String | ISO country override
    String currency = "currency_example"; // String | Currency override
    String language = "language_example"; // String | Locale override, e.g. en-GB
    try {
      Object result = apiInstance.asosListSearchFilters(query, categoryId, market, store, country, currency, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AsosApi#asosListSearchFilters");
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
| **query** | **String**|  | [optional] |
| **categoryId** | **Integer**|  | [optional] |
| **market** | **String**| Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to uk] |
| **store** | **String**| Override store, e.g. COM or US | [optional] |
| **country** | **String**| ISO country override | [optional] |
| **currency** | **String**| Currency override | [optional] |
| **language** | **String**| Locale override, e.g. en-GB | [optional] |

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

<a id="asosSearchProducts"></a>
# **asosSearchProducts**
> PortalApiRoutersV1AsosSearchResponse asosSearchProducts(query, categoryId, offset, limit, sort, brand, colour, size, minPrice, maxPrice, market, store, country, currency, language)

Search products

Search by query, category_id, or both. Includes price, images and filter facets.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AsosApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AsosApi apiInstance = new AsosApi(defaultClient);
    String query = "query_example"; // String | Keyword, e.g. shoes
    Integer categoryId = 56; // Integer | Category id from navigation
    Integer offset = 0; // Integer | 
    Integer limit = 48; // Integer | 
    String sort = "recommended"; // String | 
    String brand = "brand_example"; // String | Comma-separated brand facet ids
    String colour = "colour_example"; // String | Comma-separated colour facet ids
    String size = "size_example"; // String | Comma-separated size facet ids
    BigDecimal minPrice = new BigDecimal(78); // BigDecimal | 
    BigDecimal maxPrice = new BigDecimal(78); // BigDecimal | 
    String market = "uk"; // String | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl
    String store = "store_example"; // String | Override store, e.g. COM or US
    String country = "country_example"; // String | ISO country override
    String currency = "currency_example"; // String | Currency override
    String language = "language_example"; // String | Locale override, e.g. en-GB
    try {
      PortalApiRoutersV1AsosSearchResponse result = apiInstance.asosSearchProducts(query, categoryId, offset, limit, sort, brand, colour, size, minPrice, maxPrice, market, store, country, currency, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AsosApi#asosSearchProducts");
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
| **query** | **String**| Keyword, e.g. shoes | [optional] |
| **categoryId** | **Integer**| Category id from navigation | [optional] |
| **offset** | **Integer**|  | [optional] [default to 0] |
| **limit** | **Integer**|  | [optional] [default to 48] |
| **sort** | **String**|  | [optional] [default to recommended] [enum: recommended, freshness, priceasc, pricedesc] |
| **brand** | **String**| Comma-separated brand facet ids | [optional] |
| **colour** | **String**| Comma-separated colour facet ids | [optional] |
| **size** | **String**| Comma-separated size facet ids | [optional] |
| **minPrice** | **BigDecimal**|  | [optional] |
| **maxPrice** | **BigDecimal**|  | [optional] |
| **market** | **String**| Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to uk] |
| **store** | **String**| Override store, e.g. COM or US | [optional] |
| **country** | **String**| ISO country override | [optional] |
| **currency** | **String**| Currency override | [optional] |
| **language** | **String**| Locale override, e.g. en-GB | [optional] |

### Return type

[**PortalApiRoutersV1AsosSearchResponse**](PortalApiRoutersV1AsosSearchResponse.md)

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

<a id="asosSearchSuggestions"></a>
# **asosSearchSuggestions**
> Object asosSearchSuggestions(query, market, store, country, currency, language)

Search suggestions

Search suggestions with result counts.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AsosApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AsosApi apiInstance = new AsosApi(defaultClient);
    String query = "query_example"; // String | 
    String market = "uk"; // String | Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl
    String store = "store_example"; // String | Override store, e.g. COM or US
    String country = "country_example"; // String | ISO country override
    String currency = "currency_example"; // String | Currency override
    String language = "language_example"; // String | Locale override, e.g. en-GB
    try {
      Object result = apiInstance.asosSearchSuggestions(query, market, store, country, currency, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AsosApi#asosSearchSuggestions");
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
| **query** | **String**|  | |
| **market** | **String**| Storefront: uk, us, au, de, fr, it, es, nl, se, dk, pl | [optional] [default to uk] |
| **store** | **String**| Override store, e.g. COM or US | [optional] |
| **country** | **String**| ISO country override | [optional] |
| **currency** | **String**| Currency override | [optional] |
| **language** | **String**| Locale override, e.g. en-GB | [optional] |

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


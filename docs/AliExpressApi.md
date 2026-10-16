# AliExpressApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**aliexpressGetCategoryNavigation**](AliExpressApi.md#aliexpressGetCategoryNavigation) | **GET** /v1/aliexpress/categories | Get category navigation |
| [**aliexpressGetProductDetail**](AliExpressApi.md#aliexpressGetProductDetail) | **GET** /v1/aliexpress/products/{product_id} | Get product detail |
| [**aliexpressGetProductReviews**](AliExpressApi.md#aliexpressGetProductReviews) | **GET** /v1/aliexpress/products/{product_id}/reviews | Get product reviews |
| [**aliexpressGetSearchSuggestions**](AliExpressApi.md#aliexpressGetSearchSuggestions) | **GET** /v1/aliexpress/autocomplete | Get search suggestions |
| [**aliexpressGetStoreProductCategories**](AliExpressApi.md#aliexpressGetStoreProductCategories) | **GET** /v1/aliexpress/stores/{store_id}/categories | Get store product categories |
| [**aliexpressGetStoreProducts**](AliExpressApi.md#aliexpressGetStoreProducts) | **GET** /v1/aliexpress/stores/{store_id}/products | Get store products |
| [**aliexpressGetStoreProfile**](AliExpressApi.md#aliexpressGetStoreProfile) | **GET** /v1/aliexpress/stores/{store_id} | Get store profile |
| [**aliexpressSearchProducts**](AliExpressApi.md#aliexpressSearchProducts) | **GET** /v1/aliexpress/search | Search products |


<a id="aliexpressGetCategoryNavigation"></a>
# **aliexpressGetCategoryNavigation**
> Object aliexpressGetCategoryNavigation()

Get category navigation

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AliExpressApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AliExpressApi apiInstance = new AliExpressApi(defaultClient);
    try {
      Object result = apiInstance.aliexpressGetCategoryNavigation();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AliExpressApi#aliexpressGetCategoryNavigation");
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

<a id="aliexpressGetProductDetail"></a>
# **aliexpressGetProductDetail**
> Object aliexpressGetProductDetail(productId, country, currency, language)

Get product detail

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AliExpressApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AliExpressApi apiInstance = new AliExpressApi(defaultClient);
    String productId = "productId_example"; // String | 
    String country = "US"; // String | 
    String currency = "USD"; // String | 
    String language = "en_US"; // String | 
    try {
      Object result = apiInstance.aliexpressGetProductDetail(productId, country, currency, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AliExpressApi#aliexpressGetProductDetail");
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
| **country** | **String**|  | [optional] [default to US] |
| **currency** | **String**|  | [optional] [default to USD] |
| **language** | **String**|  | [optional] [default to en_US] |

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

<a id="aliexpressGetProductReviews"></a>
# **aliexpressGetProductReviews**
> Object aliexpressGetProductReviews(productId, page, pageSize, sort)

Get product reviews

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AliExpressApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AliExpressApi apiInstance = new AliExpressApi(defaultClient);
    String productId = "productId_example"; // String | 
    Integer page = 1; // Integer | 
    Integer pageSize = 10; // Integer | 
    String sort = "complex_default"; // String | 
    try {
      Object result = apiInstance.aliexpressGetProductReviews(productId, page, pageSize, sort);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AliExpressApi#aliexpressGetProductReviews");
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
| **page** | **Integer**|  | [optional] [default to 1] |
| **pageSize** | **Integer**|  | [optional] [default to 10] |
| **sort** | **String**|  | [optional] [default to complex_default] [enum: complex_default, latest_sort] |

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

<a id="aliexpressGetSearchSuggestions"></a>
# **aliexpressGetSearchSuggestions**
> Object aliexpressGetSearchSuggestions(query, country, language)

Get search suggestions

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AliExpressApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AliExpressApi apiInstance = new AliExpressApi(defaultClient);
    String query = "query_example"; // String | 
    String country = "US"; // String | 
    String language = "en"; // String | 
    try {
      Object result = apiInstance.aliexpressGetSearchSuggestions(query, country, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AliExpressApi#aliexpressGetSearchSuggestions");
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
| **country** | **String**|  | [optional] [default to US] |
| **language** | **String**|  | [optional] [default to en] |

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

<a id="aliexpressGetStoreProductCategories"></a>
# **aliexpressGetStoreProductCategories**
> Object aliexpressGetStoreProductCategories(storeId, country)

Get store product categories

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AliExpressApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AliExpressApi apiInstance = new AliExpressApi(defaultClient);
    String storeId = "storeId_example"; // String | 
    String country = "US"; // String | 
    try {
      Object result = apiInstance.aliexpressGetStoreProductCategories(storeId, country);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AliExpressApi#aliexpressGetStoreProductCategories");
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
| **storeId** | **String**|  | |
| **country** | **String**|  | [optional] [default to US] |

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

<a id="aliexpressGetStoreProducts"></a>
# **aliexpressGetStoreProducts**
> Object aliexpressGetStoreProducts(storeId, page, pageSize, country, currency, language, query, sort)

Get store products

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AliExpressApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AliExpressApi apiInstance = new AliExpressApi(defaultClient);
    String storeId = "storeId_example"; // String | 
    Integer page = 1; // Integer | 
    Integer pageSize = 24; // Integer | 
    String country = "US"; // String | 
    String currency = "USD"; // String | 
    String language = "en"; // String | 
    String query = ""; // String | 
    String sort = "bestmatch_sort"; // String | 
    try {
      Object result = apiInstance.aliexpressGetStoreProducts(storeId, page, pageSize, country, currency, language, query, sort);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AliExpressApi#aliexpressGetStoreProducts");
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
| **storeId** | **String**|  | |
| **page** | **Integer**|  | [optional] [default to 1] |
| **pageSize** | **Integer**|  | [optional] [default to 24] |
| **country** | **String**|  | [optional] [default to US] |
| **currency** | **String**|  | [optional] [default to USD] |
| **language** | **String**|  | [optional] [default to en] |
| **query** | **String**|  | [optional] [default to ] |
| **sort** | **String**|  | [optional] [default to bestmatch_sort] [enum: bestmatch_sort, price_asc, price_desc, orders_desc] |

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

<a id="aliexpressGetStoreProfile"></a>
# **aliexpressGetStoreProfile**
> Object aliexpressGetStoreProfile(storeId, country, currency, language)

Get store profile

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AliExpressApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AliExpressApi apiInstance = new AliExpressApi(defaultClient);
    String storeId = "storeId_example"; // String | 
    String country = "US"; // String | 
    String currency = "USD"; // String | 
    String language = "en"; // String | 
    try {
      Object result = apiInstance.aliexpressGetStoreProfile(storeId, country, currency, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AliExpressApi#aliexpressGetStoreProfile");
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
| **storeId** | **String**|  | |
| **country** | **String**|  | [optional] [default to US] |
| **currency** | **String**|  | [optional] [default to USD] |
| **language** | **String**|  | [optional] [default to en] |

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

<a id="aliexpressSearchProducts"></a>
# **aliexpressSearchProducts**
> Object aliexpressSearchProducts(query, page, country, currency, language, sort, minPrice, maxPrice)

Search products

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.AliExpressApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    AliExpressApi apiInstance = new AliExpressApi(defaultClient);
    String query = "query_example"; // String | 
    Integer page = 1; // Integer | 
    String country = "US"; // String | 
    String currency = "USD"; // String | 
    String language = "en"; // String | 
    String sort = "default"; // String | 
    BigDecimal minPrice = new BigDecimal(78); // BigDecimal | 
    BigDecimal maxPrice = new BigDecimal(78); // BigDecimal | 
    try {
      Object result = apiInstance.aliexpressSearchProducts(query, page, country, currency, language, sort, minPrice, maxPrice);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling AliExpressApi#aliexpressSearchProducts");
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
| **page** | **Integer**|  | [optional] [default to 1] |
| **country** | **String**|  | [optional] [default to US] |
| **currency** | **String**|  | [optional] [default to USD] |
| **language** | **String**|  | [optional] [default to en] |
| **sort** | **String**|  | [optional] [default to default] [enum: default, price_asc, price_desc, total_tranpro_desc] |
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


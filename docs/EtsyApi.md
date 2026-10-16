# EtsyApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**etsyGetCategories**](EtsyApi.md#etsyGetCategories) | **GET** /v1/etsy/categories | Get categories |
| [**etsyGetListingDetail**](EtsyApi.md#etsyGetListingDetail) | **GET** /v1/etsy/listings/{listing_id} | Get listing detail |
| [**etsyGetListingReviews**](EtsyApi.md#etsyGetListingReviews) | **GET** /v1/etsy/listings/{listing_id}/reviews | Get listing reviews |
| [**etsyGetSearchSuggestions**](EtsyApi.md#etsyGetSearchSuggestions) | **GET** /v1/etsy/autocomplete | Get search suggestions |
| [**etsyGetShopListings**](EtsyApi.md#etsyGetShopListings) | **GET** /v1/etsy/shops/{shop_name}/listings | Get shop listings |
| [**etsyGetShopProfile**](EtsyApi.md#etsyGetShopProfile) | **GET** /v1/etsy/shops/{shop_name} | Get shop profile |
| [**etsyGetShopReviews**](EtsyApi.md#etsyGetShopReviews) | **GET** /v1/etsy/shops/{shop_name}/reviews | Get shop reviews |
| [**etsySearchListings**](EtsyApi.md#etsySearchListings) | **GET** /v1/etsy/search | Search listings |


<a id="etsyGetCategories"></a>
# **etsyGetCategories**
> Object etsyGetCategories(country, currency, language)

Get categories

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EtsyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EtsyApi apiInstance = new EtsyApi(defaultClient);
    String country = "US"; // String | 
    String currency = "USD"; // String | 
    String language = "en-US"; // String | 
    try {
      Object result = apiInstance.etsyGetCategories(country, currency, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EtsyApi#etsyGetCategories");
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
| **country** | **String**|  | [optional] [default to US] |
| **currency** | **String**|  | [optional] [default to USD] |
| **language** | **String**|  | [optional] [default to en-US] |

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

<a id="etsyGetListingDetail"></a>
# **etsyGetListingDetail**
> Object etsyGetListingDetail(listingId, country, currency, language)

Get listing detail

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EtsyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EtsyApi apiInstance = new EtsyApi(defaultClient);
    String listingId = "listingId_example"; // String | 
    String country = "US"; // String | 
    String currency = "USD"; // String | 
    String language = "en-US"; // String | 
    try {
      Object result = apiInstance.etsyGetListingDetail(listingId, country, currency, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EtsyApi#etsyGetListingDetail");
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
| **listingId** | **String**|  | |
| **country** | **String**|  | [optional] [default to US] |
| **currency** | **String**|  | [optional] [default to USD] |
| **language** | **String**|  | [optional] [default to en-US] |

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

<a id="etsyGetListingReviews"></a>
# **etsyGetListingReviews**
> Object etsyGetListingReviews(listingId, page, sort, country, currency, language)

Get listing reviews

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EtsyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EtsyApi apiInstance = new EtsyApi(defaultClient);
    String listingId = "listingId_example"; // String | 
    Integer page = 1; // Integer | 
    String sort = "Relevancy"; // String | 
    String country = "US"; // String | 
    String currency = "USD"; // String | 
    String language = "en-US"; // String | 
    try {
      Object result = apiInstance.etsyGetListingReviews(listingId, page, sort, country, currency, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EtsyApi#etsyGetListingReviews");
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
| **listingId** | **String**|  | |
| **page** | **Integer**|  | [optional] [default to 1] |
| **sort** | **String**|  | [optional] [default to Relevancy] [enum: Relevancy, Recency, Highest, Lowest] |
| **country** | **String**|  | [optional] [default to US] |
| **currency** | **String**|  | [optional] [default to USD] |
| **language** | **String**|  | [optional] [default to en-US] |

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

<a id="etsyGetSearchSuggestions"></a>
# **etsyGetSearchSuggestions**
> Object etsyGetSearchSuggestions(query, country, currency, language)

Get search suggestions

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EtsyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EtsyApi apiInstance = new EtsyApi(defaultClient);
    String query = "query_example"; // String | 
    String country = "US"; // String | 
    String currency = "USD"; // String | 
    String language = "en-US"; // String | 
    try {
      Object result = apiInstance.etsyGetSearchSuggestions(query, country, currency, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EtsyApi#etsyGetSearchSuggestions");
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
| **currency** | **String**|  | [optional] [default to USD] |
| **language** | **String**|  | [optional] [default to en-US] |

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

<a id="etsyGetShopListings"></a>
# **etsyGetShopListings**
> Object etsyGetShopListings(shopName, page, country, currency, language)

Get shop listings

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EtsyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EtsyApi apiInstance = new EtsyApi(defaultClient);
    String shopName = "shopName_example"; // String | 
    Integer page = 1; // Integer | 
    String country = "US"; // String | 
    String currency = "USD"; // String | 
    String language = "en-US"; // String | 
    try {
      Object result = apiInstance.etsyGetShopListings(shopName, page, country, currency, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EtsyApi#etsyGetShopListings");
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
| **shopName** | **String**|  | |
| **page** | **Integer**|  | [optional] [default to 1] |
| **country** | **String**|  | [optional] [default to US] |
| **currency** | **String**|  | [optional] [default to USD] |
| **language** | **String**|  | [optional] [default to en-US] |

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

<a id="etsyGetShopProfile"></a>
# **etsyGetShopProfile**
> Object etsyGetShopProfile(shopName, country, currency, language)

Get shop profile

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EtsyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EtsyApi apiInstance = new EtsyApi(defaultClient);
    String shopName = "shopName_example"; // String | 
    String country = "US"; // String | 
    String currency = "USD"; // String | 
    String language = "en-US"; // String | 
    try {
      Object result = apiInstance.etsyGetShopProfile(shopName, country, currency, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EtsyApi#etsyGetShopProfile");
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
| **shopName** | **String**|  | |
| **country** | **String**|  | [optional] [default to US] |
| **currency** | **String**|  | [optional] [default to USD] |
| **language** | **String**|  | [optional] [default to en-US] |

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

<a id="etsyGetShopReviews"></a>
# **etsyGetShopReviews**
> Object etsyGetShopReviews(shopName, page, country, currency, language)

Get shop reviews

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EtsyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EtsyApi apiInstance = new EtsyApi(defaultClient);
    String shopName = "shopName_example"; // String | 
    Integer page = 1; // Integer | 
    String country = "US"; // String | 
    String currency = "USD"; // String | 
    String language = "en-US"; // String | 
    try {
      Object result = apiInstance.etsyGetShopReviews(shopName, page, country, currency, language);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EtsyApi#etsyGetShopReviews");
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
| **shopName** | **String**|  | |
| **page** | **Integer**|  | [optional] [default to 1] |
| **country** | **String**|  | [optional] [default to US] |
| **currency** | **String**|  | [optional] [default to USD] |
| **language** | **String**|  | [optional] [default to en-US] |

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

<a id="etsySearchListings"></a>
# **etsySearchListings**
> Object etsySearchListings(query, page, country, currency, language, sort, minPrice, maxPrice)

Search listings

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.EtsyApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    EtsyApi apiInstance = new EtsyApi(defaultClient);
    String query = "query_example"; // String | 
    Integer page = 1; // Integer | 
    String country = "US"; // String | 
    String currency = "USD"; // String | 
    String language = "en-US"; // String | 
    String sort = "most_relevant"; // String | 
    BigDecimal minPrice = new BigDecimal(78); // BigDecimal | 
    BigDecimal maxPrice = new BigDecimal(78); // BigDecimal | 
    try {
      Object result = apiInstance.etsySearchListings(query, page, country, currency, language, sort, minPrice, maxPrice);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling EtsyApi#etsySearchListings");
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
| **language** | **String**|  | [optional] [default to en-US] |
| **sort** | **String**|  | [optional] [default to most_relevant] [enum: most_relevant, date_desc, price_asc, price_desc] |
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


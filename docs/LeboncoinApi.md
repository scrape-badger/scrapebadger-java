# LeboncoinApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**leboncoinGetASellerSAds**](LeboncoinApi.md#leboncoinGetASellerSAds) | **GET** /v1/leboncoin/sellers/{user_id}/listings | Get a seller&#39;s ads |
| [**leboncoinGetAdDetail**](LeboncoinApi.md#leboncoinGetAdDetail) | **GET** /v1/leboncoin/ads/{list_id} | Get ad detail |
| [**leboncoinGetSellerProfile**](LeboncoinApi.md#leboncoinGetSellerProfile) | **GET** /v1/leboncoin/sellers/{user_id} | Get seller profile |
| [**leboncoinGetSimilarAds**](LeboncoinApi.md#leboncoinGetSimilarAds) | **GET** /v1/leboncoin/ads/{list_id}/similar | Get similar ads |
| [**leboncoinLeboncoinScraperHealthCheck**](LeboncoinApi.md#leboncoinLeboncoinScraperHealthCheck) | **GET** /v1/leboncoin/health | Leboncoin scraper health check |
| [**leboncoinLeboncoinScraperHealthCheckHead**](LeboncoinApi.md#leboncoinLeboncoinScraperHealthCheckHead) | **HEAD** /v1/leboncoin/health | Leboncoin scraper health check |
| [**leboncoinListCategories**](LeboncoinApi.md#leboncoinListCategories) | **GET** /v1/leboncoin/categories | List categories |
| [**leboncoinListDepartments**](LeboncoinApi.md#leboncoinListDepartments) | **GET** /v1/leboncoin/departments | List departments |
| [**leboncoinListMarkets**](LeboncoinApi.md#leboncoinListMarkets) | **GET** /v1/leboncoin/markets | List markets |
| [**leboncoinListRegions**](LeboncoinApi.md#leboncoinListRegions) | **GET** /v1/leboncoin/regions | List regions |
| [**leboncoinLocationAutocomplete**](LeboncoinApi.md#leboncoinLocationAutocomplete) | **GET** /v1/leboncoin/locations/search | Location autocomplete |
| [**leboncoinSearchLeboncoinAds**](LeboncoinApi.md#leboncoinSearchLeboncoinAds) | **GET** /v1/leboncoin/search | Search Leboncoin ads |


<a id="leboncoinGetASellerSAds"></a>
# **leboncoinGetASellerSAds**
> Object leboncoinGetASellerSAds(userId, page, limit)

Get a seller&#39;s ads

A seller&#39;s active ads.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LeboncoinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LeboncoinApi apiInstance = new LeboncoinApi(defaultClient);
    String userId = "userId_example"; // String | 
    Integer page = 1; // Integer | 
    Integer limit = 35; // Integer | 
    try {
      Object result = apiInstance.leboncoinGetASellerSAds(userId, page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LeboncoinApi#leboncoinGetASellerSAds");
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
| **page** | **Integer**|  | [optional] [default to 1] |
| **limit** | **Integer**|  | [optional] [default to 35] |

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

<a id="leboncoinGetAdDetail"></a>
# **leboncoinGetAdDetail**
> Object leboncoinGetAdDetail(listId)

Get ad detail

Full detail for a Leboncoin ad.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LeboncoinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LeboncoinApi apiInstance = new LeboncoinApi(defaultClient);
    Integer listId = 56; // Integer | 
    try {
      Object result = apiInstance.leboncoinGetAdDetail(listId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LeboncoinApi#leboncoinGetAdDetail");
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
| **listId** | **Integer**|  | |

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

<a id="leboncoinGetSellerProfile"></a>
# **leboncoinGetSellerProfile**
> Object leboncoinGetSellerProfile(userId)

Get seller profile

Public seller/pro-store profile.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LeboncoinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LeboncoinApi apiInstance = new LeboncoinApi(defaultClient);
    String userId = "userId_example"; // String | 
    try {
      Object result = apiInstance.leboncoinGetSellerProfile(userId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LeboncoinApi#leboncoinGetSellerProfile");
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

<a id="leboncoinGetSimilarAds"></a>
# **leboncoinGetSimilarAds**
> Object leboncoinGetSimilarAds(listId, limit)

Get similar ads

Ads Leboncoin surfaces as similar to the given ad.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LeboncoinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LeboncoinApi apiInstance = new LeboncoinApi(defaultClient);
    Integer listId = 56; // Integer | 
    Integer limit = 20; // Integer | 
    try {
      Object result = apiInstance.leboncoinGetSimilarAds(listId, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LeboncoinApi#leboncoinGetSimilarAds");
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
| **listId** | **Integer**|  | |
| **limit** | **Integer**|  | [optional] [default to 20] |

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

<a id="leboncoinLeboncoinScraperHealthCheck"></a>
# **leboncoinLeboncoinScraperHealthCheck**
> Object leboncoinLeboncoinScraperHealthCheck()

Leboncoin scraper health check

Check health of the Leboncoin scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LeboncoinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LeboncoinApi apiInstance = new LeboncoinApi(defaultClient);
    try {
      Object result = apiInstance.leboncoinLeboncoinScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LeboncoinApi#leboncoinLeboncoinScraperHealthCheck");
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

<a id="leboncoinLeboncoinScraperHealthCheckHead"></a>
# **leboncoinLeboncoinScraperHealthCheckHead**
> Object leboncoinLeboncoinScraperHealthCheckHead()

Leboncoin scraper health check

Check health of the Leboncoin scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LeboncoinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LeboncoinApi apiInstance = new LeboncoinApi(defaultClient);
    try {
      Object result = apiInstance.leboncoinLeboncoinScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LeboncoinApi#leboncoinLeboncoinScraperHealthCheckHead");
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

<a id="leboncoinListCategories"></a>
# **leboncoinListCategories**
> Object leboncoinListCategories()

List categories

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LeboncoinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LeboncoinApi apiInstance = new LeboncoinApi(defaultClient);
    try {
      Object result = apiInstance.leboncoinListCategories();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LeboncoinApi#leboncoinListCategories");
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

<a id="leboncoinListDepartments"></a>
# **leboncoinListDepartments**
> Object leboncoinListDepartments(regionId)

List departments

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LeboncoinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LeboncoinApi apiInstance = new LeboncoinApi(defaultClient);
    String regionId = "regionId_example"; // String | 
    try {
      Object result = apiInstance.leboncoinListDepartments(regionId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LeboncoinApi#leboncoinListDepartments");
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
| **regionId** | **String**|  | [optional] |

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

<a id="leboncoinListMarkets"></a>
# **leboncoinListMarkets**
> Object leboncoinListMarkets()

List markets

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LeboncoinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LeboncoinApi apiInstance = new LeboncoinApi(defaultClient);
    try {
      Object result = apiInstance.leboncoinListMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LeboncoinApi#leboncoinListMarkets");
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

<a id="leboncoinListRegions"></a>
# **leboncoinListRegions**
> Object leboncoinListRegions()

List regions

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LeboncoinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LeboncoinApi apiInstance = new LeboncoinApi(defaultClient);
    try {
      Object result = apiInstance.leboncoinListRegions();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LeboncoinApi#leboncoinListRegions");
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

<a id="leboncoinLocationAutocomplete"></a>
# **leboncoinLocationAutocomplete**
> Object leboncoinLocationAutocomplete(q)

Location autocomplete

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LeboncoinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LeboncoinApi apiInstance = new LeboncoinApi(defaultClient);
    String q = "q_example"; // String | Place name
    try {
      Object result = apiInstance.leboncoinLocationAutocomplete(q);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LeboncoinApi#leboncoinLocationAutocomplete");
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
| **q** | **String**| Place name | |

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

<a id="leboncoinSearchLeboncoinAds"></a>
# **leboncoinSearchLeboncoinAds**
> Object leboncoinSearchLeboncoinAds(text, category, regionId, departmentId, city, zipcode, priceMin, priceMax, ownerType, adType, sort, page, limit)

Search Leboncoin ads

Search Leboncoin classifieds (France; scope by region/department/city).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LeboncoinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LeboncoinApi apiInstance = new LeboncoinApi(defaultClient);
    String text = "text_example"; // String | Free-text query
    String category = "category_example"; // String | Category id (see /categories)
    String regionId = "regionId_example"; // String | Region id (see /regions)
    String departmentId = "departmentId_example"; // String | Department id, e.g. 75
    String city = "city_example"; // String | 
    String zipcode = "zipcode_example"; // String | 
    Integer priceMin = 56; // Integer | 
    Integer priceMax = 56; // Integer | 
    String ownerType = "all"; // String | all | pro | private
    String adType = "offer"; // String | offer | demand
    String sort = "relevance"; // String | relevance|newest|oldest|price_low|price_high
    Integer page = 1; // Integer | 
    Integer limit = 35; // Integer | 
    try {
      Object result = apiInstance.leboncoinSearchLeboncoinAds(text, category, regionId, departmentId, city, zipcode, priceMin, priceMax, ownerType, adType, sort, page, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LeboncoinApi#leboncoinSearchLeboncoinAds");
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
| **text** | **String**| Free-text query | [optional] |
| **category** | **String**| Category id (see /categories) | [optional] |
| **regionId** | **String**| Region id (see /regions) | [optional] |
| **departmentId** | **String**| Department id, e.g. 75 | [optional] |
| **city** | **String**|  | [optional] |
| **zipcode** | **String**|  | [optional] |
| **priceMin** | **Integer**|  | [optional] |
| **priceMax** | **Integer**|  | [optional] |
| **ownerType** | **String**| all | pro | private | [optional] [default to all] |
| **adType** | **String**| offer | demand | [optional] [default to offer] |
| **sort** | **String**| relevance|newest|oldest|price_low|price_high | [optional] [default to relevance] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **limit** | **Integer**|  | [optional] [default to 35] |

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


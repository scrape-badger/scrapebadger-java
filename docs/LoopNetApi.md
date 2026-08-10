# LoopNetApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**loopnetGetBrokerProfile**](LoopNetApi.md#loopnetGetBrokerProfile) | **GET** /v1/loopnet/brokers/{slug}/{broker_id} | Get broker profile |
| [**loopnetGetListingDetail**](LoopNetApi.md#loopnetGetListingDetail) | **GET** /v1/loopnet/listings/{listing_id} | Get listing detail |
| [**loopnetListCoverageMarkets**](LoopNetApi.md#loopnetListCoverageMarkets) | **GET** /v1/loopnet/markets | List coverage markets |
| [**loopnetListPropertyTypes**](LoopNetApi.md#loopnetListPropertyTypes) | **GET** /v1/loopnet/property-types | List property types |
| [**loopnetLoopnetScraperHealthCheck**](LoopNetApi.md#loopnetLoopnetScraperHealthCheck) | **GET** /v1/loopnet/health | LoopNet scraper health check |
| [**loopnetLoopnetScraperHealthCheckHead**](LoopNetApi.md#loopnetLoopnetScraperHealthCheckHead) | **HEAD** /v1/loopnet/health | LoopNet scraper health check |
| [**loopnetSearchCommercialRealEstate**](LoopNetApi.md#loopnetSearchCommercialRealEstate) | **GET** /v1/loopnet/search | Search commercial real estate |


<a id="loopnetGetBrokerProfile"></a>
# **loopnetGetBrokerProfile**
> Object loopnetGetBrokerProfile(slug, brokerId, market)

Get broker profile

Get a LoopNet broker profile + their listings by slug + id.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LoopNetApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LoopNetApi apiInstance = new LoopNetApi(defaultClient);
    String slug = "slug_example"; // String | 
    String brokerId = "brokerId_example"; // String | 
    String market = "us"; // String | us|ca|uk|fr|es
    try {
      Object result = apiInstance.loopnetGetBrokerProfile(slug, brokerId, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LoopNetApi#loopnetGetBrokerProfile");
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
| **slug** | **String**|  | |
| **brokerId** | **String**|  | |
| **market** | **String**| us|ca|uk|fr|es | [optional] [default to us] |

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

<a id="loopnetGetListingDetail"></a>
# **loopnetGetListingDetail**
> Object loopnetGetListingDetail(listingId, market)

Get listing detail

Get a single LoopNet listing&#39;s full detail by its numeric id.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LoopNetApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LoopNetApi apiInstance = new LoopNetApi(defaultClient);
    String listingId = "listingId_example"; // String | 
    String market = "us"; // String | us|ca|uk|fr|es
    try {
      Object result = apiInstance.loopnetGetListingDetail(listingId, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LoopNetApi#loopnetGetListingDetail");
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
| **market** | **String**| us|ca|uk|fr|es | [optional] [default to us] |

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

<a id="loopnetListCoverageMarkets"></a>
# **loopnetListCoverageMarkets**
> Object loopnetListCoverageMarkets()

List coverage markets

List LoopNet coverage markets (US, CA, UK, FR, ES).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LoopNetApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LoopNetApi apiInstance = new LoopNetApi(defaultClient);
    try {
      Object result = apiInstance.loopnetListCoverageMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LoopNetApi#loopnetListCoverageMarkets");
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

<a id="loopnetListPropertyTypes"></a>
# **loopnetListPropertyTypes**
> Object loopnetListPropertyTypes()

List property types

List LoopNet property-type facets accepted by /search.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LoopNetApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LoopNetApi apiInstance = new LoopNetApi(defaultClient);
    try {
      Object result = apiInstance.loopnetListPropertyTypes();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LoopNetApi#loopnetListPropertyTypes");
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

<a id="loopnetLoopnetScraperHealthCheck"></a>
# **loopnetLoopnetScraperHealthCheck**
> Object loopnetLoopnetScraperHealthCheck()

LoopNet scraper health check

Check health of the LoopNet scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LoopNetApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LoopNetApi apiInstance = new LoopNetApi(defaultClient);
    try {
      Object result = apiInstance.loopnetLoopnetScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LoopNetApi#loopnetLoopnetScraperHealthCheck");
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

<a id="loopnetLoopnetScraperHealthCheckHead"></a>
# **loopnetLoopnetScraperHealthCheckHead**
> Object loopnetLoopnetScraperHealthCheckHead()

LoopNet scraper health check

Check health of the LoopNet scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LoopNetApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LoopNetApi apiInstance = new LoopNetApi(defaultClient);
    try {
      Object result = apiInstance.loopnetLoopnetScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LoopNetApi#loopnetLoopnetScraperHealthCheckHead");
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

<a id="loopnetSearchCommercialRealEstate"></a>
# **loopnetSearchCommercialRealEstate**
> Object loopnetSearchCommercialRealEstate(location, market, listingType, propertyType, page, minPrice, maxPrice, priceType, minSize, maxSize)

Search commercial real estate

Search LoopNet for-lease / for-sale / auction listings across all markets.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.LoopNetApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    LoopNetApi apiInstance = new LoopNetApi(defaultClient);
    String location = "location_example"; // String | City/state, ZIP, state code, or 'usa'
    String market = "us"; // String | us|ca|uk|fr|es
    String listingType = "for-lease"; // String | for-lease|for-sale|auctions
    String propertyType = "propertyType_example"; // String | Slug from /property-types
    Integer page = 1; // Integer | 
    Integer minPrice = 56; // Integer | 
    Integer maxPrice = 56; // Integer | 
    String priceType = "priceType_example"; // String | unit | sf | acre
    Integer minSize = 56; // Integer | 
    Integer maxSize = 56; // Integer | 
    try {
      Object result = apiInstance.loopnetSearchCommercialRealEstate(location, market, listingType, propertyType, page, minPrice, maxPrice, priceType, minSize, maxSize);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling LoopNetApi#loopnetSearchCommercialRealEstate");
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
| **location** | **String**| City/state, ZIP, state code, or &#39;usa&#39; | |
| **market** | **String**| us|ca|uk|fr|es | [optional] [default to us] |
| **listingType** | **String**| for-lease|for-sale|auctions | [optional] [default to for-lease] |
| **propertyType** | **String**| Slug from /property-types | [optional] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **minPrice** | **Integer**|  | [optional] |
| **maxPrice** | **Integer**|  | [optional] |
| **priceType** | **String**| unit | sf | acre | [optional] |
| **minSize** | **Integer**|  | [optional] |
| **maxSize** | **Integer**|  | [optional] |

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


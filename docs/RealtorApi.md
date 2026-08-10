# RealtorApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**realtorGetFullPropertyDetail**](RealtorApi.md#realtorGetFullPropertyDetail) | **GET** /v1/realtor/properties/{property_id} | Get full property detail |
| [**realtorListMarkets**](RealtorApi.md#realtorListMarkets) | **GET** /v1/realtor/markets | List markets |
| [**realtorLocationAutocomplete**](RealtorApi.md#realtorLocationAutocomplete) | **GET** /v1/realtor/autocomplete | Location autocomplete |
| [**realtorRealtorScraperHealthCheck**](RealtorApi.md#realtorRealtorScraperHealthCheck) | **GET** /v1/realtor/health | Realtor scraper health check |
| [**realtorRealtorScraperHealthCheckHead**](RealtorApi.md#realtorRealtorScraperHealthCheckHead) | **HEAD** /v1/realtor/health | Realtor scraper health check |
| [**realtorSearchPropertyListings**](RealtorApi.md#realtorSearchPropertyListings) | **GET** /v1/realtor/search | Search property listings |


<a id="realtorGetFullPropertyDetail"></a>
# **realtorGetFullPropertyDetail**
> Object realtorGetFullPropertyDetail(propertyId, market)

Get full property detail

Full listing detail: features, tax &amp; price history, schools, photos, agents.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RealtorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RealtorApi apiInstance = new RealtorApi(defaultClient);
    String propertyId = "propertyId_example"; // String | 
    String market = "us"; // String | us (realtor.com) | ca (realtor.ca)
    try {
      Object result = apiInstance.realtorGetFullPropertyDetail(propertyId, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RealtorApi#realtorGetFullPropertyDetail");
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
| **propertyId** | **String**|  | |
| **market** | **String**| us (realtor.com) | ca (realtor.ca) | [optional] [default to us] |

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

<a id="realtorListMarkets"></a>
# **realtorListMarkets**
> Object realtorListMarkets()

List markets

List supported Realtor markets (US &#x3D; realtor.com, CA &#x3D; realtor.ca).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RealtorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RealtorApi apiInstance = new RealtorApi(defaultClient);
    try {
      Object result = apiInstance.realtorListMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RealtorApi#realtorListMarkets");
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

<a id="realtorLocationAutocomplete"></a>
# **realtorLocationAutocomplete**
> Object realtorLocationAutocomplete(query, market, limit)

Location autocomplete

Resolve a location query into candidate places to feed /search.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RealtorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RealtorApi apiInstance = new RealtorApi(defaultClient);
    String query = "query_example"; // String | Freetext location (city, ZIP/postal, address…)
    String market = "us"; // String | us (realtor.com) | ca (realtor.ca)
    Integer limit = 10; // Integer | 
    try {
      Object result = apiInstance.realtorLocationAutocomplete(query, market, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RealtorApi#realtorLocationAutocomplete");
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
| **query** | **String**| Freetext location (city, ZIP/postal, address…) | |
| **market** | **String**| us (realtor.com) | ca (realtor.ca) | [optional] [default to us] |
| **limit** | **Integer**|  | [optional] [default to 10] |

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

<a id="realtorRealtorScraperHealthCheck"></a>
# **realtorRealtorScraperHealthCheck**
> Object realtorRealtorScraperHealthCheck()

Realtor scraper health check

Check health of the realtor scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RealtorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RealtorApi apiInstance = new RealtorApi(defaultClient);
    try {
      Object result = apiInstance.realtorRealtorScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RealtorApi#realtorRealtorScraperHealthCheck");
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

<a id="realtorRealtorScraperHealthCheckHead"></a>
# **realtorRealtorScraperHealthCheckHead**
> Object realtorRealtorScraperHealthCheckHead()

Realtor scraper health check

Check health of the realtor scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RealtorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RealtorApi apiInstance = new RealtorApi(defaultClient);
    try {
      Object result = apiInstance.realtorRealtorScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RealtorApi#realtorRealtorScraperHealthCheckHead");
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

<a id="realtorSearchPropertyListings"></a>
# **realtorSearchPropertyListings**
> Object realtorSearchPropertyListings(location, market, status, priceMin, priceMax, bedsMin, bathsMin, sqftMin, sqftMax, propertyType, sort, page, limit, latMin, latMax, lngMin, lngMax)

Search property listings

Search for-sale/for-rent/sold listings with rich filters.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RealtorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RealtorApi apiInstance = new RealtorApi(defaultClient);
    String location = "location_example"; // String | 'Austin, TX', a ZIP, 'Toronto, ON'…
    String market = "us"; // String | us (realtor.com) | ca (realtor.ca)
    String status = "for_sale"; // String | for_sale | for_rent | sold | pending
    BigDecimal priceMin = new BigDecimal(78); // BigDecimal | 
    BigDecimal priceMax = new BigDecimal(78); // BigDecimal | 
    Integer bedsMin = 56; // Integer | 
    Integer bathsMin = 56; // Integer | 
    Integer sqftMin = 56; // Integer | US only
    Integer sqftMax = 56; // Integer | US only
    String propertyType = "propertyType_example"; // String | US only, CSV of property types
    String sort = "relevant"; // String | relevant | newest | price_low | price_high | photo_count
    Integer page = 1; // Integer | 
    Integer limit = 56; // Integer | 
    BigDecimal latMin = new BigDecimal(78); // BigDecimal | CA bbox south
    BigDecimal latMax = new BigDecimal(78); // BigDecimal | CA bbox north
    BigDecimal lngMin = new BigDecimal(78); // BigDecimal | CA bbox west
    BigDecimal lngMax = new BigDecimal(78); // BigDecimal | CA bbox east
    try {
      Object result = apiInstance.realtorSearchPropertyListings(location, market, status, priceMin, priceMax, bedsMin, bathsMin, sqftMin, sqftMax, propertyType, sort, page, limit, latMin, latMax, lngMin, lngMax);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RealtorApi#realtorSearchPropertyListings");
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
| **location** | **String**| &#39;Austin, TX&#39;, a ZIP, &#39;Toronto, ON&#39;… | [optional] |
| **market** | **String**| us (realtor.com) | ca (realtor.ca) | [optional] [default to us] |
| **status** | **String**| for_sale | for_rent | sold | pending | [optional] [default to for_sale] |
| **priceMin** | **BigDecimal**|  | [optional] |
| **priceMax** | **BigDecimal**|  | [optional] |
| **bedsMin** | **Integer**|  | [optional] |
| **bathsMin** | **Integer**|  | [optional] |
| **sqftMin** | **Integer**| US only | [optional] |
| **sqftMax** | **Integer**| US only | [optional] |
| **propertyType** | **String**| US only, CSV of property types | [optional] |
| **sort** | **String**| relevant | newest | price_low | price_high | photo_count | [optional] [default to relevant] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **limit** | **Integer**|  | [optional] |
| **latMin** | **BigDecimal**| CA bbox south | [optional] |
| **latMax** | **BigDecimal**| CA bbox north | [optional] |
| **lngMin** | **BigDecimal**| CA bbox west | [optional] |
| **lngMax** | **BigDecimal**| CA bbox east | [optional] |

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


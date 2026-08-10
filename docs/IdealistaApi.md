# IdealistaApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**idealistaAgencyByPhone**](IdealistaApi.md#idealistaAgencyByPhone) | **GET** /v1/idealista/agency/by-phone/{phone} | Agency by phone |
| [**idealistaAgencyProfileListings**](IdealistaApi.md#idealistaAgencyProfileListings) | **GET** /v1/idealista/agency/{short_name} | Agency profile + listings |
| [**idealistaGetListingEngagementStats**](IdealistaApi.md#idealistaGetListingEngagementStats) | **GET** /v1/idealista/properties/{property_code}/stats | Get listing engagement stats |
| [**idealistaGetPropertyDetail**](IdealistaApi.md#idealistaGetPropertyDetail) | **GET** /v1/idealista/properties/{property_code} | Get property detail |
| [**idealistaIdealistaScraperHealthCheck**](IdealistaApi.md#idealistaIdealistaScraperHealthCheck) | **GET** /v1/idealista/health | Idealista scraper health check |
| [**idealistaIdealistaScraperHealthCheckHead**](IdealistaApi.md#idealistaIdealistaScraperHealthCheckHead) | **HEAD** /v1/idealista/health | Idealista scraper health check |
| [**idealistaListMarkets**](IdealistaApi.md#idealistaListMarkets) | **GET** /v1/idealista/markets | List markets |
| [**idealistaResolveLocations**](IdealistaApi.md#idealistaResolveLocations) | **GET** /v1/idealista/suggest | Resolve locations |
| [**idealistaSearchAllBeatsResultCap**](IdealistaApi.md#idealistaSearchAllBeatsResultCap) | **GET** /v1/idealista/search/all | Search all (beats result cap) |
| [**idealistaSearchListings**](IdealistaApi.md#idealistaSearchListings) | **GET** /v1/idealista/search | Search listings |


<a id="idealistaAgencyByPhone"></a>
# **idealistaAgencyByPhone**
> Object idealistaAgencyByPhone(phone, market, operation, propertyType, page, maxItems, includeListings)

Agency by phone

Reverse-lookup the agency behind a contact phone (national number), with its listings.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.IdealistaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    IdealistaApi apiInstance = new IdealistaApi(defaultClient);
    String phone = "phone_example"; // String | 
    String market = "es"; // String | es|it|pt
    String operation = "operation_example"; // String | sale|rent
    String propertyType = "propertyType_example"; // String | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms
    Integer page = 1; // Integer | 
    Integer maxItems = 30; // Integer | 
    Boolean includeListings = true; // Boolean | 
    try {
      Object result = apiInstance.idealistaAgencyByPhone(phone, market, operation, propertyType, page, maxItems, includeListings);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IdealistaApi#idealistaAgencyByPhone");
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
| **phone** | **String**|  | |
| **market** | **String**| es|it|pt | [optional] [default to es] |
| **operation** | **String**| sale|rent | [optional] |
| **propertyType** | **String**| homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **maxItems** | **Integer**|  | [optional] [default to 30] |
| **includeListings** | **Boolean**|  | [optional] [default to true] |

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

<a id="idealistaAgencyProfileListings"></a>
# **idealistaAgencyProfileListings**
> Object idealistaAgencyProfileListings(shortName, market, operation, propertyType, page, maxItems, includeListings)

Agency profile + listings

An agency&#39;s microsite profile plus a page of its listings (by URL-slug shortName).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.IdealistaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    IdealistaApi apiInstance = new IdealistaApi(defaultClient);
    String shortName = "shortName_example"; // String | 
    String market = "es"; // String | es|it|pt
    String operation = "operation_example"; // String | sale|rent
    String propertyType = "propertyType_example"; // String | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms
    Integer page = 1; // Integer | 
    Integer maxItems = 30; // Integer | 
    Boolean includeListings = true; // Boolean | 
    try {
      Object result = apiInstance.idealistaAgencyProfileListings(shortName, market, operation, propertyType, page, maxItems, includeListings);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IdealistaApi#idealistaAgencyProfileListings");
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
| **shortName** | **String**|  | |
| **market** | **String**| es|it|pt | [optional] [default to es] |
| **operation** | **String**| sale|rent | [optional] |
| **propertyType** | **String**| homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **maxItems** | **Integer**|  | [optional] [default to 30] |
| **includeListings** | **Boolean**|  | [optional] [default to true] |

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

<a id="idealistaGetListingEngagementStats"></a>
# **idealistaGetListingEngagementStats**
> Object idealistaGetListingEngagementStats(propertyCode, market, locale)

Get listing engagement stats

Engagement counters for a listing: views, email contacts, sent-to-friend, favourites.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.IdealistaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    IdealistaApi apiInstance = new IdealistaApi(defaultClient);
    String propertyCode = "propertyCode_example"; // String | 
    String market = "es"; // String | es|it|pt
    String locale = "en"; // String | Language for stat labels
    try {
      Object result = apiInstance.idealistaGetListingEngagementStats(propertyCode, market, locale);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IdealistaApi#idealistaGetListingEngagementStats");
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
| **propertyCode** | **String**|  | |
| **market** | **String**| es|it|pt | [optional] [default to es] |
| **locale** | **String**| Language for stat labels | [optional] [default to en] |

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

<a id="idealistaGetPropertyDetail"></a>
# **idealistaGetPropertyDetail**
> Object idealistaGetPropertyDetail(propertyCode, market, locale)

Get property detail

Get a single Idealista listing&#39;s full detail (energy cert, characteristics, media).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.IdealistaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    IdealistaApi apiInstance = new IdealistaApi(defaultClient);
    String propertyCode = "propertyCode_example"; // String | 
    String market = "es"; // String | es|it|pt
    String locale = "en"; // String | Response language (en, es, it, pt)
    try {
      Object result = apiInstance.idealistaGetPropertyDetail(propertyCode, market, locale);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IdealistaApi#idealistaGetPropertyDetail");
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
| **propertyCode** | **String**|  | |
| **market** | **String**| es|it|pt | [optional] [default to es] |
| **locale** | **String**| Response language (en, es, it, pt) | [optional] [default to en] |

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

<a id="idealistaIdealistaScraperHealthCheck"></a>
# **idealistaIdealistaScraperHealthCheck**
> Object idealistaIdealistaScraperHealthCheck()

Idealista scraper health check

Check health of the Idealista scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.IdealistaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    IdealistaApi apiInstance = new IdealistaApi(defaultClient);
    try {
      Object result = apiInstance.idealistaIdealistaScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IdealistaApi#idealistaIdealistaScraperHealthCheck");
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

<a id="idealistaIdealistaScraperHealthCheckHead"></a>
# **idealistaIdealistaScraperHealthCheckHead**
> Object idealistaIdealistaScraperHealthCheckHead()

Idealista scraper health check

Check health of the Idealista scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.IdealistaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    IdealistaApi apiInstance = new IdealistaApi(defaultClient);
    try {
      Object result = apiInstance.idealistaIdealistaScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IdealistaApi#idealistaIdealistaScraperHealthCheckHead");
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

<a id="idealistaListMarkets"></a>
# **idealistaListMarkets**
> Object idealistaListMarkets()

List markets

List supported Idealista markets (ES, IT, PT).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.IdealistaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    IdealistaApi apiInstance = new IdealistaApi(defaultClient);
    try {
      Object result = apiInstance.idealistaListMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IdealistaApi#idealistaListMarkets");
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

<a id="idealistaResolveLocations"></a>
# **idealistaResolveLocations**
> Object idealistaResolveLocations(query, operation, propertyType, market, locale)

Resolve locations

Resolve a free-text query into Idealista location codes for a search.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.IdealistaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    IdealistaApi apiInstance = new IdealistaApi(defaultClient);
    String query = "query_example"; // String | Free-text location, e.g. 'sagrada familia'
    String operation = "sale"; // String | sale|rent
    String propertyType = "homes"; // String | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms
    String market = "es"; // String | es|it|pt
    String locale = "locale_example"; // String | Response language (en, es, it, pt)
    try {
      Object result = apiInstance.idealistaResolveLocations(query, operation, propertyType, market, locale);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IdealistaApi#idealistaResolveLocations");
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
| **query** | **String**| Free-text location, e.g. &#39;sagrada familia&#39; | |
| **operation** | **String**| sale|rent | [optional] [default to sale] |
| **propertyType** | **String**| homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] [default to homes] |
| **market** | **String**| es|it|pt | [optional] [default to es] |
| **locale** | **String**| Response language (en, es, it, pt) | [optional] |

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

<a id="idealistaSearchAllBeatsResultCap"></a>
# **idealistaSearchAllBeatsResultCap**
> Object idealistaSearchAllBeatsResultCap(location, operation, propertyType, market, maxResults, minPrice, maxPrice, minSize, maxSize, minRooms, maxRooms, locale)

Search all (beats result cap)

Full inventory for a location, beating Idealista&#39;s ~1800 per-search cap via price-range tiling (deduped). Billed per page fetched.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.IdealistaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    IdealistaApi apiInstance = new IdealistaApi(defaultClient);
    String location = "location_example"; // String | Idealista location code (from /suggest)
    String operation = "sale"; // String | sale|rent
    String propertyType = "homes"; // String | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms
    String market = "es"; // String | es|it|pt
    Integer maxResults = 500; // Integer | 
    BigDecimal minPrice = new BigDecimal(78); // BigDecimal | 
    BigDecimal maxPrice = new BigDecimal(78); // BigDecimal | 
    BigDecimal minSize = new BigDecimal(78); // BigDecimal | 
    BigDecimal maxSize = new BigDecimal(78); // BigDecimal | 
    Integer minRooms = 56; // Integer | 
    Integer maxRooms = 56; // Integer | 
    String locale = "locale_example"; // String | Response language (en, es, it, pt)
    try {
      Object result = apiInstance.idealistaSearchAllBeatsResultCap(location, operation, propertyType, market, maxResults, minPrice, maxPrice, minSize, maxSize, minRooms, maxRooms, locale);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IdealistaApi#idealistaSearchAllBeatsResultCap");
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
| **location** | **String**| Idealista location code (from /suggest) | |
| **operation** | **String**| sale|rent | [optional] [default to sale] |
| **propertyType** | **String**| homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] [default to homes] |
| **market** | **String**| es|it|pt | [optional] [default to es] |
| **maxResults** | **Integer**|  | [optional] [default to 500] |
| **minPrice** | **BigDecimal**|  | [optional] |
| **maxPrice** | **BigDecimal**|  | [optional] |
| **minSize** | **BigDecimal**|  | [optional] |
| **maxSize** | **BigDecimal**|  | [optional] |
| **minRooms** | **Integer**|  | [optional] |
| **maxRooms** | **Integer**|  | [optional] |
| **locale** | **String**| Response language (en, es, it, pt) | [optional] |

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

<a id="idealistaSearchListings"></a>
# **idealistaSearchListings**
> Object idealistaSearchListings(location, operation, propertyType, market, page, maxItems, sortBy, sortOrder, minPrice, maxPrice, minSize, maxSize, minRooms, maxRooms, locale)

Search listings

Search Idealista real-estate listings by location code.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.IdealistaApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    IdealistaApi apiInstance = new IdealistaApi(defaultClient);
    String location = "location_example"; // String | Idealista location code (from /suggest)
    String operation = "sale"; // String | sale|rent
    String propertyType = "homes"; // String | homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms
    String market = "es"; // String | es|it|pt
    Integer page = 1; // Integer | 
    Integer maxItems = 30; // Integer | 
    String sortBy = "sortBy_example"; // String | distance|size|rooms|floor|ratioeurm2|price|street|photos|modificationDate|publicationDate|weigh|priceDown|preservationTypeAndPrice|privateAds
    String sortOrder = "desc"; // String | asc|desc
    BigDecimal minPrice = new BigDecimal(78); // BigDecimal | 
    BigDecimal maxPrice = new BigDecimal(78); // BigDecimal | 
    BigDecimal minSize = new BigDecimal(78); // BigDecimal | 
    BigDecimal maxSize = new BigDecimal(78); // BigDecimal | 
    Integer minRooms = 56; // Integer | 
    Integer maxRooms = 56; // Integer | 
    String locale = "locale_example"; // String | Response language (en, es, it, pt)
    try {
      Object result = apiInstance.idealistaSearchListings(location, operation, propertyType, market, page, maxItems, sortBy, sortOrder, minPrice, maxPrice, minSize, maxSize, minRooms, maxRooms, locale);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling IdealistaApi#idealistaSearchListings");
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
| **location** | **String**| Idealista location code (from /suggest) | |
| **operation** | **String**| sale|rent | [optional] [default to sale] |
| **propertyType** | **String**| homes|offices|premises|garages|newDevelopments|lands|storageRooms|buildings|bedrooms | [optional] [default to homes] |
| **market** | **String**| es|it|pt | [optional] [default to es] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **maxItems** | **Integer**|  | [optional] [default to 30] |
| **sortBy** | **String**| distance|size|rooms|floor|ratioeurm2|price|street|photos|modificationDate|publicationDate|weigh|priceDown|preservationTypeAndPrice|privateAds | [optional] |
| **sortOrder** | **String**| asc|desc | [optional] [default to desc] |
| **minPrice** | **BigDecimal**|  | [optional] |
| **maxPrice** | **BigDecimal**|  | [optional] |
| **minSize** | **BigDecimal**|  | [optional] |
| **maxSize** | **BigDecimal**|  | [optional] |
| **minRooms** | **Integer**|  | [optional] |
| **maxRooms** | **Integer**|  | [optional] |
| **locale** | **String**| Response language (en, es, it, pt) | [optional] |

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


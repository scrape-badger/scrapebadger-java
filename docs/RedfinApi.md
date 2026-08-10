# RedfinApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**redfinGetAgentProfileListings**](RedfinApi.md#redfinGetAgentProfileListings) | **GET** /v1/redfin/agent | Get agent profile + listings |
| [**redfinGetPropertyDetail**](RedfinApi.md#redfinGetPropertyDetail) | **GET** /v1/redfin/property/{property_id} | Get property detail |
| [**redfinGetPropertyDetailByUrl**](RedfinApi.md#redfinGetPropertyDetailByUrl) | **GET** /v1/redfin/property | Get property detail by URL |
| [**redfinListCoverageMarkets**](RedfinApi.md#redfinListCoverageMarkets) | **GET** /v1/redfin/markets | List coverage markets |
| [**redfinRedfinScraperHealthCheck**](RedfinApi.md#redfinRedfinScraperHealthCheck) | **GET** /v1/redfin/health | Redfin scraper health check |
| [**redfinRedfinScraperHealthCheckHead**](RedfinApi.md#redfinRedfinScraperHealthCheckHead) | **HEAD** /v1/redfin/health | Redfin scraper health check |
| [**redfinRegionAddressSuggestions**](RedfinApi.md#redfinRegionAddressSuggestions) | **GET** /v1/redfin/autocomplete | Region/address suggestions |
| [**redfinSearchProperties**](RedfinApi.md#redfinSearchProperties) | **GET** /v1/redfin/search | Search properties |


<a id="redfinGetAgentProfileListings"></a>
# **redfinGetAgentProfileListings**
> Object redfinGetAgentProfileListings(url, agentId)

Get agent profile + listings

Get a Redfin real-estate agent&#39;s profile and their active listings.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedfinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedfinApi apiInstance = new RedfinApi(defaultClient);
    String url = "url_example"; // String | Full Redfin /realestateagents/ URL
    String agentId = "agentId_example"; // String | Redfin agent id
    try {
      Object result = apiInstance.redfinGetAgentProfileListings(url, agentId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedfinApi#redfinGetAgentProfileListings");
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
| **url** | **String**| Full Redfin /realestateagents/ URL | [optional] |
| **agentId** | **String**| Redfin agent id | [optional] |

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

<a id="redfinGetPropertyDetail"></a>
# **redfinGetPropertyDetail**
> Object redfinGetPropertyDetail(propertyId)

Get property detail

Get a single Redfin property&#39;s full detail by its numeric propertyId.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedfinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedfinApi apiInstance = new RedfinApi(defaultClient);
    String propertyId = "propertyId_example"; // String | 
    try {
      Object result = apiInstance.redfinGetPropertyDetail(propertyId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedfinApi#redfinGetPropertyDetail");
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

<a id="redfinGetPropertyDetailByUrl"></a>
# **redfinGetPropertyDetailByUrl**
> Object redfinGetPropertyDetailByUrl(url)

Get property detail by URL

Get a single Redfin property&#39;s full detail by its home URL.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedfinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedfinApi apiInstance = new RedfinApi(defaultClient);
    String url = "url_example"; // String | Full Redfin property URL (/CA/City/.../home/12345678)
    try {
      Object result = apiInstance.redfinGetPropertyDetailByUrl(url);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedfinApi#redfinGetPropertyDetailByUrl");
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
| **url** | **String**| Full Redfin property URL (/CA/City/.../home/12345678) | |

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

<a id="redfinListCoverageMarkets"></a>
# **redfinListCoverageMarkets**
> Object redfinListCoverageMarkets()

List coverage markets

List Redfin coverage regions (US).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedfinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedfinApi apiInstance = new RedfinApi(defaultClient);
    try {
      Object result = apiInstance.redfinListCoverageMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedfinApi#redfinListCoverageMarkets");
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

<a id="redfinRedfinScraperHealthCheck"></a>
# **redfinRedfinScraperHealthCheck**
> Object redfinRedfinScraperHealthCheck()

Redfin scraper health check

Check health of the Redfin scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedfinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedfinApi apiInstance = new RedfinApi(defaultClient);
    try {
      Object result = apiInstance.redfinRedfinScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedfinApi#redfinRedfinScraperHealthCheck");
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

<a id="redfinRedfinScraperHealthCheckHead"></a>
# **redfinRedfinScraperHealthCheckHead**
> Object redfinRedfinScraperHealthCheckHead()

Redfin scraper health check

Check health of the Redfin scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedfinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedfinApi apiInstance = new RedfinApi(defaultClient);
    try {
      Object result = apiInstance.redfinRedfinScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedfinApi#redfinRedfinScraperHealthCheckHead");
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

<a id="redfinRegionAddressSuggestions"></a>
# **redfinRegionAddressSuggestions**
> Object redfinRegionAddressSuggestions(query)

Region/address suggestions

Resolve a search term to Redfin regions/addresses.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedfinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedfinApi apiInstance = new RedfinApi(defaultClient);
    String query = "query_example"; // String | Partial location — city, ZIP, address, neighborhood
    try {
      Object result = apiInstance.redfinRegionAddressSuggestions(query);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedfinApi#redfinRegionAddressSuggestions");
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
| **query** | **String**| Partial location — city, ZIP, address, neighborhood | |

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

<a id="redfinSearchProperties"></a>
# **redfinSearchProperties**
> Object redfinSearchProperties(location, page, sort, priceMin, priceMax, bedsMin, bathsMin, homeType, sqftMin, sqftMax, lotMin, lotMax, yearBuiltMin, yearBuiltMax, maxDaysOnMarket, north, south, east, west)

Search properties

Search Redfin for for-sale / for-rent / recently-sold properties.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.RedfinApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    RedfinApi apiInstance = new RedfinApi(defaultClient);
    String location = "location_example"; // String | City/state, ZIP, address or neighborhood
    Integer page = 1; // Integer | 
    String sort = "sort_example"; // String | relevant|newest|price_high_to_low|price_low_to_high|square_feet|lot_size|price_per_sqft|beds|baths
    Integer priceMin = 56; // Integer | 
    Integer priceMax = 56; // Integer | 
    Integer bedsMin = 56; // Integer | 
    BigDecimal bathsMin = new BigDecimal(78); // BigDecimal | 
    String homeType = "homeType_example"; // String | house|condo|townhouse|multi_family|land|mobile|coop|other
    Integer sqftMin = 56; // Integer | 
    Integer sqftMax = 56; // Integer | 
    Integer lotMin = 56; // Integer | 
    Integer lotMax = 56; // Integer | 
    Integer yearBuiltMin = 56; // Integer | 
    Integer yearBuiltMax = 56; // Integer | 
    Integer maxDaysOnMarket = 56; // Integer | 
    BigDecimal north = new BigDecimal(78); // BigDecimal | Map bounds for tiling past the cap
    BigDecimal south = new BigDecimal(78); // BigDecimal | 
    BigDecimal east = new BigDecimal(78); // BigDecimal | 
    BigDecimal west = new BigDecimal(78); // BigDecimal | 
    try {
      Object result = apiInstance.redfinSearchProperties(location, page, sort, priceMin, priceMax, bedsMin, bathsMin, homeType, sqftMin, sqftMax, lotMin, lotMax, yearBuiltMin, yearBuiltMax, maxDaysOnMarket, north, south, east, west);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling RedfinApi#redfinSearchProperties");
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
| **location** | **String**| City/state, ZIP, address or neighborhood | |
| **page** | **Integer**|  | [optional] [default to 1] |
| **sort** | **String**| relevant|newest|price_high_to_low|price_low_to_high|square_feet|lot_size|price_per_sqft|beds|baths | [optional] |
| **priceMin** | **Integer**|  | [optional] |
| **priceMax** | **Integer**|  | [optional] |
| **bedsMin** | **Integer**|  | [optional] |
| **bathsMin** | **BigDecimal**|  | [optional] |
| **homeType** | **String**| house|condo|townhouse|multi_family|land|mobile|coop|other | [optional] |
| **sqftMin** | **Integer**|  | [optional] |
| **sqftMax** | **Integer**|  | [optional] |
| **lotMin** | **Integer**|  | [optional] |
| **lotMax** | **Integer**|  | [optional] |
| **yearBuiltMin** | **Integer**|  | [optional] |
| **yearBuiltMax** | **Integer**|  | [optional] |
| **maxDaysOnMarket** | **Integer**|  | [optional] |
| **north** | **BigDecimal**| Map bounds for tiling past the cap | [optional] |
| **south** | **BigDecimal**|  | [optional] |
| **east** | **BigDecimal**|  | [optional] |
| **west** | **BigDecimal**|  | [optional] |

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


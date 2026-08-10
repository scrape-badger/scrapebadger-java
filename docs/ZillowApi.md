# ZillowApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**zillowGetAgentProfileListings**](ZillowApi.md#zillowGetAgentProfileListings) | **GET** /v1/zillow/agent | Get agent profile + listings |
| [**zillowGetPropertyDetail**](ZillowApi.md#zillowGetPropertyDetail) | **GET** /v1/zillow/property/{zpid} | Get property detail |
| [**zillowGetPropertyDetailByUrl**](ZillowApi.md#zillowGetPropertyDetailByUrl) | **GET** /v1/zillow/property | Get property detail by URL |
| [**zillowListCoverageMarkets**](ZillowApi.md#zillowListCoverageMarkets) | **GET** /v1/zillow/markets | List coverage markets |
| [**zillowRegionAddressSuggestions**](ZillowApi.md#zillowRegionAddressSuggestions) | **GET** /v1/zillow/autocomplete | Region/address suggestions |
| [**zillowSearchProperties**](ZillowApi.md#zillowSearchProperties) | **GET** /v1/zillow/search | Search properties |
| [**zillowZillowScraperHealthCheck**](ZillowApi.md#zillowZillowScraperHealthCheck) | **GET** /v1/zillow/health | Zillow scraper health check |
| [**zillowZillowScraperHealthCheckHead**](ZillowApi.md#zillowZillowScraperHealthCheckHead) | **HEAD** /v1/zillow/health | Zillow scraper health check |


<a id="zillowGetAgentProfileListings"></a>
# **zillowGetAgentProfileListings**
> Object zillowGetAgentProfileListings(username, url)

Get agent profile + listings

Get a Zillow professional&#39;s profile and their active listings.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ZillowApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ZillowApi apiInstance = new ZillowApi(defaultClient);
    String username = "username_example"; // String | Zillow profile username
    String url = "url_example"; // String | Full Zillow /profile/... URL
    try {
      Object result = apiInstance.zillowGetAgentProfileListings(username, url);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ZillowApi#zillowGetAgentProfileListings");
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
| **username** | **String**| Zillow profile username | [optional] |
| **url** | **String**| Full Zillow /profile/... URL | [optional] |

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

<a id="zillowGetPropertyDetail"></a>
# **zillowGetPropertyDetail**
> Object zillowGetPropertyDetail(zpid)

Get property detail

Get a single Zillow property&#39;s full detail by zpid.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ZillowApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ZillowApi apiInstance = new ZillowApi(defaultClient);
    String zpid = "zpid_example"; // String | 
    try {
      Object result = apiInstance.zillowGetPropertyDetail(zpid);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ZillowApi#zillowGetPropertyDetail");
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
| **zpid** | **String**|  | |

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

<a id="zillowGetPropertyDetailByUrl"></a>
# **zillowGetPropertyDetailByUrl**
> Object zillowGetPropertyDetailByUrl(url)

Get property detail by URL

Get a single Zillow property&#39;s full detail by its homedetails URL.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ZillowApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ZillowApi apiInstance = new ZillowApi(defaultClient);
    String url = "url_example"; // String | Full Zillow /homedetails/... URL
    try {
      Object result = apiInstance.zillowGetPropertyDetailByUrl(url);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ZillowApi#zillowGetPropertyDetailByUrl");
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
| **url** | **String**| Full Zillow /homedetails/... URL | |

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

<a id="zillowListCoverageMarkets"></a>
# **zillowListCoverageMarkets**
> Object zillowListCoverageMarkets()

List coverage markets

List Zillow coverage regions (US + Canada).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ZillowApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ZillowApi apiInstance = new ZillowApi(defaultClient);
    try {
      Object result = apiInstance.zillowListCoverageMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ZillowApi#zillowListCoverageMarkets");
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

<a id="zillowRegionAddressSuggestions"></a>
# **zillowRegionAddressSuggestions**
> Object zillowRegionAddressSuggestions(query)

Region/address suggestions

Resolve a search term to Zillow regions/addresses.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ZillowApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ZillowApi apiInstance = new ZillowApi(defaultClient);
    String query = "query_example"; // String | Partial location — city, ZIP, address, neighborhood
    try {
      Object result = apiInstance.zillowRegionAddressSuggestions(query);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ZillowApi#zillowRegionAddressSuggestions");
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

<a id="zillowSearchProperties"></a>
# **zillowSearchProperties**
> Object zillowSearchProperties(location, status, page, sort, priceMin, priceMax, bedsMin, bathsMin, homeType, sqftMin, sqftMax, lotMin, lotMax, yearBuiltMin, yearBuiltMax, hoaMax, keywords, daysOn, north, south, east, west)

Search properties

Search Zillow for for-sale / for-rent / recently-sold properties.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ZillowApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ZillowApi apiInstance = new ZillowApi(defaultClient);
    String location = "location_example"; // String | City/state, ZIP, address or neighborhood
    String status = "for_sale"; // String | for_sale|for_rent|sold
    Integer page = 1; // Integer | 
    String sort = "sort_example"; // String | homes_for_you|newest|price_high_to_low|price_low_to_high|bedrooms|bathrooms|square_feet|lot_size|year_built
    Integer priceMin = 56; // Integer | 
    Integer priceMax = 56; // Integer | 
    Integer bedsMin = 56; // Integer | 
    BigDecimal bathsMin = new BigDecimal(78); // BigDecimal | 
    String homeType = "homeType_example"; // String | houses|condos|townhomes|apartments|manufactured|lots|multi_family
    Integer sqftMin = 56; // Integer | 
    Integer sqftMax = 56; // Integer | 
    Integer lotMin = 56; // Integer | 
    Integer lotMax = 56; // Integer | 
    Integer yearBuiltMin = 56; // Integer | 
    Integer yearBuiltMax = 56; // Integer | 
    Integer hoaMax = 56; // Integer | 
    String keywords = "keywords_example"; // String | 
    String daysOn = "daysOn_example"; // String | 
    BigDecimal north = new BigDecimal(78); // BigDecimal | Map bounds for tiling past the 820 cap
    BigDecimal south = new BigDecimal(78); // BigDecimal | 
    BigDecimal east = new BigDecimal(78); // BigDecimal | 
    BigDecimal west = new BigDecimal(78); // BigDecimal | 
    try {
      Object result = apiInstance.zillowSearchProperties(location, status, page, sort, priceMin, priceMax, bedsMin, bathsMin, homeType, sqftMin, sqftMax, lotMin, lotMax, yearBuiltMin, yearBuiltMax, hoaMax, keywords, daysOn, north, south, east, west);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ZillowApi#zillowSearchProperties");
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
| **status** | **String**| for_sale|for_rent|sold | [optional] [default to for_sale] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **sort** | **String**| homes_for_you|newest|price_high_to_low|price_low_to_high|bedrooms|bathrooms|square_feet|lot_size|year_built | [optional] |
| **priceMin** | **Integer**|  | [optional] |
| **priceMax** | **Integer**|  | [optional] |
| **bedsMin** | **Integer**|  | [optional] |
| **bathsMin** | **BigDecimal**|  | [optional] |
| **homeType** | **String**| houses|condos|townhomes|apartments|manufactured|lots|multi_family | [optional] |
| **sqftMin** | **Integer**|  | [optional] |
| **sqftMax** | **Integer**|  | [optional] |
| **lotMin** | **Integer**|  | [optional] |
| **lotMax** | **Integer**|  | [optional] |
| **yearBuiltMin** | **Integer**|  | [optional] |
| **yearBuiltMax** | **Integer**|  | [optional] |
| **hoaMax** | **Integer**|  | [optional] |
| **keywords** | **String**|  | [optional] |
| **daysOn** | **String**|  | [optional] |
| **north** | **BigDecimal**| Map bounds for tiling past the 820 cap | [optional] |
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

<a id="zillowZillowScraperHealthCheck"></a>
# **zillowZillowScraperHealthCheck**
> Object zillowZillowScraperHealthCheck()

Zillow scraper health check

Check health of the Zillow scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ZillowApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ZillowApi apiInstance = new ZillowApi(defaultClient);
    try {
      Object result = apiInstance.zillowZillowScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ZillowApi#zillowZillowScraperHealthCheck");
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

<a id="zillowZillowScraperHealthCheckHead"></a>
# **zillowZillowScraperHealthCheckHead**
> Object zillowZillowScraperHealthCheckHead()

Zillow scraper health check

Check health of the Zillow scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ZillowApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ZillowApi apiInstance = new ZillowApi(defaultClient);
    try {
      Object result = apiInstance.zillowZillowScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ZillowApi#zillowZillowScraperHealthCheckHead");
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


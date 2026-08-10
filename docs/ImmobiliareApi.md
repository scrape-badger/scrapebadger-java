# ImmobiliareApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**immobiliareGetAgencyProfile**](ImmobiliareApi.md#immobiliareGetAgencyProfile) | **GET** /v1/immobiliare/agencies/{agency_id} | Get agency profile |
| [**immobiliareGetAnAgencySListings**](ImmobiliareApi.md#immobiliareGetAnAgencySListings) | **GET** /v1/immobiliare/agencies/{agency_id}/listings | Get an agency&#39;s listings |
| [**immobiliareGetListingDetail**](ImmobiliareApi.md#immobiliareGetListingDetail) | **GET** /v1/immobiliare/listings/{listing_id} | Get listing detail |
| [**immobiliareImmobiliareScraperHealthCheck**](ImmobiliareApi.md#immobiliareImmobiliareScraperHealthCheck) | **GET** /v1/immobiliare/health | Immobiliare scraper health check |
| [**immobiliareImmobiliareScraperHealthCheckHead**](ImmobiliareApi.md#immobiliareImmobiliareScraperHealthCheckHead) | **HEAD** /v1/immobiliare/health | Immobiliare scraper health check |
| [**immobiliareListFilterEnums**](ImmobiliareApi.md#immobiliareListFilterEnums) | **GET** /v1/immobiliare/reference | List filter enums |
| [**immobiliareListMarkets**](ImmobiliareApi.md#immobiliareListMarkets) | **GET** /v1/immobiliare/markets | List markets |
| [**immobiliareLocationAutocomplete**](ImmobiliareApi.md#immobiliareLocationAutocomplete) | **GET** /v1/immobiliare/autocomplete | Location autocomplete |
| [**immobiliarePriceMTimeSeries**](ImmobiliareApi.md#immobiliarePriceMTimeSeries) | **GET** /v1/immobiliare/market-insights/prices | Price €/m² time series |
| [**immobiliareSearchListings**](ImmobiliareApi.md#immobiliareSearchListings) | **GET** /v1/immobiliare/search | Search listings |


<a id="immobiliareGetAgencyProfile"></a>
# **immobiliareGetAgencyProfile**
> Object immobiliareGetAgencyProfile(agencyId, market)

Get agency profile

Public agency/advertiser profile.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ImmobiliareApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ImmobiliareApi apiInstance = new ImmobiliareApi(defaultClient);
    Integer agencyId = 56; // Integer | 
    String market = "it"; // String | it | es | gr | lu
    try {
      Object result = apiInstance.immobiliareGetAgencyProfile(agencyId, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImmobiliareApi#immobiliareGetAgencyProfile");
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
| **agencyId** | **Integer**|  | |
| **market** | **String**| it | es | gr | lu | [optional] [default to it] |

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

<a id="immobiliareGetAnAgencySListings"></a>
# **immobiliareGetAnAgencySListings**
> Object immobiliareGetAnAgencySListings(agencyId, market, contract, page)

Get an agency&#39;s listings

An agency&#39;s active listings.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ImmobiliareApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ImmobiliareApi apiInstance = new ImmobiliareApi(defaultClient);
    Integer agencyId = 56; // Integer | 
    String market = "it"; // String | it | es | gr | lu
    String contract = "sale"; // String | sale | rent
    Integer page = 1; // Integer | 
    try {
      Object result = apiInstance.immobiliareGetAnAgencySListings(agencyId, market, contract, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImmobiliareApi#immobiliareGetAnAgencySListings");
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
| **agencyId** | **Integer**|  | |
| **market** | **String**| it | es | gr | lu | [optional] [default to it] |
| **contract** | **String**| sale | rent | [optional] [default to sale] |
| **page** | **Integer**|  | [optional] [default to 1] |

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

<a id="immobiliareGetListingDetail"></a>
# **immobiliareGetListingDetail**
> Object immobiliareGetListingDetail(listingId, market)

Get listing detail

Full detail for a single listing.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ImmobiliareApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ImmobiliareApi apiInstance = new ImmobiliareApi(defaultClient);
    Integer listingId = 56; // Integer | 
    String market = "it"; // String | it | es | gr | lu
    try {
      Object result = apiInstance.immobiliareGetListingDetail(listingId, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImmobiliareApi#immobiliareGetListingDetail");
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
| **listingId** | **Integer**|  | |
| **market** | **String**| it | es | gr | lu | [optional] [default to it] |

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

<a id="immobiliareImmobiliareScraperHealthCheck"></a>
# **immobiliareImmobiliareScraperHealthCheck**
> Object immobiliareImmobiliareScraperHealthCheck()

Immobiliare scraper health check

Check health of the Immobiliare scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ImmobiliareApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ImmobiliareApi apiInstance = new ImmobiliareApi(defaultClient);
    try {
      Object result = apiInstance.immobiliareImmobiliareScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImmobiliareApi#immobiliareImmobiliareScraperHealthCheck");
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

<a id="immobiliareImmobiliareScraperHealthCheckHead"></a>
# **immobiliareImmobiliareScraperHealthCheckHead**
> Object immobiliareImmobiliareScraperHealthCheckHead()

Immobiliare scraper health check

Check health of the Immobiliare scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ImmobiliareApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ImmobiliareApi apiInstance = new ImmobiliareApi(defaultClient);
    try {
      Object result = apiInstance.immobiliareImmobiliareScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImmobiliareApi#immobiliareImmobiliareScraperHealthCheckHead");
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

<a id="immobiliareListFilterEnums"></a>
# **immobiliareListFilterEnums**
> Object immobiliareListFilterEnums()

List filter enums

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ImmobiliareApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ImmobiliareApi apiInstance = new ImmobiliareApi(defaultClient);
    try {
      Object result = apiInstance.immobiliareListFilterEnums();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImmobiliareApi#immobiliareListFilterEnums");
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

<a id="immobiliareListMarkets"></a>
# **immobiliareListMarkets**
> Object immobiliareListMarkets()

List markets

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ImmobiliareApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ImmobiliareApi apiInstance = new ImmobiliareApi(defaultClient);
    try {
      Object result = apiInstance.immobiliareListMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImmobiliareApi#immobiliareListMarkets");
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

<a id="immobiliareLocationAutocomplete"></a>
# **immobiliareLocationAutocomplete**
> Object immobiliareLocationAutocomplete(query, market)

Location autocomplete

Resolve a place name to region/province/city ids usable in search.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ImmobiliareApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ImmobiliareApi apiInstance = new ImmobiliareApi(defaultClient);
    String query = "query_example"; // String | Free-text place name, e.g. 'Milano'
    String market = "it"; // String | it | es | gr | lu
    try {
      Object result = apiInstance.immobiliareLocationAutocomplete(query, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImmobiliareApi#immobiliareLocationAutocomplete");
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
| **query** | **String**| Free-text place name, e.g. &#39;Milano&#39; | |
| **market** | **String**| it | es | gr | lu | [optional] [default to it] |

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

<a id="immobiliarePriceMTimeSeries"></a>
# **immobiliarePriceMTimeSeries**
> Object immobiliarePriceMTimeSeries(regionId, market, provinceId, cityId, contract)

Price €/m² time series

Historical €/m² price statistics for an area.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ImmobiliareApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ImmobiliareApi apiInstance = new ImmobiliareApi(defaultClient);
    String regionId = "regionId_example"; // String | Region id, e.g. 'lom'
    String market = "it"; // String | it | es | gr | lu
    String provinceId = "provinceId_example"; // String | Province id, e.g. 'MI'
    String cityId = "cityId_example"; // String | City id (idComune)
    String contract = "sale"; // String | sale | rent
    try {
      Object result = apiInstance.immobiliarePriceMTimeSeries(regionId, market, provinceId, cityId, contract);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImmobiliareApi#immobiliarePriceMTimeSeries");
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
| **regionId** | **String**| Region id, e.g. &#39;lom&#39; | |
| **market** | **String**| it | es | gr | lu | [optional] [default to it] |
| **provinceId** | **String**| Province id, e.g. &#39;MI&#39; | [optional] |
| **cityId** | **String**| City id (idComune) | [optional] |
| **contract** | **String**| sale | rent | [optional] [default to sale] |

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

<a id="immobiliareSearchListings"></a>
# **immobiliareSearchListings**
> Object immobiliareSearchListings(market, location, regionId, provinceId, cityId, contract, category, priceMin, priceMax, surfaceMin, surfaceMax, roomsMin, roomsMax, bathroomsMin, sort, page)

Search listings

Search Immobiliare-group listings (scope by location + contract + filters).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ImmobiliareApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ImmobiliareApi apiInstance = new ImmobiliareApi(defaultClient);
    String market = "it"; // String | it | es | gr | lu
    String location = "location_example"; // String | Free-text place (auto-resolved)
    String regionId = "regionId_example"; // String | fkRegione (from /autocomplete)
    String provinceId = "provinceId_example"; // String | idProvincia (from /autocomplete)
    String cityId = "cityId_example"; // String | idComune (from /autocomplete)
    String contract = "sale"; // String | sale | rent
    String category = "residential"; // String | see /reference
    Integer priceMin = 56; // Integer | 
    Integer priceMax = 56; // Integer | 
    Integer surfaceMin = 56; // Integer | 
    Integer surfaceMax = 56; // Integer | 
    Integer roomsMin = 56; // Integer | 
    Integer roomsMax = 56; // Integer | 
    Integer bathroomsMin = 56; // Integer | 
    String sort = "relevance"; // String | see /reference
    Integer page = 1; // Integer | 
    try {
      Object result = apiInstance.immobiliareSearchListings(market, location, regionId, provinceId, cityId, contract, category, priceMin, priceMax, surfaceMin, surfaceMax, roomsMin, roomsMax, bathroomsMin, sort, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImmobiliareApi#immobiliareSearchListings");
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
| **market** | **String**| it | es | gr | lu | [optional] [default to it] |
| **location** | **String**| Free-text place (auto-resolved) | [optional] |
| **regionId** | **String**| fkRegione (from /autocomplete) | [optional] |
| **provinceId** | **String**| idProvincia (from /autocomplete) | [optional] |
| **cityId** | **String**| idComune (from /autocomplete) | [optional] |
| **contract** | **String**| sale | rent | [optional] [default to sale] |
| **category** | **String**| see /reference | [optional] [default to residential] |
| **priceMin** | **Integer**|  | [optional] |
| **priceMax** | **Integer**|  | [optional] |
| **surfaceMin** | **Integer**|  | [optional] |
| **surfaceMax** | **Integer**|  | [optional] |
| **roomsMin** | **Integer**|  | [optional] |
| **roomsMax** | **Integer**|  | [optional] |
| **bathroomsMin** | **Integer**|  | [optional] |
| **sort** | **String**| see /reference | [optional] [default to relevance] |
| **page** | **Integer**|  | [optional] [default to 1] |

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


# DuckDuckGoApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**duckduckgoDuckduckgoScraperHealthCheck**](DuckDuckGoApi.md#duckduckgoDuckduckgoScraperHealthCheck) | **GET** /v1/duckduckgo/health | DuckDuckGo scraper health check |
| [**duckduckgoDuckduckgoScraperHealthCheckHead**](DuckDuckGoApi.md#duckduckgoDuckduckgoScraperHealthCheckHead) | **HEAD** /v1/duckduckgo/health | DuckDuckGo scraper health check |
| [**duckduckgoImageSearch**](DuckDuckGoApi.md#duckduckgoImageSearch) | **GET** /v1/duckduckgo/images | Image search |
| [**duckduckgoInstantAnswer**](DuckDuckGoApi.md#duckduckgoInstantAnswer) | **GET** /v1/duckduckgo/instant | Instant Answer |
| [**duckduckgoListSupportedRegions**](DuckDuckGoApi.md#duckduckgoListSupportedRegions) | **GET** /v1/duckduckgo/regions | List supported regions |
| [**duckduckgoNewsSearch**](DuckDuckGoApi.md#duckduckgoNewsSearch) | **GET** /v1/duckduckgo/news | News search |
| [**duckduckgoSearchSuggestions**](DuckDuckGoApi.md#duckduckgoSearchSuggestions) | **GET** /v1/duckduckgo/autocomplete | Search suggestions |
| [**duckduckgoVideoSearch**](DuckDuckGoApi.md#duckduckgoVideoSearch) | **GET** /v1/duckduckgo/videos | Video search |
| [**duckduckgoWebSearch**](DuckDuckGoApi.md#duckduckgoWebSearch) | **GET** /v1/duckduckgo/search | Web search |


<a id="duckduckgoDuckduckgoScraperHealthCheck"></a>
# **duckduckgoDuckduckgoScraperHealthCheck**
> Object duckduckgoDuckduckgoScraperHealthCheck()

DuckDuckGo scraper health check

Check health of the DuckDuckGo scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.DuckDuckGoApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DuckDuckGoApi apiInstance = new DuckDuckGoApi(defaultClient);
    try {
      Object result = apiInstance.duckduckgoDuckduckgoScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DuckDuckGoApi#duckduckgoDuckduckgoScraperHealthCheck");
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

<a id="duckduckgoDuckduckgoScraperHealthCheckHead"></a>
# **duckduckgoDuckduckgoScraperHealthCheckHead**
> Object duckduckgoDuckduckgoScraperHealthCheckHead()

DuckDuckGo scraper health check

Check health of the DuckDuckGo scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.DuckDuckGoApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DuckDuckGoApi apiInstance = new DuckDuckGoApi(defaultClient);
    try {
      Object result = apiInstance.duckduckgoDuckduckgoScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DuckDuckGoApi#duckduckgoDuckduckgoScraperHealthCheckHead");
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

<a id="duckduckgoImageSearch"></a>
# **duckduckgoImageSearch**
> Object duckduckgoImageSearch(query, region, safesearch, page, size, color, imageType, layout, license)

Image search

DuckDuckGo image search with size/color/type/layout/license filters.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.DuckDuckGoApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DuckDuckGoApi apiInstance = new DuckDuckGoApi(defaultClient);
    String query = "query_example"; // String | Search query
    String region = "wt-wt"; // String | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions.
    String safesearch = "moderate"; // String | on | moderate | off
    Integer page = 1; // Integer | 100 results per page
    String size = ""; // String | Small | Medium | Large | Wallpaper
    String color = ""; // String | color | Monochrome | Red | Blue | …
    String imageType = ""; // String | photo | clipart | gif | transparent | line
    String layout = ""; // String | Square | Tall | Wide
    String license = ""; // String | Any | Public | Share | ShareCommercially | Modify
    try {
      Object result = apiInstance.duckduckgoImageSearch(query, region, safesearch, page, size, color, imageType, layout, license);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DuckDuckGoApi#duckduckgoImageSearch");
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
| **query** | **String**| Search query | |
| **region** | **String**| DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to wt-wt] |
| **safesearch** | **String**| on | moderate | off | [optional] [default to moderate] |
| **page** | **Integer**| 100 results per page | [optional] [default to 1] |
| **size** | **String**| Small | Medium | Large | Wallpaper | [optional] [default to ] |
| **color** | **String**| color | Monochrome | Red | Blue | … | [optional] [default to ] |
| **imageType** | **String**| photo | clipart | gif | transparent | line | [optional] [default to ] |
| **layout** | **String**| Square | Tall | Wide | [optional] [default to ] |
| **license** | **String**| Any | Public | Share | ShareCommercially | Modify | [optional] [default to ] |

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

<a id="duckduckgoInstantAnswer"></a>
# **duckduckgoInstantAnswer**
> Object duckduckgoInstantAnswer(query)

Instant Answer

DuckDuckGo Instant Answer — abstract, definition, direct answer, related topics.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.DuckDuckGoApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DuckDuckGoApi apiInstance = new DuckDuckGoApi(defaultClient);
    String query = "query_example"; // String | Query for the Instant Answer API
    try {
      Object result = apiInstance.duckduckgoInstantAnswer(query);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DuckDuckGoApi#duckduckgoInstantAnswer");
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
| **query** | **String**| Query for the Instant Answer API | |

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

<a id="duckduckgoListSupportedRegions"></a>
# **duckduckgoListSupportedRegions**
> Object duckduckgoListSupportedRegions()

List supported regions

The full DuckDuckGo region (kl) code list.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.DuckDuckGoApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DuckDuckGoApi apiInstance = new DuckDuckGoApi(defaultClient);
    try {
      Object result = apiInstance.duckduckgoListSupportedRegions();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DuckDuckGoApi#duckduckgoListSupportedRegions");
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

<a id="duckduckgoNewsSearch"></a>
# **duckduckgoNewsSearch**
> Object duckduckgoNewsSearch(query, region, safesearch, timelimit, page)

News search

DuckDuckGo news search — headline, source, excerpt, unix + ISO date, image.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.DuckDuckGoApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DuckDuckGoApi apiInstance = new DuckDuckGoApi(defaultClient);
    String query = "query_example"; // String | Search query
    String region = "wt-wt"; // String | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions.
    String safesearch = "moderate"; // String | on | moderate | off
    String timelimit = ""; // String | day | week | month | year
    Integer page = 1; // Integer | 30 results per page
    try {
      Object result = apiInstance.duckduckgoNewsSearch(query, region, safesearch, timelimit, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DuckDuckGoApi#duckduckgoNewsSearch");
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
| **query** | **String**| Search query | |
| **region** | **String**| DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to wt-wt] |
| **safesearch** | **String**| on | moderate | off | [optional] [default to moderate] |
| **timelimit** | **String**| day | week | month | year | [optional] [default to ] |
| **page** | **Integer**| 30 results per page | [optional] [default to 1] |

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

<a id="duckduckgoSearchSuggestions"></a>
# **duckduckgoSearchSuggestions**
> Object duckduckgoSearchSuggestions(query, region)

Search suggestions

DuckDuckGo search-box suggestions.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.DuckDuckGoApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DuckDuckGoApi apiInstance = new DuckDuckGoApi(defaultClient);
    String query = "query_example"; // String | Partial query to complete
    String region = "wt-wt"; // String | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions.
    try {
      Object result = apiInstance.duckduckgoSearchSuggestions(query, region);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DuckDuckGoApi#duckduckgoSearchSuggestions");
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
| **query** | **String**| Partial query to complete | |
| **region** | **String**| DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to wt-wt] |

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

<a id="duckduckgoVideoSearch"></a>
# **duckduckgoVideoSearch**
> Object duckduckgoVideoSearch(query, region, safesearch, page, duration, resolution)

Video search

DuckDuckGo video search — title, publisher, uploader, duration, views, thumbnails.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.DuckDuckGoApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DuckDuckGoApi apiInstance = new DuckDuckGoApi(defaultClient);
    String query = "query_example"; // String | Search query
    String region = "wt-wt"; // String | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions.
    String safesearch = "moderate"; // String | on | moderate | off
    Integer page = 1; // Integer | 60 results per page
    String duration = ""; // String | short | medium | long
    String resolution = ""; // String | high | standard
    try {
      Object result = apiInstance.duckduckgoVideoSearch(query, region, safesearch, page, duration, resolution);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DuckDuckGoApi#duckduckgoVideoSearch");
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
| **query** | **String**| Search query | |
| **region** | **String**| DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to wt-wt] |
| **safesearch** | **String**| on | moderate | off | [optional] [default to moderate] |
| **page** | **Integer**| 60 results per page | [optional] [default to 1] |
| **duration** | **String**| short | medium | long | [optional] [default to ] |
| **resolution** | **String**| high | standard | [optional] [default to ] |

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

<a id="duckduckgoWebSearch"></a>
# **duckduckgoWebSearch**
> Object duckduckgoWebSearch(query, region, safesearch, timelimit, page)

Web search

DuckDuckGo web SERP — organic results, the zero-click abstract box, ads flagged.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.DuckDuckGoApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    DuckDuckGoApi apiInstance = new DuckDuckGoApi(defaultClient);
    String query = "query_example"; // String | Search query
    String region = "wt-wt"; // String | DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt = all regions.
    String safesearch = "moderate"; // String | on | moderate | off
    String timelimit = ""; // String | day | week | month | year
    Integer page = 1; // Integer | 
    try {
      Object result = apiInstance.duckduckgoWebSearch(query, region, safesearch, timelimit, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DuckDuckGoApi#duckduckgoWebSearch");
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
| **query** | **String**| Search query | |
| **region** | **String**| DuckDuckGo region code (kl), e.g. us-en, uk-en, de-de. wt-wt &#x3D; all regions. | [optional] [default to wt-wt] |
| **safesearch** | **String**| on | moderate | off | [optional] [default to moderate] |
| **timelimit** | **String**| day | week | month | year | [optional] [default to ] |
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


# BingApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**bingBingScraperHealthCheck**](BingApi.md#bingBingScraperHealthCheck) | **GET** /v1/bing/health | Bing scraper health check |
| [**bingBingScraperHealthCheckHead**](BingApi.md#bingBingScraperHealthCheckHead) | **HEAD** /v1/bing/health | Bing scraper health check |
| [**bingImageSearch**](BingApi.md#bingImageSearch) | **GET** /v1/bing/images | Image search |
| [**bingListSupportedMarkets**](BingApi.md#bingListSupportedMarkets) | **GET** /v1/bing/markets | List supported markets |
| [**bingNewsSearch**](BingApi.md#bingNewsSearch) | **GET** /v1/bing/news | News search |
| [**bingSearchSuggestions**](BingApi.md#bingSearchSuggestions) | **GET** /v1/bing/autocomplete | Search suggestions |
| [**bingVideoSearch**](BingApi.md#bingVideoSearch) | **GET** /v1/bing/videos | Video search |
| [**bingWebSearch**](BingApi.md#bingWebSearch) | **GET** /v1/bing/search | Web search |


<a id="bingBingScraperHealthCheck"></a>
# **bingBingScraperHealthCheck**
> Object bingBingScraperHealthCheck()

Bing scraper health check

Check health of the Bing scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BingApi apiInstance = new BingApi(defaultClient);
    try {
      Object result = apiInstance.bingBingScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BingApi#bingBingScraperHealthCheck");
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

<a id="bingBingScraperHealthCheckHead"></a>
# **bingBingScraperHealthCheckHead**
> Object bingBingScraperHealthCheckHead()

Bing scraper health check

Check health of the Bing scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BingApi apiInstance = new BingApi(defaultClient);
    try {
      Object result = apiInstance.bingBingScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BingApi#bingBingScraperHealthCheckHead");
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

<a id="bingImageSearch"></a>
# **bingImageSearch**
> Object bingImageSearch(query, market, count, safeSearch)

Image search

Bing Images — thumbnail, full-size and source URL per result.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BingApi apiInstance = new BingApi(defaultClient);
    String query = "query_example"; // String | Search keywords, e.g. 'golden retriever'
    String market = "en-US"; // String | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets.
    Integer count = 35; // Integer | Results to return
    String safeSearch = "safeSearch_example"; // String | off | moderate | strict
    try {
      Object result = apiInstance.bingImageSearch(query, market, count, safeSearch);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BingApi#bingImageSearch");
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
| **query** | **String**| Search keywords, e.g. &#39;golden retriever&#39; | |
| **market** | **String**| Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to en-US] |
| **count** | **Integer**| Results to return | [optional] [default to 35] |
| **safeSearch** | **String**| off | moderate | strict | [optional] |

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

<a id="bingListSupportedMarkets"></a>
# **bingListSupportedMarkets**
> Object bingListSupportedMarkets()

List supported markets

Supported Bing market codes. Free — costs no credits.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BingApi apiInstance = new BingApi(defaultClient);
    try {
      Object result = apiInstance.bingListSupportedMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BingApi#bingListSupportedMarkets");
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

<a id="bingNewsSearch"></a>
# **bingNewsSearch**
> Object bingNewsSearch(query, market, freshness)

News search

Bing News — headline, source, published time and snippet per article.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BingApi apiInstance = new BingApi(defaultClient);
    String query = "query_example"; // String | Search keywords, e.g. 'interest rates'
    String market = "en-US"; // String | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets.
    String freshness = "freshness_example"; // String | day | week | month — restrict to recent articles
    try {
      Object result = apiInstance.bingNewsSearch(query, market, freshness);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BingApi#bingNewsSearch");
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
| **query** | **String**| Search keywords, e.g. &#39;interest rates&#39; | |
| **market** | **String**| Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to en-US] |
| **freshness** | **String**| day | week | month — restrict to recent articles | [optional] |

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

<a id="bingSearchSuggestions"></a>
# **bingSearchSuggestions**
> Object bingSearchSuggestions(query, market)

Search suggestions

Bing search-box query suggestions.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BingApi apiInstance = new BingApi(defaultClient);
    String query = "query_example"; // String | Partial search term, e.g. 'coff'
    String market = "en-US"; // String | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets.
    try {
      Object result = apiInstance.bingSearchSuggestions(query, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BingApi#bingSearchSuggestions");
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
| **query** | **String**| Partial search term, e.g. &#39;coff&#39; | |
| **market** | **String**| Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to en-US] |

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

<a id="bingVideoSearch"></a>
# **bingVideoSearch**
> Object bingVideoSearch(query, market, count, safeSearch)

Video search

Bing Videos — title, thumbnail, duration, publisher and source per result.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BingApi apiInstance = new BingApi(defaultClient);
    String query = "query_example"; // String | Search keywords, e.g. 'espresso tutorial'
    String market = "en-US"; // String | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets.
    Integer count = 35; // Integer | Results to return
    String safeSearch = "safeSearch_example"; // String | off | moderate | strict
    try {
      Object result = apiInstance.bingVideoSearch(query, market, count, safeSearch);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BingApi#bingVideoSearch");
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
| **query** | **String**| Search keywords, e.g. &#39;espresso tutorial&#39; | |
| **market** | **String**| Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to en-US] |
| **count** | **Integer**| Results to return | [optional] [default to 35] |
| **safeSearch** | **String**| off | moderate | strict | [optional] |

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

<a id="bingWebSearch"></a>
# **bingWebSearch**
> Object bingWebSearch(query, market, count, offset, safeSearch)

Web search

Bing web SERP — organic results, ads, related searches and total count.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.BingApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    BingApi apiInstance = new BingApi(defaultClient);
    String query = "query_example"; // String | Search keywords, e.g. 'coffee machine'
    String market = "en-US"; // String | Bing market code, e.g. 'en-US', 'en-GB', 'de-DE'. See /markets.
    Integer count = 10; // Integer | Results per page (1-50)
    Integer offset = 0; // Integer | Zero-based result offset for pagination
    String safeSearch = "safeSearch_example"; // String | off | moderate | strict (default moderate)
    try {
      Object result = apiInstance.bingWebSearch(query, market, count, offset, safeSearch);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling BingApi#bingWebSearch");
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
| **query** | **String**| Search keywords, e.g. &#39;coffee machine&#39; | |
| **market** | **String**| Bing market code, e.g. &#39;en-US&#39;, &#39;en-GB&#39;, &#39;de-DE&#39;. See /markets. | [optional] [default to en-US] |
| **count** | **Integer**| Results per page (1-50) | [optional] [default to 10] |
| **offset** | **Integer**| Zero-based result offset for pagination | [optional] [default to 0] |
| **safeSearch** | **String**| off | moderate | strict (default moderate) | [optional] |

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


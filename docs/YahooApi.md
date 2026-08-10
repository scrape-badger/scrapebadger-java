# YahooApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**yahooImageSearch**](YahooApi.md#yahooImageSearch) | **GET** /v1/yahoo/images | Image search |
| [**yahooListSupportedMarkets**](YahooApi.md#yahooListSupportedMarkets) | **GET** /v1/yahoo/markets | List supported markets |
| [**yahooNewsSearch**](YahooApi.md#yahooNewsSearch) | **GET** /v1/yahoo/news | News search |
| [**yahooSearchSuggestions**](YahooApi.md#yahooSearchSuggestions) | **GET** /v1/yahoo/autocomplete | Search suggestions |
| [**yahooVideoSearch**](YahooApi.md#yahooVideoSearch) | **GET** /v1/yahoo/videos | Video search |
| [**yahooWebSearch**](YahooApi.md#yahooWebSearch) | **GET** /v1/yahoo/search | Web search |
| [**yahooYahooScraperHealthCheck**](YahooApi.md#yahooYahooScraperHealthCheck) | **GET** /v1/yahoo/health | Yahoo scraper health check |
| [**yahooYahooScraperHealthCheckHead**](YahooApi.md#yahooYahooScraperHealthCheckHead) | **HEAD** /v1/yahoo/health | Yahoo scraper health check |


<a id="yahooImageSearch"></a>
# **yahooImageSearch**
> Object yahooImageSearch(query, market, count)

Image search

Yahoo Images — thumbnail, full-size and source URL per result.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YahooApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YahooApi apiInstance = new YahooApi(defaultClient);
    String query = "query_example"; // String | Search keywords, e.g. 'golden retriever'
    String market = "us"; // String | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets.
    Integer count = 30; // Integer | Results to return
    try {
      Object result = apiInstance.yahooImageSearch(query, market, count);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YahooApi#yahooImageSearch");
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
| **market** | **String**| Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to us] |
| **count** | **Integer**| Results to return | [optional] [default to 30] |

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

<a id="yahooListSupportedMarkets"></a>
# **yahooListSupportedMarkets**
> Object yahooListSupportedMarkets()

List supported markets

Supported Yahoo market codes. Free — costs no credits.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YahooApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YahooApi apiInstance = new YahooApi(defaultClient);
    try {
      Object result = apiInstance.yahooListSupportedMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YahooApi#yahooListSupportedMarkets");
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

<a id="yahooNewsSearch"></a>
# **yahooNewsSearch**
> Object yahooNewsSearch(query, market)

News search

Yahoo News — headline, source, published time and snippet per article.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YahooApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YahooApi apiInstance = new YahooApi(defaultClient);
    String query = "query_example"; // String | Search keywords, e.g. 'interest rates'
    String market = "us"; // String | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets.
    try {
      Object result = apiInstance.yahooNewsSearch(query, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YahooApi#yahooNewsSearch");
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
| **market** | **String**| Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to us] |

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

<a id="yahooSearchSuggestions"></a>
# **yahooSearchSuggestions**
> Object yahooSearchSuggestions(query, market)

Search suggestions

Yahoo search-box query suggestions.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YahooApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YahooApi apiInstance = new YahooApi(defaultClient);
    String query = "query_example"; // String | Partial search term, e.g. 'coff'
    String market = "us"; // String | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets.
    try {
      Object result = apiInstance.yahooSearchSuggestions(query, market);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YahooApi#yahooSearchSuggestions");
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
| **market** | **String**| Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to us] |

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

<a id="yahooVideoSearch"></a>
# **yahooVideoSearch**
> Object yahooVideoSearch(query, market, count)

Video search

Yahoo Videos — title, thumbnail, duration, publisher and source per result.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YahooApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YahooApi apiInstance = new YahooApi(defaultClient);
    String query = "query_example"; // String | Search keywords, e.g. 'espresso tutorial'
    String market = "us"; // String | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets.
    Integer count = 30; // Integer | Results to return
    try {
      Object result = apiInstance.yahooVideoSearch(query, market, count);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YahooApi#yahooVideoSearch");
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
| **market** | **String**| Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to us] |
| **count** | **Integer**| Results to return | [optional] [default to 30] |

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

<a id="yahooWebSearch"></a>
# **yahooWebSearch**
> Object yahooWebSearch(query, market, offset, safeSearch)

Web search

Yahoo web SERP — organic results, ads, related searches and total count.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YahooApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YahooApi apiInstance = new YahooApi(defaultClient);
    String query = "query_example"; // String | Search keywords, e.g. 'coffee machine'
    String market = "us"; // String | Yahoo market code, e.g. 'us', 'uk', 'fr', 'de'. See /markets.
    Integer offset = 0; // Integer | Zero-based result offset for pagination
    String safeSearch = "safeSearch_example"; // String | off | moderate | strict (default moderate)
    try {
      Object result = apiInstance.yahooWebSearch(query, market, offset, safeSearch);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YahooApi#yahooWebSearch");
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
| **market** | **String**| Yahoo market code, e.g. &#39;us&#39;, &#39;uk&#39;, &#39;fr&#39;, &#39;de&#39;. See /markets. | [optional] [default to us] |
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

<a id="yahooYahooScraperHealthCheck"></a>
# **yahooYahooScraperHealthCheck**
> Object yahooYahooScraperHealthCheck()

Yahoo scraper health check

Check health of the Yahoo scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YahooApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YahooApi apiInstance = new YahooApi(defaultClient);
    try {
      Object result = apiInstance.yahooYahooScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YahooApi#yahooYahooScraperHealthCheck");
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

<a id="yahooYahooScraperHealthCheckHead"></a>
# **yahooYahooScraperHealthCheckHead**
> Object yahooYahooScraperHealthCheckHead()

Yahoo scraper health check

Check health of the Yahoo scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YahooApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YahooApi apiInstance = new YahooApi(defaultClient);
    try {
      Object result = apiInstance.yahooYahooScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YahooApi#yahooYahooScraperHealthCheckHead");
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


# YandexApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**yandexImageSearch**](YandexApi.md#yandexImageSearch) | **GET** /v1/yandex/images/search | Image search |
| [**yandexListSupportedMarkets**](YandexApi.md#yandexListSupportedMarkets) | **GET** /v1/yandex/markets | List supported markets |
| [**yandexReverseImageSearch**](YandexApi.md#yandexReverseImageSearch) | **GET** /v1/yandex/images/reverse | Reverse image search |
| [**yandexWebSearch**](YandexApi.md#yandexWebSearch) | **GET** /v1/yandex/search | Web search |
| [**yandexYandexScraperHealthCheck**](YandexApi.md#yandexYandexScraperHealthCheck) | **GET** /v1/yandex/health | Yandex scraper health check |
| [**yandexYandexScraperHealthCheckHead**](YandexApi.md#yandexYandexScraperHealthCheckHead) | **HEAD** /v1/yandex/health | Yandex scraper health check |


<a id="yandexImageSearch"></a>
# **yandexImageSearch**
> Object yandexImageSearch(query, domain, page)

Image search

Search Yandex Images by text — thumbnail, full-res URL, dimensions, source page.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YandexApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YandexApi apiInstance = new YandexApi(defaultClient);
    String query = "query_example"; // String | Image search query, e.g. 'coffee machine'
    String domain = "tr"; // String | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate.
    Integer page = 1; // Integer | 
    try {
      Object result = apiInstance.yandexImageSearch(query, domain, page);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YandexApi#yandexImageSearch");
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
| **query** | **String**| Image search query, e.g. &#39;coffee machine&#39; | |
| **domain** | **String**| Yandex market: &#39;tr&#39; (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), &#39;com&#39;, &#39;ru&#39;, &#39;by&#39;, &#39;kz&#39;, &#39;uz&#39;. &#39;com&#39;/&#39;ru&#39; have a lower success rate. | [optional] [default to tr] |
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

<a id="yandexListSupportedMarkets"></a>
# **yandexListSupportedMarkets**
> Object yandexListSupportedMarkets()

List supported markets

Supported Yandex markets (domains, default region and language).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YandexApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YandexApi apiInstance = new YandexApi(defaultClient);
    try {
      Object result = apiInstance.yandexListSupportedMarkets();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YandexApi#yandexListSupportedMarkets");
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

<a id="yandexReverseImageSearch"></a>
# **yandexReverseImageSearch**
> Object yandexReverseImageSearch(imageUrl, domain)

Reverse image search

Reverse image search by URL — hosting pages, similar images, tags, other sizes.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YandexApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YandexApi apiInstance = new YandexApi(defaultClient);
    String imageUrl = "imageUrl_example"; // String | Public URL of the image to reverse-search
    String domain = "tr"; // String | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate.
    try {
      Object result = apiInstance.yandexReverseImageSearch(imageUrl, domain);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YandexApi#yandexReverseImageSearch");
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
| **imageUrl** | **String**| Public URL of the image to reverse-search | |
| **domain** | **String**| Yandex market: &#39;tr&#39; (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), &#39;com&#39;, &#39;ru&#39;, &#39;by&#39;, &#39;kz&#39;, &#39;uz&#39;. &#39;com&#39;/&#39;ru&#39; have a lower success rate. | [optional] [default to tr] |

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

<a id="yandexWebSearch"></a>
# **yandexWebSearch**
> Object yandexWebSearch(query, domain, page, lr, lang)

Web search

Search Yandex web results — organic results, ads, displayed URLs, snippets.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YandexApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YandexApi apiInstance = new YandexApi(defaultClient);
    String query = "query_example"; // String | Search query, e.g. 'coffee machine'
    String domain = "tr"; // String | Yandex market: 'tr' (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), 'com', 'ru', 'by', 'kz', 'uz'. 'com'/'ru' have a lower success rate.
    Integer page = 1; // Integer | 
    Integer lr = 56; // Integer | Yandex region id, e.g. 213=Moscow, 84=USA
    String lang = "lang_example"; // String | UI language: ru, en, tr, be, kk, uk
    try {
      Object result = apiInstance.yandexWebSearch(query, domain, page, lr, lang);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YandexApi#yandexWebSearch");
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
| **query** | **String**| Search query, e.g. &#39;coffee machine&#39; | |
| **domain** | **String**| Yandex market: &#39;tr&#39; (yandex.com.tr, DEFAULT — the domain that reliably clears anti-bot), &#39;com&#39;, &#39;ru&#39;, &#39;by&#39;, &#39;kz&#39;, &#39;uz&#39;. &#39;com&#39;/&#39;ru&#39; have a lower success rate. | [optional] [default to tr] |
| **page** | **Integer**|  | [optional] [default to 1] |
| **lr** | **Integer**| Yandex region id, e.g. 213&#x3D;Moscow, 84&#x3D;USA | [optional] |
| **lang** | **String**| UI language: ru, en, tr, be, kk, uk | [optional] |

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

<a id="yandexYandexScraperHealthCheck"></a>
# **yandexYandexScraperHealthCheck**
> Object yandexYandexScraperHealthCheck()

Yandex scraper health check

Check health of the Yandex scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YandexApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YandexApi apiInstance = new YandexApi(defaultClient);
    try {
      Object result = apiInstance.yandexYandexScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YandexApi#yandexYandexScraperHealthCheck");
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

<a id="yandexYandexScraperHealthCheckHead"></a>
# **yandexYandexScraperHealthCheckHead**
> Object yandexYandexScraperHealthCheckHead()

Yandex scraper health check

Check health of the Yandex scraper service (accepts HEAD for UptimeRobot).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.YandexApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    YandexApi apiInstance = new YandexApi(defaultClient);
    try {
      Object result = apiInstance.yandexYandexScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling YandexApi#yandexYandexScraperHealthCheckHead");
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


# MetaAiApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**metaAiAskMetaAiAQuestion**](MetaAiApi.md#metaAiAskMetaAiAQuestion) | **GET** /v1/meta-ai/ask | Ask Meta AI a question |
| [**metaAiAskMetaAiAQuestionPost**](MetaAiApi.md#metaAiAskMetaAiAQuestionPost) | **POST** /v1/meta-ai/ask | Ask Meta AI a question (POST) |
| [**metaAiListMetaAiAssistantModes**](MetaAiApi.md#metaAiListMetaAiAssistantModes) | **GET** /v1/meta-ai/models | List Meta AI assistant modes |
| [**metaAiMetaAiScraperHealthCheck**](MetaAiApi.md#metaAiMetaAiScraperHealthCheck) | **GET** /v1/meta-ai/health | Meta AI scraper health check |
| [**metaAiMetaAiScraperHealthCheckHead**](MetaAiApi.md#metaAiMetaAiScraperHealthCheckHead) | **HEAD** /v1/meta-ai/health | Meta AI scraper health check |


<a id="metaAiAskMetaAiAQuestion"></a>
# **metaAiAskMetaAiAQuestion**
> Object metaAiAskMetaAiAQuestion(prompt, country)

Ask Meta AI a question

Send a prompt to meta.ai and get the answer (anonymous, no Meta account).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.MetaAiApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    MetaAiApi apiInstance = new MetaAiApi(defaultClient);
    String prompt = "prompt_example"; // String | The prompt to send to Meta AI (max 4000 characters).
    String country = "country_example"; // String | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'.
    try {
      Object result = apiInstance.metaAiAskMetaAiAQuestion(prompt, country);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MetaAiApi#metaAiAskMetaAiAQuestion");
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
| **prompt** | **String**| The prompt to send to Meta AI (max 4000 characters). | |
| **country** | **String**| ISO-3166 alpha-2 egress country, e.g. &#39;US&#39;, &#39;GB&#39;, &#39;DE&#39;. | [optional] |

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

<a id="metaAiAskMetaAiAQuestionPost"></a>
# **metaAiAskMetaAiAQuestionPost**
> Object metaAiAskMetaAiAQuestionPost()

Ask Meta AI a question (POST)

POST form of &#x60;/ask&#x60;, for prompts too long for a query string.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.MetaAiApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    MetaAiApi apiInstance = new MetaAiApi(defaultClient);
    try {
      Object result = apiInstance.metaAiAskMetaAiAQuestionPost();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MetaAiApi#metaAiAskMetaAiAQuestionPost");
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

<a id="metaAiListMetaAiAssistantModes"></a>
# **metaAiListMetaAiAssistantModes**
> Object metaAiListMetaAiAssistantModes(country)

List Meta AI assistant modes

Assistant modes meta.ai currently serves to an anonymous visitor.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.MetaAiApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    MetaAiApi apiInstance = new MetaAiApi(defaultClient);
    String country = "country_example"; // String | ISO-3166 alpha-2 egress country.
    try {
      Object result = apiInstance.metaAiListMetaAiAssistantModes(country);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MetaAiApi#metaAiListMetaAiAssistantModes");
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
| **country** | **String**| ISO-3166 alpha-2 egress country. | [optional] |

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

<a id="metaAiMetaAiScraperHealthCheck"></a>
# **metaAiMetaAiScraperHealthCheck**
> Object metaAiMetaAiScraperHealthCheck()

Meta AI scraper health check

Check health of the Meta AI scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.MetaAiApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    MetaAiApi apiInstance = new MetaAiApi(defaultClient);
    try {
      Object result = apiInstance.metaAiMetaAiScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MetaAiApi#metaAiMetaAiScraperHealthCheck");
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

<a id="metaAiMetaAiScraperHealthCheckHead"></a>
# **metaAiMetaAiScraperHealthCheckHead**
> Object metaAiMetaAiScraperHealthCheckHead()

Meta AI scraper health check

Check health of the Meta AI scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.MetaAiApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    MetaAiApi apiInstance = new MetaAiApi(defaultClient);
    try {
      Object result = apiInstance.metaAiMetaAiScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling MetaAiApi#metaAiMetaAiScraperHealthCheckHead");
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


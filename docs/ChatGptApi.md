# ChatGptApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**chatgptAskChatgptAQuestion**](ChatGptApi.md#chatgptAskChatgptAQuestion) | **GET** /v1/chatgpt/ask | Ask ChatGPT a question |
| [**chatgptAskChatgptAQuestionPost**](ChatGptApi.md#chatgptAskChatgptAQuestionPost) | **POST** /v1/chatgpt/ask | Ask ChatGPT a question (POST) |
| [**chatgptChatgptScraperHealthCheck**](ChatGptApi.md#chatgptChatgptScraperHealthCheck) | **GET** /v1/chatgpt/health | ChatGPT scraper health check |
| [**chatgptChatgptScraperHealthCheckHead**](ChatGptApi.md#chatgptChatgptScraperHealthCheckHead) | **HEAD** /v1/chatgpt/health | ChatGPT scraper health check |
| [**chatgptListChatgptModels**](ChatGptApi.md#chatgptListChatgptModels) | **GET** /v1/chatgpt/models | List ChatGPT models |
| [**chatgptMeasureABrandSVisibilityInAChatgptAnswer**](ChatGptApi.md#chatgptMeasureABrandSVisibilityInAChatgptAnswer) | **GET** /v1/chatgpt/brand-visibility | Measure a brand&#39;s visibility in a ChatGPT answer |
| [**chatgptMeasureABrandSVisibilityInAChatgptAnswerPost**](ChatGptApi.md#chatgptMeasureABrandSVisibilityInAChatgptAnswerPost) | **POST** /v1/chatgpt/brand-visibility | Measure a brand&#39;s visibility in a ChatGPT answer (POST) |


<a id="chatgptAskChatgptAQuestion"></a>
# **chatgptAskChatgptAQuestion**
> Object chatgptAskChatgptAQuestion(prompt, country, webSearch)

Ask ChatGPT a question

Send a prompt to ChatGPT and get the answer plus the web sources it cited.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ChatGptApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ChatGptApi apiInstance = new ChatGptApi(defaultClient);
    String prompt = "prompt_example"; // String | The prompt to send to ChatGPT (max 4096 characters).
    String country = "country_example"; // String | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'.
    String webSearch = "auto"; // String | auto (let ChatGPT decide) | force (ask it to browse) | off (answer from memory). `web_search_triggered` in the response always reports what actually happened.
    try {
      Object result = apiInstance.chatgptAskChatgptAQuestion(prompt, country, webSearch);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChatGptApi#chatgptAskChatgptAQuestion");
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
| **prompt** | **String**| The prompt to send to ChatGPT (max 4096 characters). | |
| **country** | **String**| ISO-3166 alpha-2 egress country, e.g. &#39;US&#39;, &#39;GB&#39;, &#39;DE&#39;. | [optional] |
| **webSearch** | **String**| auto (let ChatGPT decide) | force (ask it to browse) | off (answer from memory). &#x60;web_search_triggered&#x60; in the response always reports what actually happened. | [optional] [default to auto] |

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

<a id="chatgptAskChatgptAQuestionPost"></a>
# **chatgptAskChatgptAQuestionPost**
> Object chatgptAskChatgptAQuestionPost()

Ask ChatGPT a question (POST)

POST form of &#x60;/ask&#x60;, for prompts too long for a query string.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ChatGptApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ChatGptApi apiInstance = new ChatGptApi(defaultClient);
    try {
      Object result = apiInstance.chatgptAskChatgptAQuestionPost();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChatGptApi#chatgptAskChatgptAQuestionPost");
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

<a id="chatgptChatgptScraperHealthCheck"></a>
# **chatgptChatgptScraperHealthCheck**
> Object chatgptChatgptScraperHealthCheck()

ChatGPT scraper health check

Check health of the ChatGPT scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ChatGptApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ChatGptApi apiInstance = new ChatGptApi(defaultClient);
    try {
      Object result = apiInstance.chatgptChatgptScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChatGptApi#chatgptChatgptScraperHealthCheck");
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

<a id="chatgptChatgptScraperHealthCheckHead"></a>
# **chatgptChatgptScraperHealthCheckHead**
> Object chatgptChatgptScraperHealthCheckHead()

ChatGPT scraper health check

Check health of the ChatGPT scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ChatGptApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ChatGptApi apiInstance = new ChatGptApi(defaultClient);
    try {
      Object result = apiInstance.chatgptChatgptScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChatGptApi#chatgptChatgptScraperHealthCheckHead");
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

<a id="chatgptListChatgptModels"></a>
# **chatgptListChatgptModels**
> Object chatgptListChatgptModels(country)

List ChatGPT models

Models chatgpt.com currently serves to an anonymous visitor.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ChatGptApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ChatGptApi apiInstance = new ChatGptApi(defaultClient);
    String country = "country_example"; // String | ISO-3166 alpha-2 egress country.
    try {
      Object result = apiInstance.chatgptListChatgptModels(country);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChatGptApi#chatgptListChatgptModels");
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

<a id="chatgptMeasureABrandSVisibilityInAChatgptAnswer"></a>
# **chatgptMeasureABrandSVisibilityInAChatgptAnswer**
> Object chatgptMeasureABrandSVisibilityInAChatgptAnswer(prompt, brand, domain, aliases, competitors, country, webSearch)

Measure a brand&#39;s visibility in a ChatGPT answer

Ask ChatGPT, then report whether the brand is mentioned, cited and how prominently.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ChatGptApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ChatGptApi apiInstance = new ChatGptApi(defaultClient);
    String prompt = "prompt_example"; // String | The prompt to ask ChatGPT.
    String brand = "brand_example"; // String | Brand name to look for in the answer.
    String domain = "domain_example"; // String | Brand domain, for citation matching.
    String aliases = "aliases_example"; // String | Comma-separated alternative names.
    String competitors = "competitors_example"; // String | Comma-separated competitor names.
    String country = "country_example"; // String | ISO-3166 alpha-2 egress country.
    String webSearch = "force"; // String | auto | force | off
    try {
      Object result = apiInstance.chatgptMeasureABrandSVisibilityInAChatgptAnswer(prompt, brand, domain, aliases, competitors, country, webSearch);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChatGptApi#chatgptMeasureABrandSVisibilityInAChatgptAnswer");
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
| **prompt** | **String**| The prompt to ask ChatGPT. | |
| **brand** | **String**| Brand name to look for in the answer. | |
| **domain** | **String**| Brand domain, for citation matching. | [optional] |
| **aliases** | **String**| Comma-separated alternative names. | [optional] |
| **competitors** | **String**| Comma-separated competitor names. | [optional] |
| **country** | **String**| ISO-3166 alpha-2 egress country. | [optional] |
| **webSearch** | **String**| auto | force | off | [optional] [default to force] |

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

<a id="chatgptMeasureABrandSVisibilityInAChatgptAnswerPost"></a>
# **chatgptMeasureABrandSVisibilityInAChatgptAnswerPost**
> Object chatgptMeasureABrandSVisibilityInAChatgptAnswerPost()

Measure a brand&#39;s visibility in a ChatGPT answer (POST)

POST form, for longer prompts and larger competitor sets.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.ChatGptApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    ChatGptApi apiInstance = new ChatGptApi(defaultClient);
    try {
      Object result = apiInstance.chatgptMeasureABrandSVisibilityInAChatgptAnswerPost();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ChatGptApi#chatgptMeasureABrandSVisibilityInAChatgptAnswerPost");
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


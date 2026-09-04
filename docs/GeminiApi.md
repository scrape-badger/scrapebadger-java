# GeminiApi

All URIs are relative to *https://scrapebadger.com*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**geminiAskGeminiAQuestion**](GeminiApi.md#geminiAskGeminiAQuestion) | **GET** /v1/gemini/ask | Ask Gemini a question |
| [**geminiAskGeminiAQuestionPost**](GeminiApi.md#geminiAskGeminiAQuestionPost) | **POST** /v1/gemini/ask | Ask Gemini a question (POST) |
| [**geminiGeminiScraperHealthCheck**](GeminiApi.md#geminiGeminiScraperHealthCheck) | **GET** /v1/gemini/health | Gemini scraper health check |
| [**geminiGeminiScraperHealthCheckHead**](GeminiApi.md#geminiGeminiScraperHealthCheckHead) | **HEAD** /v1/gemini/health | Gemini scraper health check |
| [**geminiMeasureABrandSVisibilityInAGeminiAnswer**](GeminiApi.md#geminiMeasureABrandSVisibilityInAGeminiAnswer) | **GET** /v1/gemini/brand-visibility | Measure a brand&#39;s visibility in a Gemini answer |
| [**geminiMeasureABrandSVisibilityInAGeminiAnswerPost**](GeminiApi.md#geminiMeasureABrandSVisibilityInAGeminiAnswerPost) | **POST** /v1/gemini/brand-visibility | Measure a brand&#39;s visibility in a Gemini answer (POST) |


<a id="geminiAskGeminiAQuestion"></a>
# **geminiAskGeminiAQuestion**
> Object geminiAskGeminiAQuestion(prompt, country, webSearch, imageUrl)

Ask Gemini a question

Send a prompt to Gemini and get the answer plus the web sources it cited.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GeminiApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GeminiApi apiInstance = new GeminiApi(defaultClient);
    String prompt = "prompt_example"; // String | The prompt to send to Gemini (max 4096 characters).
    String country = "country_example"; // String | ISO-3166 alpha-2 egress country, e.g. 'US', 'GB', 'DE'.
    String webSearch = "auto"; // String | auto (let Gemini decide) | force (ask it to browse) | off (answer from memory). `web_search_triggered` in the response always reports what actually happened.
    String imageUrl = "imageUrl_example"; // String | Public http(s) URL of an image to attach to the prompt. Gemini reads it and answers about it. POST also accepts `image_base64`. Exactly one of the two.
    try {
      Object result = apiInstance.geminiAskGeminiAQuestion(prompt, country, webSearch, imageUrl);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GeminiApi#geminiAskGeminiAQuestion");
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
| **prompt** | **String**| The prompt to send to Gemini (max 4096 characters). | |
| **country** | **String**| ISO-3166 alpha-2 egress country, e.g. &#39;US&#39;, &#39;GB&#39;, &#39;DE&#39;. | [optional] |
| **webSearch** | **String**| auto (let Gemini decide) | force (ask it to browse) | off (answer from memory). &#x60;web_search_triggered&#x60; in the response always reports what actually happened. | [optional] [default to auto] |
| **imageUrl** | **String**| Public http(s) URL of an image to attach to the prompt. Gemini reads it and answers about it. POST also accepts &#x60;image_base64&#x60;. Exactly one of the two. | [optional] |

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

<a id="geminiAskGeminiAQuestionPost"></a>
# **geminiAskGeminiAQuestionPost**
> Object geminiAskGeminiAQuestionPost()

Ask Gemini a question (POST)

POST form of &#x60;/ask&#x60;, for prompts too long for a query string.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GeminiApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GeminiApi apiInstance = new GeminiApi(defaultClient);
    try {
      Object result = apiInstance.geminiAskGeminiAQuestionPost();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GeminiApi#geminiAskGeminiAQuestionPost");
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

<a id="geminiGeminiScraperHealthCheck"></a>
# **geminiGeminiScraperHealthCheck**
> Object geminiGeminiScraperHealthCheck()

Gemini scraper health check

Check health of the Gemini scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GeminiApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GeminiApi apiInstance = new GeminiApi(defaultClient);
    try {
      Object result = apiInstance.geminiGeminiScraperHealthCheck();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GeminiApi#geminiGeminiScraperHealthCheck");
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

<a id="geminiGeminiScraperHealthCheckHead"></a>
# **geminiGeminiScraperHealthCheckHead**
> Object geminiGeminiScraperHealthCheckHead()

Gemini scraper health check

Check health of the Gemini scraper service (accepts HEAD).

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GeminiApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GeminiApi apiInstance = new GeminiApi(defaultClient);
    try {
      Object result = apiInstance.geminiGeminiScraperHealthCheckHead();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GeminiApi#geminiGeminiScraperHealthCheckHead");
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

<a id="geminiMeasureABrandSVisibilityInAGeminiAnswer"></a>
# **geminiMeasureABrandSVisibilityInAGeminiAnswer**
> Object geminiMeasureABrandSVisibilityInAGeminiAnswer(prompt, brand, domain, aliases, competitors, country, webSearch)

Measure a brand&#39;s visibility in a Gemini answer

Ask Gemini, then report whether the brand is mentioned, cited and how prominently.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GeminiApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GeminiApi apiInstance = new GeminiApi(defaultClient);
    String prompt = "prompt_example"; // String | The prompt to ask Gemini.
    String brand = "brand_example"; // String | Brand name to look for in the answer.
    String domain = "domain_example"; // String | Brand domain, for citation matching.
    String aliases = "aliases_example"; // String | Comma-separated alternative names.
    String competitors = "competitors_example"; // String | Comma-separated competitor names.
    String country = "country_example"; // String | ISO-3166 alpha-2 egress country.
    String webSearch = "force"; // String | auto | force | off
    try {
      Object result = apiInstance.geminiMeasureABrandSVisibilityInAGeminiAnswer(prompt, brand, domain, aliases, competitors, country, webSearch);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GeminiApi#geminiMeasureABrandSVisibilityInAGeminiAnswer");
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
| **prompt** | **String**| The prompt to ask Gemini. | |
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

<a id="geminiMeasureABrandSVisibilityInAGeminiAnswerPost"></a>
# **geminiMeasureABrandSVisibilityInAGeminiAnswerPost**
> Object geminiMeasureABrandSVisibilityInAGeminiAnswerPost()

Measure a brand&#39;s visibility in a Gemini answer (POST)

POST form, for longer prompts and larger competitor sets.

### Example
```java
// Import classes:
import com.scrapebadger.client.ApiClient;
import com.scrapebadger.client.ApiException;
import com.scrapebadger.client.Configuration;
import com.scrapebadger.client.auth.*;
import com.scrapebadger.client.models.*;
import com.scrapebadger.client.api.GeminiApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("https://scrapebadger.com");
    
    // Configure API key authorization: ApiKeyAuth
    ApiKeyAuth ApiKeyAuth = (ApiKeyAuth) defaultClient.getAuthentication("ApiKeyAuth");
    ApiKeyAuth.setApiKey("YOUR API KEY");
    // Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
    //ApiKeyAuth.setApiKeyPrefix("Token");

    GeminiApi apiInstance = new GeminiApi(defaultClient);
    try {
      Object result = apiInstance.geminiMeasureABrandSVisibilityInAGeminiAnswerPost();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling GeminiApi#geminiMeasureABrandSVisibilityInAGeminiAnswerPost");
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

